# ENTITY — Entity Brain 

This module decides **if** and **what** ENTITY says, with a “cinematic” pace and consistent style.

* **TemporalController** → senses silence/tension over time and decides *whether to speak now*.
* **Remote Generator (HF)** → asks the model (Mixtral) for a sentence.
* **Validator** → cleans and accepts only suitable sentences (8–16 words, correct tone).
* **Scene3** → also maintains a **local memory (history)** that passes to the brain to provide context, so that ENTITY doesn't speak “into the void”.

---

## Glossary (key terms)

* **EMA (Exponential Moving Average)**
Exponential Moving Average: updates a state (“how high is the tension?”) giving **more weight to recent values**.
Parameter: **half-life** (see below).

* **Half-life**
Time after which information becomes **half** in weight.
Example: `hl_short=4s` → the tension from 4 seconds ago weighs ~50% of what it is now.

* **Silence normalization (`s_norm`)**
Converts the seconds of silence to a value **0..1** (e.g., 60s ≈ 1.0) to use silence within EMAs.

* **Emotions with hysteresis**
Discrete state: `curious | bored | irritated`.
**Hysteresis** = minimum wait (`emotion_min_dwell`) before changing, to avoid continuous bounces.

* **Emotion bias**
Probabilistic offset related to emotion (e.g., *irritated* slightly increases the desire to speak).

* **Temporal boost**
Bonus if the **silence exceeds** thresholds: `min_gap_micro/short/long`.
Idea: the longer the pause, the more sense it makes for ENTITY to break in.

* **Speak rate (speaks/minute)**
EMA of the rate at which ENTITY has spoken recently.
It serves to **self-brake** if it has just spoken too much.

* **Rate term**
Correction of the probability based on the **speak rate** compared to the **target** (if it has spoken too much → brake; if it has spoken too little → slight push).

* **Probabilistic gating**
Calculation of a probability `p` (0..1). ENTITY speaks if `random() < p`.
`p` is a mix of: base, tension, memory (accumulated silence), emotion, temporal boost, rate term, noise.

* **History (local memory in Scene3)**
A list of `(role, text)` pairs labeled `"USER"` or `"ENTITY"`.
It is used to build a **mini-contextual dialogue** that is passed to the model.
It is **very primitive**: it only keeps the last `MAX_TURNS` keystrokes.
It is not “true semantic memory,” but it prevents ENTITY from responding unrelatedly.

* **Auto-talk (heartbeat)**
Periodic heartbeat that can trigger a response **even without the user submitting** (always filtered by the gate).

* **Pre-clean**
“Coarse” cleaning of the model text: links, markdown, bullets, meta brackets… before validating.

* **Validator**
Final checks: **first sentence**, final punctuation, **6–16 words**, plausible Italian words, no recent duplicates.

* **Stop tokens**
Sequences that tell the model to **stop** (e.g., `"\n"`, `ENTITY:`, `IO:`, quotes, `•`, `http`, `[`/`(`).

---

## Synthetic Architecture

```
[Scene3] --(history + tension + silence_sec)--> [TemporalController]
|
[should_speak?]
yes -------/ \-------- no
|
[HF Generation (Mixtral)]
|
[Pre-clean]
|
[Validator]
|
[Final Sentence]
```

---

## Local Storage in Scene3

Current Snippet:

```python
# Conversation (User only ↔ ENTITY)
history = []
MAX_TURNS = 8 # how many pairs to keep in the brain context

def push(role: str, text: str):
if not text:
return
history.append((role, text.strip()))
if len(history) > MAX_TURNS * 2:
del history[0:len(history) - MAX_TURNS * 2]

def build_context() -> str:
lines = []
for role, text in history[-MAX_TURNS*2:]:
if role == "USER":
lines.append(f"IO: {text}")
else:
lines.append(f"ENTITY: {text}")
return "\n".join(lines)
```

* Keeps **only the last lines** of IO and ENTITY.
* Builds a simple context to give to the model.
* It is useful for **maintaining immediate consistency** (e.g., ENTITY responds by connecting to the sentence in IO).
* It's not a "real" memory like a knowledge base: it's a **rolling buffer**.

---

## TL;DR

* The **EntityBrain** manages *when* and *how* ENTITY speaks, with EMA, probabilistic gating, and emotions.
* In **Scene3**, there's a **minimal local memory** that preserves the last turns and provides narrative coherence.
* Together, these two layers make ENTITY both **temporally autonomous** and **contextual**.

---

## [Showcase](https://www.youtube.com/watch?v=3mbZdoRYnSA)

The video shows how **ENTITY** doesn't always respond:

* the user's messages are displayed in the box at the bottom, in the background of the scene;
* each input is passed to the ENTITY's "brain," which evaluates whether it's worth intervening;
* sometimes the sentence is **discarded** not because it's incomprehensible, but because the ENTITY, based on its internal state (tension, accumulated silence, emotion), decides to **keep quiet**.

This makes the conversation less predictable and more "alive": the user perceives that the ENTITY **chooses when to speak**, as if it had its own interests or annoyances. In practice, it's not a linear chatbot that always responds, but a **narrative presence** that filters messages and reacts only when it truly wants to disrupt.
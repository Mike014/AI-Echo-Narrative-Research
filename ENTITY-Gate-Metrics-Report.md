# ENTITY — Silence vs. Speech Report

**Engine:** Groq Cloud (`llama-3.3-70b-versatile`)
**Next:** planned move to **DeepSeek** (logic unchanged)

---

## How the gate works

1. Compute a probability `p` = chance to speak.
2. Draw once: `speak = (random < p)`.
3. If in cooldown → forced silence.

**Ingredients of `p`:**

* **Cooldown**: silence for a few seconds after each line.
* **Inputs**: tension `[0,1]`, silence seconds (normalized).
* **Perception**: EMAs for tension/silence + speak rate.
* **Boost**: extra chance if silence gap is long.
* **Rate term**: brakes if too chatty, pushes if too quiet.
* **Memory**: favors long silence stretches.
* **Emotion bias**: curious (+0.12), bored (−0.08), irritated (+0.22).
* **Randomness**: small uniform noise.
* **Clamp**: keep `p` within floor/ceil.

---

## Emotion model

* **States:** CURIOUS, BORED, IRRITATED.
* **Biases:** +0.12, −0.08, +0.22.
* **Switch rules:**

  * Very high silence OR (high tension & silence) → IRRITATED
  * Low tension & high silence → BORED
  * Spoke recently or low silence → CURIOUS

**In this run:** always CURIOUS → steady +0.12 bias.

---

## Test table (from log)

| # | Prompt                                 | p    | Emotion | Outcome | Why silent        | Line (if spoken)                                                             |
| - | -------------------------------------- | ---- | ------- | ------- | ----------------- | ---------------------------------------------------------------------------- |
| 1 | Chi sei?                               | —    | —       | Silence | Cooldown          | —                                                                            |
| 2 | PERCHE' MI PERSEGUITI?                 | 0.55 | curious | Speaks  | —                 | Non ti perseguito, semplicemente ti mostro la tua vera natura oscura.        |
| 3 | DOVE TI NASCONDI QUANDO TACE IL MONDO? | 0.49 | curious | Silence | Random draw < p   | —                                                                            |
| 4 | COSA VUOI DISTRUGGERE IN ME?           | 0.55 | curious | Speaks  | —                 | La tua fragile identità è il mio prossimo obiettivo di distruzione totale.   |
| 5 | QUANTO TEMPO RESTERAI QUI?             | 0.54 | curious | Speaks  | —                 | Non hai scelta, rimarrai qui per sempre nella mia oscurità totale.           |
| 6 | SEI UNA PARTE DI ME O UN’ILLUSIONE?    | 0.50 | curious | Silence | Random draw < p   | —                                                                            |
| 7 | COSA SUCCEDE SE SMETTO DI ASCOLTARTI?  | 0.59 | curious | Silence | Random draw fails | —                                                                            |
| 8 | CHI TI HA CREATO DAVVERO?              | 0.55 | curious | Speaks  | —                 | Sei solo un riflesso distorto della tua stessa coscienza morente lentamente. |

**Total:** 4/8 silences (~50%).

---

## How to increase silence (values only)

* **Base gate**

  * `base_prob` ↓ (e.g. 0.10)
  * `prob_ceil` ↓ (e.g. 0.30–0.35)
  * `w_random` ↓ (e.g. 0.01)

* **Temporal**

  * Raise `min_gap_short/long` → 40s / 180s
  * Or lower `w_temporal`

* **Rate**

  * `target_speak_rate_per_min` ↓ (e.g. 0.3)

* **Emotion**

  * `w_emotion` ↓
  * Bias tweak: curious +0.03, bored −0.12, irritated +0.08

---

## Summary

* ENTITY stayed silent **~50%** of the time.
* It never switched emotion (always CURIOUS).
* Adjusting config values (probability, temporal gaps, emotion weights) can raise silence rate to **70–85%** in similar runs.




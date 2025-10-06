# AI Echo Narrative Research

**Independent Research Project**
Michele Grimaldi · 2025

---

## Overview

This repository documents an **independent research prototype** at the intersection of **AI (agentic AI), game design, digital narrative, sound design, poetry, and psychology**.

The work originates from *Dialoghi con un’Eco* and evolves into a **digital psychodrama** where **ENTITY**—not a scripted NPC but an **agentic AI**—can **choose when to speak or remain silent**. A **Temporal Controller** (multi-scale EMA, hysteresis, cooldown) turns **time and silence** into first-class mechanics, avoiding chatbot-style reactivity.

Three core components anchor the prototype:

* **Entity Brain + Temporal Controller** — governs silence/speech decisions, timing, and mood-biased interventions.
* **Metronarrative framework** — scenes aligned to a beat/tempo grid where rhythm, pauses, and breaks carry narrative meaning.
* **Entity Director (real-time notifications & paratext)** — an external orchestrator that reads dialog context, scores emotional channels, and triggers **sandboxed** side-effects (desktop-style note lines, guaranteed in-game toasts, optional OS-aware toasts) with **cooldowns** and **de-duplication**.

The **engine is functional**: ENTITY reacts autonomously, metronarrative scenes run end-to-end, and the **Entity Director** coordinates real-time side effects safely. What’s still in progress is the **game-design articulation** (core loop, player verbs, onboarding) to turn the research system into a fully playable slice.

### Recent engine updates

* **Neural TTS voice for ENTITY**
  A new voice pipeline (Neural TTS + light post-FX) delivers a **hybrid timbre**—influenced by Heath Ledger’s Joker (attack/taunt) and grunge textures (Layne Staley, Kurt Cobain). Result: **more fluid laugh transitions** and a darker, controlled **single-sentence** delivery.

* **Environment detection (“establish environment”)**
  Runtime detection of **OS and screen resolution/DPI** to:

  * scale UI safely across displays,
  * enable **OS-aware affordances** in a **sandboxed** manner (simulate notes/overlays in-game when **Safe Mode** is on),
  * log session metadata (`os`, `resolution`, `dpi`) for tuning.

> Status: suitable for a **mini-demo** (engine-first). Next steps: packaging, safe defaults, and a clearer core loop.
> 
---

**YouTube Showcase Playlist** → [Watch the Video](https://www.youtube.com/watch?v=0Y-_Rt0oZkU&list=PLgKASgLUSpNYKyusWO6iHcxTe-odeIho1)

---

## Index of Research (Restructured)

### 0) Vision & Premise

* **Draft of the Premise (notebook)**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Creative_Writing/Draft_of_the_Premise.ipynb](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Creative_Writing/Draft_of_the_Premise.ipynb)
  *One-line premise and highlighted version; establishes IO–COSCIENZA–ENTITÀ → LUI and the “integrated–hard” outcome (power without consolation).*
* **Anatomy of Story — Working Notes** *(placeholder)*
  *Applying Truby’s premise, 7 steps, and designing principle to Dialoghi con un Eco; keeps the story organic and unified.*

---

### 1) Narrative Architecture (Story Space & Influences)

* **Lore / World & Parallels**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/narrative-parallels-bandersnatch-dialoghi.md](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/narrative-parallels-bandersnatch-dialoghi.md)
  *World/lore of the project and narrative parallels with Bandersnatch; defines tone, rules, and the meta layer.*
* **Dialoghi con un’Eco: AI, Digital Trauma, and Interactive Narrative**
  [https://medium.com/@mikgrimaldi7/dialoghi-con-uneco-ai-digital-trauma-and-interactive-narrative-4e818c451d8e](https://medium.com/@mikgrimaldi7/dialoghi-con-uneco-ai-digital-trauma-and-interactive-narrative-4e818c451d8e)
  *Introduces the triad (IO–COSCIENZA–ENTITÀ), digital psychodrama, and the diary format as diegetic structure.*
* **Dialogues with an Echo — Part 2**
  [https://medium.com/@mikgrimaldi7/dialogues-with-an-echo-digital-trauma-and-interactive-narrative-3aedb850eea4](https://medium.com/@mikgrimaldi7/dialogues-with-an-echo-digital-trauma-and-interactive-narrative-3aedb850eea4)
  *Explores dissociation, memory, and trauma via interwoven voices; expands the symbolic roles of IO/ENTITÀ/COSCIENZA.*
* **Suspended Epilogue**
  [https://medium.com/@mikgrimaldi7/dialoghi-con-uneco-560299e444be](https://medium.com/@mikgrimaldi7/dialoghi-con-uneco-560299e444be)
  *“What am I?” as identity hinge; outlines a non-consolatory ending logic.*
* **Batman: Zur-En-Arrh vs. Dialoghi con un’Eco**
  [https://medium.com/@mikgrimaldi7/batman-zur-en-arrh-vs-dialoghi-con-uneco-symbolic-death-ego-failsafe-and-triadic-integration-6cc5f8fe68c5](https://medium.com/@mikgrimaldi7/batman-zur-en-arrh-vs-dialoghi-con-uneco-symbolic-death-ego-failsafe-and-triadic-integration-6cc5f8fe68c5)
  *Frames LEI as trigger, ENTITÀ as intrusive failsafe, and COSCIENZA as containment—triadic integration lens.*
* **Entity vs Pax**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/The-Entity-vs-Pax.md](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/The-Entity-vs-Pax.md)
  *Compares ENTITÀ with Bandersnatch’s Pax to clarify antagonism, agency, and meta control.*
* **Generative Agents vs Black Mirror Plaything**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Generative_Agents_vs_Black_Mirror_Plaything_Analysis.md](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Generative_Agents_vs_Black_Mirror_Plaything_Analysis.md)
  *Convergent mechanics for simulated minds and authored meta-narratives; where they align/diverge.*
* **Meta Gaming**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Meta-Gaming.md](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Meta-Gaming.md)
  *Player awareness, authorial intrusion, and meta signals as part of the diegesis.*

---

### 2) Game Design Framework

* **MDA Framework — Dialoghi con un’Eco**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/MDA.ipynb](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/MDA.ipynb)
  *Mechanics–Dynamics–Aesthetics mapping; introduces “metronarrative” beats for identity pressure and release.*
* **Game System — Dialoghi con un’Eco**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Game-System.ipynb](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Game-System.ipynb)
  *Scene-driven psychodrama structure; defines goals, obstacles, decisions, and costs (IO vs ENTITÀ under COSCIENZA).*
* **Meta Gaming (design lens)**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Meta-Gaming.md](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Meta-Gaming.md)
  *Design rules for fourth-wall nudges, diegetic UI, and narrative reliability.*

---

### 3) Engine & AI Architecture

* **ENTITÀ: Entity Brain & Temporal Controller**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/entita-brain-temporal-controller.md](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/entita-brain-temporal-controller.md)
  *Core control loop: silence vs speech gating, emotional state machine, escalating pressure on IO.*
* **Temporal Controller (spec)**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/TemporalController.md](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/TemporalController.md)
  *Decision policy for whether ENTITÀ speaks, waits, or withholds—narrative pacing lever.*
* **ENTITÀ — Non-Deterministic NPCs**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/ENTIT%C3%80-Non-Deterministic-NPCs.ipynb](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/ENTIT%C3%80-Non-Deterministic-NPCs.ipynb)
  *Asymmetric, stochastic behaviors that keep ENTITÀ legible yet unpredictable.*
* **Silence vs. Speech Report**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/ENTITY-Gate-Metrics-Report.md](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/ENTITY-Gate-Metrics-Report.md)
  *Why silence matters; how withholding becomes a functional narrative device (tension, anticipation).*
* **Affective State & Behavior of ENTITÀ**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Report%E2%80%94Affective-state-and-behavior-of-ENTITY.ipynb](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Report%E2%80%94Affective-state-and-behavior-of-ENTITY.ipynb)
  *Mood trajectory model (silence → curious → bored → irritated) and its triggers; effects on player experience.*
* **Unity Inference Engine (exploration)**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Unity-Inference-AI-Engine/Unity-Inference-Engine.ipynb](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Unity-Inference-AI-Engine/Unity-Inference-Engine.ipynb)
  *Early prototype for integrating inference pipelines into a realtime environment.*
* **ENTITÀ Web Demo (diegetic site)**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Entit%C3%A0_Web_Demo_Attempt1.ipynb](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Entit%C3%A0_Web_Demo_Attempt1.ipynb)
  *Diegetic, in-world web surface; supports mystery-drop pacing and indirect exposition.*

---

### 4) Metrics & Evaluation

* **Gate Metrics — Silence/Speech**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/ENTITY-Gate-Metrics-Report.md](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/ENTITY-Gate-Metrics-Report.md)
  *Quantifies when ENTITÀ should speak or stay silent; correlates gating with tension and comprehension.*
* **Affective Trajectories**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Report%E2%80%94Affective-state-and-behavior-of-ENTITY.ipynb](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Report%E2%80%94Affective-state-and-behavior-of-ENTITY.ipynb)
  *Measures mood shifts and their downstream narrative effects; informs tuning of the temporal controller.*

---

### 5) Research Corpus (Background & Theory)

* **Generative Agents: Interactive Simulacra of Human Behavior**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Research/Generative-Agents-Interactive-Simulacra-of-Human-Behavior.ipynb](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Research/Generative-Agents-Interactive-Simulacra-of-Human-Behavior.ipynb)
  *Reference work for memory, reflection, and planning modules in simulated agents.*
* **Generative Agents — Structure (notes)**
  [https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Generative-Agents.ipynb](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Generative-Agents.ipynb)
  *Practical breakdown of Memory / Reflection / Planning and how they map to ENTITÀ.*

---

### 6) Publications & Dissemination

* **Preprint (Zenodo) — Ongoing Research in Development**
  [https://zenodo.org/records/17198849](https://zenodo.org/records/17198849)
  *Living preprint documenting narrative design, AI control strategies, and psychodrama framing.*

---

### 7) Safety, Ethics & Content Guidelines

*(for handling sensitive topics with care while maintaining artistic intent)*

* **Intent & Framing**: portray loneliness, intrusive thoughts, and self-destructive ideation **without glamorization**; highlight consequences and limits.
* **Diegetic Safeguards**: within the story, COSCIENZA enforces **boundaries, pauses, and escalation limits**; ENTITÀ’s pressure is contextualized, not celebrated.
* **Alternatives & Agency**: show **choices that de-escalate** (contact, delay, routine) even if the protagonist refuses them; agency is visible, not removed.
* **Language**: avoid sensational detail; prefer **clear, clinical phrasing** for harm-related content.
* **Signals & Warnings**: provide **content notes** in intros/menus; allow players/readers to opt out of certain sequences.
* **Resources (Credits/Appendix)**: include pointers to **support resources** and mental health hotlines relevant to the target regions.
* **Testing & Review**: involve sensitivity readers or trusted peers to flag unintended glorification or harm patterns.
* **Documentation**: keep a changelog of **design decisions** tied to ethics (why a scene exists, what function it serves, what safeguards are in place).

---

## Inspiration

Directly inspired by **Black Mirror: Bandersnatch** (2018).

Like *Bandersnatch*, it blurs:

* story and choice,
* reality and simulation,
* control and the **illusion** of agency.

**ENTITY** is influenced by Pax but designed as an **AI-powered character** with:

* **Agency** → speaks only when it chooses
* **Personality** → cryptic, restrained, sometimes silent
* **Unpredictability** → mood-driven responses rather than deterministic logic

---

## Research Scope

This repository functions as both **case study and experimental lab**, exploring:

1. **Entity Modeling** — ENTITY as an agent, not a chatbot; **silence as deliberate choice**.
2. **Narrative & Agency** — choice-driven progression; convergence toward **Lucid**, **Fragmented**, or **Dark** states.
3. **Atmosphere & Immersion** — metronarrative rhythm; glitch, silence, and audio layers as narrative devices.
4. **Comparative & Theoretical References** — *Bandersnatch*; Generative Agents (Stanford, 2023); procedural narrative (*PANGeA, arXiv 2404.19721*); symbolic storytelling (*The Dream Within Huang Long Cave, arXiv 2504.04968*).

---

## License

This work is licensed under:
**Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International** (CC BY-NC-ND 4.0)
[Full License Text](https://creativecommons.org/licenses/by-nc-nd/4.0/)

---

## Author

**Michele Grimaldi** — Multidisciplinary Python/C++ developer and independent AI researcher, specializing in **game audio, DSP, and machine learning**.
[GitHub Profile](https://github.com/Mike014)




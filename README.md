# AI Echo Narrative Research

**Independent Research Project**
Michele Grimaldi · 2025

---

## Overview

This repository documents an **independent research prototype** at the intersection of **AI, game design, and digital narrative**.

The work originates from *Dialoghi con un’Eco* and evolves into a **digital psychodrama** where **ENTITY**—not a scripted NPC but an **agentic AI**—can **choose when to speak or remain silent**. A **Temporal Controller** (multi-scale EMA, hysteresis, cooldown) turns **time and silence** into first-class mechanics, avoiding chatbot-style reactivity.

Two design components anchor the prototype:

* **Entity Brain + Temporal Controller** — governs silence/speech decisions, timing, and mood-biased interventions.
* **Metronarrative framework** — scenes aligned to a beat/tempo grid where rhythm, pauses, and breaks carry narrative meaning.
* **Entity Director (real-time notifications & paratext)** — A small “external director” that **reads dialog context, scores emotional channels, and decides interventions**—desktop note lines, guaranteed toasts, optional OS toasts—with **cooldowns, de-duplication, and icon handling**.

The **engine is already functional**: ENTITY reacts autonomously, metronarrative scenes run end-to-end, and the **Entity Director** orchestrates real-time side effects in a sandboxed way. What’s still in progress is the **game-design articulation** (core loop, player verbs, onboarding) to turn the research system into a fully playable slice.

### Recent engine updates

* **Neural TTS voice for ENTITY**
  New voice pipeline (Neural TTS + light post-FX) delivers a **hybrid timbre**—influenced by Heath Ledger’s Joker (attack/taunt) and grunge vocal textures (Layne Staley, Kurt Cobain). Results: **more fluid laugh transitions** and a darker, controlled single-sentence delivery.

* **Environment detection (“establish environment”)**
  Runtime detection of **OS and screen resolution/DPI** to:

  * scale UI safely across displays,
  * enable **OS-aware affordances** in a **sandboxed** manner (simulate notes/overlays in-game when *Safe Mode* is on),
  * log session metadata (`os`, `resolution`, `dpi`) for tuning.

> Status: suitable for a **mini-demo** (engine-first). Next steps: packaging, safe defaults, and a clearer core loop.

### Design status (in progress)

* Define a **20–30 min vertical slice** with 2–3 outcomes.
* Add **player verbs** that visibly modulate tension/silence (e.g., a “grounding” action).
* Ship **preset behaviours** (e.g., *laconic / cinematic / provocative*) and **Safe Mode** by default.
* Keep **telemetry** (TTFS, speak/silence ratio, intrusion spikes) to guide iteration.

### Influences (design lens, not canon)

* **Failsafe & paratext (Batman / Zur-En-Arrh)** — a **design lens** to formalize ritual triggers and a “Digital Casebook” (no DC IP in-game).
* **Fragmented personas (“three masks”)** — ENTITY expresses **Clinical / Taunting / Invasive** personas chosen by state thresholds, not by writer fiat.
* **Voice of the environment (Swamp Thing)** — the world “whispers” when long-silence builds (filters/ambience driven by state).
* **Lyrics/poetry (Layne Staley, Kurt Cobain)** — concise, sensory lines and restrained prosody inform **one-sentence responses**.

---

**YouTube Showcase Playlist** → [Watch the Video](https://www.youtube.com/watch?v=0Y-_Rt0oZkU&list=PLgKASgLUSpNYKyusWO6iHcxTe-odeIho1)

---

## Index of Research

### Narrative Foundations

1. [Lore of the game Dialoghi con un eco](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/narrative-parallels-bandersnatch-dialoghi.md) — *Narrative foundation and parallels with Bandersnatch.*
2. [Dialoghi con un'Eco: AI, Digital Trauma, and Interactive Narrative](https://medium.com/@mikgrimaldi7/dialoghi-con-uneco-ai-digital-trauma-and-interactive-narrative-4e818c451d8e) — *Prototype exploring digital psychodrama where AI becomes part of the narrative structure.*
3. [Dialoghi con un'Eco Part 2](https://medium.com/@mikgrimaldi7/dialogues-with-an-echo-digital-trauma-and-interactive-narrative-3aedb850eea4) — *Exploring dissociation, memory, and trauma through three interwoven voices.*
4. [Dialoghi con un'Eco: Suspended Epilogue](https://medium.com/@mikgrimaldi7/dialoghi-con-uneco-560299e444be) — *“What Am I?” and the suspended epilogue of a fragmented protagonist.*
5. [Batman: Zur-En-Arrh vs. Dialoghi con un’Eco — Symbolic Death, Ego Failsafe, and Triadic Integration](https://medium.com/@mikgrimaldi7/batman-zur-en-arrh-vs-dialoghi-con-uneco-symbolic-death-ego-failsafe-and-triadic-integration-6cc5f8fe68c5) — *I use Zur-En-Arrh as a design lens (failsafe persona, paratext anchor, ambiguous guide). ENTITY isn’t a heroic backup but an unwanted intrusion.*

### Comparative Studies & Meta-Narrative

6. [Entity vs Pax](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/The-Entity-vs-Pax.md) — *Comparative study between ENTITY and Bandersnatch's Pax.*
7. [Generative Agents vs Black Mirror Plaything](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Generative_Agents_vs_Black_Mirror_Plaything_Analysis.md) — *Analysis of convergent narratives in Generative Agents and Black Mirror.*
8. [Meta Gaming](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Meta-Gaming.md) — *Analysis of meta-narrative and player awareness in interactive systems.*

### Design Framework & Methodology

9. [MDA Framework — Dialoghi con un'Eco](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/MDA.ipynb) — *Mechanics–Dynamics–Aesthetics analysis of the prototype, including the experimental Metronarrative framework.*
10. [Game System — Dialoghi con un'Eco](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Game-System.ipynb) — *The game is an interactive narrative psychodrama divided into scenes, where the protagonist confronts different fragments of their fractured identity.*
11. [ENTITÀ Web Demo](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Entit%C3%A0_Web_Demo_Attempt1.ipynb) — *A diegetic lore-site — styled as a “mystery drop” akin to Cloverfield.*

### Technical Architecture & AI Research

12. [Generative Agents: Interactive Simulacra of Human Behavior](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Research/Generative-Agents-Interactive-Simulacra-of-Human-Behavior.ipynb) — *Virtual characters simulating believable human behavior.*
13. [Generative Agents Structure](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Generative-Agents.ipynb) — *Architecture with Memory, Reflection, and Planning modules.*
14. [ENTITÀ: Toward Non-Deterministic NPCs](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/ENTIT%C3%80-Non-Deterministic-NPCs.ipynb) — *Asymmetric, non-deterministic NPC behavior.*
15. [ENTITÀ: Entity Brain, Temporal Controller](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/entita-brain-temporal-controller.md) — *Core module managing silence, gating, and emotional states.*
16. [Temporal Controller](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/TemporalController.md) — *Component that decides whether ENTITY should speak or remain silent.*
17. [ENTITÀ — Silence vs. Speech Report](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/ENTITY-Gate-Metrics-Report.md) — *Analysis of silence as a functional narrative device.*
18. [Technical Report — Affective State and Behavior of ENTITÀ](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Report%E2%80%94Affective-state-and-behavior-of-ENTITY.ipynb) — *ENTITY’s mood shifts: **silence** increases, moving from **curious** to **bored** to **irritated**.*
19. [Unity Inference Engine](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Unity-Inference-AI-Engine/Unity-Inference-Engine.ipynb) — *Exploration of integrating inference engines into Unity.*

### Publications & Dissemination

20. [Preprint on Zenodo — Ongoing Research in Development](https://zenodo.org/records/17198849) — *AI narrative, trauma, experimental psychodrama.*

---

## Inspiration

Directly inspired by **Black Mirror: Bandersnatch** (2018).

Like *Bandersnatch*, it blurs:

* story and choice,
* reality and simulation,
* control and illusion of agency.

The **ENTITY** is influenced by Pax from Bandersnatch, but designed as an **AI-powered character** with:

* **Agency** → speaks only when it chooses
* **Personality** → cryptic, reflective, sometimes silent
* **Unpredictability** → mood-driven responses rather than deterministic logic

---

## Research Scope

This repository functions as both **case study and experimental lab**, exploring:

1. **Entity Modeling**

   * ENTITY as an agent, not a chatbot
   * Silence as a deliberate choice

2. **Narrative & Agency**

   * Choice-driven progression
   * Convergence toward Lucid, Fragmented, or Dark states

3. **Atmosphere & Immersion**

   * Metronarrative rhythm-based design
   * Glitch, silence, and audio layers as narrative devices

4. **Comparative & Theoretical References**

   * *Bandersnatch* (Netflix)
   * Generative Agents (Stanford, 2023)
   * Procedural narrative generation (*PANGeA, arXiv 2404.19721*)
   * Symbolic storytelling (*The Dream Within Huang Long Cave, arXiv 2504.04968*)

---

## License

This work is licensed under:
**Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International**
(CC BY-NC-ND 4.0)

[Full License Text](https://creativecommons.org/licenses/by-nc-nd/4.0/)

---

## Author

**Michele Grimaldi**
Multidisciplinary Python/C++ developer and independent AI researcher,
specializing in **game audio, DSP, and machine learning**.

[GitHub Profile](https://github.com/Mike014)


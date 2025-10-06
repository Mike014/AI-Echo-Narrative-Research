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

* [**Draft of the Premise (notebook)**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Creative_Writing/Draft_of_the_Premise.ipynb)
  *One-line premise and highlighted version; establishes IO–COSCIENZA–ENTITÀ → LUI and the “integrated–hard” outcome.*
* **Anatomy of Story — Working Notes** *(placeholder)*
  *Applying Truby’s premise, 7 steps, and designing principle to keep the story organic and unified.*

---

### 1) Narrative Architecture (Story Space & Influences)

* [**Lore of the game Dialoghi con un eco**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/narrative-parallels-bandersnatch-dialoghi.md)
  *World/lore, tone, rules, and parallels with Bandersnatch.*
* [**Dialoghi con un’Eco: AI, Digital Trauma, and Interactive Narrative**](https://medium.com/@mikgrimaldi7/dialoghi-con-uneco-ai-digital-trauma-and-interactive-narrative-4e818c451d8e)
  *Introduces the triad (IO–COSCIENZA–ENTITÀ), digital psychodrama, diary format.*
* [**Dialogues with an Echo — Part 2**](https://medium.com/@mikgrimaldi7/dialogues-with-an-echo-digital-trauma-and-interactive-narrative-3aedb850eea4)
  *Dissociation, memory, trauma via interwoven voices.*
* [**Dialoghi con un’Eco: Suspended Epilogue**](https://medium.com/@mikgrimaldi7/dialoghi-con-uneco-560299e444be)
  *“What am I?” hinge and non-consolatory ending logic.*
* [**Batman: Zur-En-Arrh vs. Dialoghi con un’Eco — Symbolic Death, Ego Failsafe, and Triadic Integration**](https://medium.com/@mikgrimaldi7/batman-zur-en-arrh-vs-dialoghi-con-uneco-symbolic-death-ego-failsafe-and-triadic-integration-6cc5f8fe68c5)
  *LEI as trigger; ENTITÀ as intrusive failsafe; COSCIENZA as containment.*
* [**Entity vs Pax**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/The-Entity-vs-Pax.md)
  *Compares ENTITÀ to Bandersnatch’s Pax (antagonism, agency, meta control).*
* [**Generative Agents vs Black Mirror Plaything**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Generative_Agents_vs_Black_Mirror_Plaything_Analysis.md)
  *Convergences between simulated minds and authored meta-narratives.*
* [**Meta Gaming**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Meta-Gaming.md)
  *Player awareness, authorial intrusion, diegetic meta signals.*

---

### 2) Game Design Framework

* [**MDA + CCC Framework — Dialoghi con un’Eco**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/MDA.ipynb)
  *Reading IO's diary accidentally activates ENTITY inside the system.*
* [**Meta Gaming (design lens)**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Meta-Gaming.md)
  *Rules for fourth-wall nudges, diegetic UI, narrative reliability.*

---

### 3) Engine & AI Architecture

* [**ENTITÀ: Entity Brain & Temporal Controller**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/entita-brain-temporal-controller.md)
  *Core control loop: silence/speech gating, affect, pressure curves.*
* [**Temporal Controller (spec)**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/TemporalController.md)
  *Policy for speak/wait/withhold—primary pacing lever.*
* [**ENTITÀ — Toward Non-Deterministic NPCs**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/ENTIT%C3%80-Non-Deterministic-NPCs.ipynb)
  *Asymmetric, stochastic behaviors: legible yet unpredictable.*
* [**Unity Inference Engine (exploration)**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Unity-Inference-AI-Engine/Unity-Inference-Engine.ipynb)
  *Prototype path for realtime integration.*
* [**ENTITÀ Web Demo (diegetic site)**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Entit%C3%A0_Web_Demo_Attempt1.ipynb)
  *In-world web surface; mystery-drop pacing and indirect exposition.*

---

### 4) Metrics & Evaluation

* [**Gate Metrics — Silence/Speech**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/ENTITY-Gate-Metrics-Report.md)
  *Quantifies speaking vs silence; links gating to tension and comprehension.*
* [**Affective Trajectories**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Report%E2%80%94Affective-state-and-behavior-of-ENTITY.ipynb)
  *Measures mood shifts and their downstream effects; informs controller tuning.*

---

### 5) Research Corpus (Background & Theory)

* [**Generative Agents: Interactive Simulacra of Human Behavior**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Research/Generative-Agents-Interactive-Simulacra-of-Human-Behavior.ipynb)
  *Reference for Memory / Reflection / Planning in simulated agents.*
* [**Generative Agents — Structure (notes)**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Generative-Agents.ipynb)
  *Working notes mapping GA modules to ENTITÀ’s architecture.*

---

### 6) Publications & Dissemination

* [**Preprint (Zenodo) — Ongoing Research in Development**](https://zenodo.org/records/17198849)
  *Living preprint: narrative design, AI control strategies, psychodrama framing.*

---

### 7) Safety, Ethics & Content Guidelines

* **Intent & Framing**
  *Portray loneliness, intrusive thoughts, and self-destructive ideation **without glamorization**; emphasize consequences and limits.*
* **Diegetic Safeguards**
  *Within the story, COSCIENZA enforces **boundaries, pauses, escalation limits**; ENTITÀ’s pressure is contextualized, not celebrated.*
* **Alternatives & Agency**
  *Show **de-escalation choices** (contact, delay, routine) even if the protagonist refuses them; keep agency visible.*
* **Language**
  *Avoid sensational detail; use **clear, clinical phrasing** for harm-related content.*
* **Signals & Warnings**
  *Provide **content notes** and opt-outs for sensitive sequences.*
* **Resources (Credits/Appendix)**
  *Link to **support resources** and hotlines relevant to your audience.*
* **Testing & Review**
  *Use sensitivity readers / trusted peers to catch unintended glamorization or harm.*
* **Documentation**
  *Keep an ethics changelog: why a scene exists, what function it serves, what safeguards are in place.*

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

## ⚖️ License

This work is licensed under the
**Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)**

You are free to:

* **Share** — copy and redistribute the material in any medium or format

Under the following terms:

* **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made.
* **NonCommercial** — You may not use the material for commercial purposes.
* **NoDerivatives** — If you remix, transform, or build upon the material, you may not distribute the modified material.
* **No additional restrictions** — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

📄 Full license text: [https://creativecommons.org/licenses/by-nc-nd/4.0/](https://creativecommons.org/licenses/by-nc-nd/4.0/)

## Project Status & Collaboration
**Status:** Personal/authorial project.  
**Collaboration:** Not seeking collaborators. **No pull requests** will be accepted.  
**Feedback:** Issues for feedback are welcome; unsolicited PRs will be closed.

## License Summary
**Creative assets** (texts/poetry, narrative materials, audio, images):  
Licensed under **CC BY-NC-ND 4.0** — no commercial use, no derivatives.  

**Source code** (engine, scripts, tools, configs):  
**Copyright © 2025 Michele Grimaldi. All Rights Reserved.**  
Unless you have my prior **written** permission, you may **not** modify, fork outside GitHub for PR purposes, redistribute, publish binaries, sublicense, or create derivative works.

## Allowed
- View the repository and **run locally** for personal, non-commercial evaluation.
- Share an **unmodified** link to this repository with proper credit.

## Not Allowed (without written permission)
- **No derivatives:** no modified forks, ports, patches, repackaging, or spin-offs.
- **No redistribution:** no binaries/installers, mirrors, or re-uploads anywhere.
- **No commercial use** of any kind.
- **No public hosting/demos** for others to access.
- **No ML/AI usage:** do not use the code or assets for dataset creation, embeddings, 
  training, fine-tuning, or evaluation of models.

## Enforcement
Unauthorized derivative works, redistribution, or misuse may result in **DMCA takedowns**
and **legal action**. Derivative releases are **not permitted** and may expose you to liability.
For any exception, **ask first** at: <mikgrimaldi7@gmail.com> — permissions must be **in writing**.

## **COMMERCIAL LICENSING INQUIRIES**:
For game studios, researchers, or commercial entities interested 
in licensing this technology, contact: <mikgrimaldi7@gmail.com> 

*The game is currently in testing and is only available in **Italian**, but an English translation is planned for the future.*

© 2025 Michele Grimaldi






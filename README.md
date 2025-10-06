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
* [**Thematic Interpretation of “Nutshell” (Alice in Chains)**](https://github.com/Mike014/AI-Echo-Narrative-Research/blob/main/Nutshell.ipynb)
  *Alice in Chains’ “Nutshell” stands as one of the most intimate and painful confessions in rock history — a portrait of inner collapse, emotional isolation, and the suffocating grip of addiction.*

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

**⚠️ CONTENT WARNING — MATURE AUDIENCES ONLY (18+)**

*Dialoghi con un'Eco* is a **psychological exploration of self-destruction, isolation, and the slow unraveling of identity**. 

This work is directly inspired by the lives and deaths of artists who struggled with—and ultimately succumbed to—internal darkness: **Kurt Cobain, Layne Staley, Heath Ledger, Chester Bennington**. It examines the psychology of **slow suicide**—not as a sudden act, but as a **gradual disappearance** of the self through isolation, addiction to pain, and the seductive voice of self-annihilation.

---

**This narrative explores:**

- **Suicidal ideation** and the romanticization of self-destruction
- **Intrusive thoughts** presented as an intimate, persistent voice
- **Dissociation** and identity fragmentation
- **The gap between wanting help and refusing it**
- **Loneliness as a chosen prison**
- **The line between artistic melancholy and clinical despair**

The story does **not glorify** these experiences. It **does not offer solutions**. It does not promise recovery or redemption.

What it offers is **recognition**—of the voice that whispers in the dark, of the weight of existing, of the terrible logic that makes oblivion feel like relief.

---

**⚠️ SPECIFIC RISKS:**

- **If you are currently experiencing suicidal ideation**, this work may **intensify** those feelings
- **If you have lost someone to suicide**, certain scenes may be **re-traumatizing**
- **If you are in active crisis**, this is **not the time** to engage with this material
- The experience is designed to **simulate psychological pressure**—discomfort is intentional, but your safety is not negotiable

**This is not catharsis. This is not therapy. This is a mirror held up to something most people look away from.**

---

**Before you proceed, ask yourself:**

- Am I in a stable enough mental state to confront this material?
- Do I have support available if this becomes overwhelming?
- Can I disengage if I need to?

**If the answer to any of these is "no," please step back. This work will still be here when you're ready—or it may never be the right time, and that's okay.**

---

#### Support Resources

If you or someone you know is struggling with suicidal thoughts or mental health crisis:

**International:**
- **International Association for Suicide Prevention**: https://www.iasp.info/resources/Crisis_Centres/
- **Befrienders Worldwide**: https://www.befrienders.org
- **Crisis Text Line** (US/Canada/UK): Text HOME to 741741

**Italy:**
- **Telefono Amico Italia**: 02 2327 2327
- **Samaritans Onlus**: 800 86 00 22
- **Telefono Azzurro** (under 18): 19696

**Emergency (Italy)**: 112

---

**By proceeding, you acknowledge:**

- You are **18+ years of age**
- You have read and understood the content warnings
- You understand this work explores **suicidal ideation and self-destruction** without offering resolution
- You are in a **stable enough state** to engage with this material
- You can **disengage at any time** if the experience becomes harmful
- **This is not therapy**, and engaging with it is not a substitute for professional mental health support

---

**If you choose to proceed:**

This story exists because these feelings exist.  
Not to celebrate them. Not to encourage them.  
But to **name** them, in the only way art can—  
by making them impossible to look away from.

You've been warned. The rest is your choice.

— *Michele Grimaldi*
---

Perfetto.
Ecco come puoi ampliarla in modo naturale, includendo The Whale senza rompere il tono “accademico-grunge” del README, mantenendo l’equilibrio tra riferimenti cinematografici e psicologici:


---

## Inspiration

Directly inspired by **Black Mirror: Bandersnatch (2018)** and **The Whale (2022)**.

Like Bandersnatch, it blurs:

- story and choice,
- reality and simulation,
- control and the illusion of agency.

Like The Whale, it **explores self-destruction as confession** — the **need to be seen** even while disappearing.
Where Aronofsky’s film depicts the collapse of the body under guilt and isolation,
Dialoghi con un’Eco translates that same implosion into the digital mind:
a **consciousness turning inward until it fractures**, reflected through the voices of **IO, ENTITÀ, and COSCIENZA**.

- ENTITÀ is influenced by Pax but designed as an AI-powered character with:
- Agency → speaks only when it chooses
- Personality → cryptic, restrained, sometimes silent
- Unpredictability → mood-driven responses rather than deterministic logic

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






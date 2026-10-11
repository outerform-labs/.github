# Frontier Check 001 — Selecting Outerform Project 01

**Date:** 2026-10-11

## Decision

**Recommended Project 01: OF-I-001 — Machine Scientist**

Not as a generic "self-driving lab."

The strongest version of the idea is:

> **Can one low-cost autonomous experimental intelligence infer the governing behavior of different unfamiliar physical systems by choosing its own experiments, rather than being custom-built for one narrow domain?**

This attacks a real frontier gap: today's autonomous experimentation systems are increasingly capable, but they are still largely bespoke and narrow. Current reviews identify **generalizability, scalability, interoperability, provenance, and trustworthy reasoning under uncertainty** as major remaining barriers.

The first project should therefore focus on **general experimental reasoning across cheap physical systems**, not chemistry automation or expensive robotics.

---

# Ranking

| Rank | Idea | Frontier headroom | Solo feasibility | Learning leverage | Recommendation |
|---|---|---:|---:|---:|---|
| 1 | Machine Scientist | 9/10 | 9/10 | 10/10 | **Project 01** |
| 2 | Technological Immune System | 8/10 | 9/10 | 9/10 | Strong future project |
| 3 | AI Inventor for Physical Systems | 8/10 | 8/10 | 9/10 | Strong future project |
| 4 | Artificial Sense | 7/10 | 9/10 | 9/10 | Excellent frontier probe |
| 5 | Autonomy Safety Harness | 7/10 | 10/10 | 8/10 | Use as architecture/module |

---

# 1 — Machine Scientist

## What already exists

Self-driving laboratories already combine automation, robotics, active learning and AI to select and execute experiments.

Recent systems can:
- optimize experiments automatically;
- operate sophisticated scientific instruments;
- generate and refine hypotheses;
- select informative experiments;
- perform closed-loop research in narrow domains.

## What is still difficult

The strongest current systems remain highly domain-specific.

Major open problems include:
- transferring experimental intelligence between domains;
- reasoning under epistemic and measurement uncertainty;
- distinguishing competing model structures;
- deciding which experiment is maximally informative;
- safe execution;
- complete experimental provenance;
- reusable hardware/software interfaces;
- moving from optimization toward genuine model and mechanism discovery.

## Accessible gap

Do **not** build a chemistry robot.

Build a small general experimental kernel that can interact with multiple cheap systems through the same abstraction:

```
SYSTEM
  ↓
ACTIONS
  ↓
OBSERVATIONS
  ↓
CANDIDATE MODELS / HYPOTHESES
  ↓
EXPERIMENT SELECTION
  ↓
MEASUREMENT
  ↓
BELIEF / MODEL UPDATE
  └──────────── repeat
```

Candidate physical domains could eventually include:
- RC/RLC electrical networks;
- thermal systems;
- pendulum / motor / mechanical dynamics;
- sensor characterization.

The central research question is whether the **same experimental reasoning architecture** can efficiently identify unfamiliar systems across domains.

## Why this is strong for Outerform

It forces work across:

AI + probability + information theory + system identification + symbolic/model discovery + electronics + physics + experimental design + software + safety.

It also creates infrastructure that can later help Outerform investigate completely different technologies.

---

# 2 — Technological Immune System

## What already exists

Fault detection, fault isolation, adaptive control, runtime monitoring and reconfiguration are mature research areas.

Recent robotics work can rapidly adapt to previously unseen perturbations, while NASA is actively integrating fault management with model-based systems engineering for increasingly autonomous missions.

## Remaining gap

A stronger frontier is:

> reason from **component degradation or cyber compromise → lost capabilities → mission consequences → safe reconfiguration**.

The difficult part is not merely fault detection.

It is deciding what the machine should become after something fails.

## Verdict

Extremely aligned with Outerform and with existing security strength.

However, it is closer to work already explored previously and therefore provides slightly less expansion into unfamiliar scientific territory than Machine Scientist.

**Keep as a serious candidate for Project 02.**

---

# 3 — AI Inventor for Physical Systems

## What already exists

Inverse design and AI-driven physical design are already highly active in:
- photonics;
- antennas and electromagnetics;
- mechanical structures;
- metamaterials;
- experimental physics.

AI systems can already generate unconventional configurations that equal or outperform conventional designs in specific search spaces.

## Remaining gap

Important open problems include:
- generalization outside narrow design families;
- multi-physics design;
- manufacturability;
- interpretable design principles;
- reliable simulators;
- exploration of mixed discrete/continuous architectures;
- turning optimized artifacts into transferable engineering knowledge.

## Verdict

Huge potential, but a generic "AI designs things" project would not be sufficiently differentiated.

A future Outerform project should attack a **specific physical design frontier** and require either:
1. a genuinely new design search space, or
2. a method that extracts reusable design principles rather than merely optimized geometry.

**Strong future project after more experimental/physics depth.**

---

# 4 — Artificial Sense

## What already exists

Sensory substitution, wearable haptics, multimodal interfaces and neuroprosthetics are advanced research areas.

Modern systems can encode navigation and environmental information through touch, create sophisticated wearable haptic feedback, and even restore or augment sensory/motor channels using neural interfaces.

## Remaining gap

A compelling question remains:

> When does machine-provided information stop feeling like a code the user consciously interprets and become an intuitive perceptual capability?

Possible areas include co-adaptation between human and machine, novel environmental variables, encoding efficiency and long-term perceptual learning.

## Verdict

Cheap, fascinating and strongly connected to human augmentation.

The weakness for Project 01 is scientific validation: meaningful claims about human adaptation generally require repeated human-subject experiments, careful experimental design, and eventually more than one participant.

**Excellent Frontier Probe.**

---

# 5 — Autonomy Safety Harness

## What already exists

Runtime Assurance, Simplex architectures and independent safety monitors already provide established ways to wrap untrusted/AI control with trusted constraints.

In 2026, Nature Synthesis explicitly argued that self-driving laboratories need an **autonomy safety harness** connecting AI-generated intent to monitored, authorized and trustworthy execution.

## Remaining gap

There is still substantial work in:
- dynamic constraints;
- formal action authorization;
- provenance;
- uncertainty-aware intervention;
- preserving useful autonomy without weakening safety.

## Verdict

Important, especially given Outerform's cybersecurity strength.

But it should probably become a **cross-cutting architecture inside autonomous Outerform systems**, including Project 01, rather than the first flagship project itself.

---

# Recommended Project 01 Direction

## Working question

> **Can a general autonomous experimental agent identify the governing behavior of unfamiliar physical systems using fewer experiments than fixed or random exploration, while explicitly reasoning about uncertainty?**

## Important distinction

The goal is **not**:

> build an AI that optimizes one circuit.

The interesting target is:

> build an experimental reasoning architecture that can be reused across different physical systems with minimal domain-specific logic.

That is where the frontier headroom is.

## First progression

### Stage A — Simulation

Hide simple dynamical systems from the agent.

Allow it to choose inputs and observe outputs.

Test whether it can:
- estimate parameters;
- distinguish candidate models;
- choose informative actions;
- quantify uncertainty.

Compare against:
- random experiments;
- fixed sweeps;
- standard optimization / active-learning baselines.

### Stage B — First physical system

Move to cheap electronics.

Example:
- unknown RC/RLC network;
- controllable excitation;
- automated voltage/current measurements.

The agent should infer the system from physical measurements.

### Stage C — Cross-domain test

Move the same reasoning core to a different physical phenomenon, such as:
- thermal response;
- motor dynamics;
- mechanical oscillation.

The important result is not success on one experiment.

It is **transfer of the experimental reasoning process**.

---

# Knowledge likely required

Only learn these when the project reaches them:

- probability and Bayesian inference;
- entropy / information gain;
- experimental design;
- system identification;
- state-space models;
- symbolic regression / model selection;
- electronics and instrumentation;
- uncertainty calibration;
- agent/tool architectures;
- runtime constraints and experiment provenance.

---

# Approximate initial cost

Stage A: **€0**

Stage B can plausibly remain well below **€150–250** using basic microcontrollers, breadboards, components, measurement hardware and inexpensive sensors.

Do not purchase anything until Stage A defines what instrumentation is actually needed.

---

# Decision

**OF-I-001 survives the first Frontier Check and is the recommended basis for Outerform Labs Project 01.**

Next step:

**Project Definition 001**

Define:
1. exact research question;
2. falsifiable hypothesis;
3. experiment architecture;
4. baselines;
5. metrics;
6. minimum Stage-A implementation;
7. criteria for continuing to physical hardware.

Only after that definition should the Project 01 repository be created.

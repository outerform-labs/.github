# Outerform Labs — Idea Vault

> Build what should not exist yet.

This file contains questions and candidate capabilities, not commitments.

## Selection rule

A strong Outerform project should satisfy most of these:

- **Impact:** success could unlock an important capability.
- **Unknown:** there is a real technical or scientific uncertainty to attack.
- **Experimentability:** one person can test a meaningful piece with available resources.
- **Depth:** the project forces real scientific or engineering reasoning.
- **Learning leverage:** pursuing it makes future projects more ambitious.
- **Curiosity:** I genuinely want to know the answer.

Projects are selected only after a state-of-the-art / frontier check.

---

# Current Shortlist — Frontier Check Next

## OF-I-001 — Machine Scientist

**Capability:** A machine can investigate an unfamiliar physical system by choosing experiments, measuring outcomes, constructing models, and deciding what to test next.

**Central unknown:** Can a low-cost, reasonably general system choose informative physical experiments rather than merely optimize a known process?

**First test:** Give software control of a simple unknown electrical or mechanical system and compare autonomous experiment selection against random or fixed sampling.

**Status:** INVESTIGATING

---

## OF-I-002 — Autonomy Safety Harness

**Capability:** AI can control physical or cyber-physical systems while an independent layer constrains, checks, records, and rejects unsafe or unauthorized actions.

**Central unknown:** Can we preserve useful open-ended agent autonomy without relying on the agent itself to obey critical invariants?

**First test:** Let an AI agent control a simulated physical process through a constrained action gateway; inject tempting unsafe actions and measure whether the system preserves invariants without destroying task performance.

**Status:** INVESTIGATING

---

## OF-I-003 — Technological Immune System

**Capability:** An autonomous machine can detect degradation or compromise, understand its mission consequences, and reorganize itself to continue safely.

**Central unknown:** Can recovery be selected from mission-level reasoning instead of predefined fault-response tables?

**First test:** Create a small simulated robot/spacecraft with redundant capabilities, inject faults, and compare fixed recovery against mission-aware adaptive recovery.

**Status:** INVESTIGATING

---

## OF-I-004 — Artificial Sense

**Capability:** A human gains an intuitive perception of a quantity biology does not naturally expose, through continuous machine sensing and sensory substitution.

**Central unknown:** Can a novel sensor-to-human encoding become intuitive enough to improve behavior without conscious interpretation of numerical measurements?

**First test:** Map magnetic, distance, orientation, or another safe environmental signal to haptic/audio feedback and measure learning across repeated tasks.

**Status:** INVESTIGATING

---

## OF-I-005 — AI Inventor for Physical Systems

**Capability:** AI searches large physical design spaces and produces useful configurations that are non-obvious to human designers.

**Central unknown:** Under what representations and constraints does AI generate genuinely useful unconventional physical designs rather than superficial optimization?

**First test:** Choose a simulator-friendly system such as an antenna geometry, mechanism, optical layout, controller, or sensor arrangement and compare AI-generated designs with standard baselines.

**Status:** INVESTIGATING

---

# Raw Idea Pool

## OF-I-006 — Self-Modeling Robot

**Capability:** A robot learns an internal model of its own body from interaction and detects when its physical dynamics have changed.

**Key unknown:** Can useful self-models emerge without being given an accurate mechanical model?

**First test:** Learn the dynamics of a simulated or low-cost actuator system, secretly alter mass/friction/actuator response, and test detection and adaptation.

**Status:** RAW

---

## OF-I-007 — Embodied Intelligence Under Communication Loss

**Capability:** A robot continues meaningful exploration when remote instruction becomes impossible.

**Key unknown:** What minimum world-model and planning capabilities are necessary for useful long-horizon autonomy in unfamiliar terrain?

**First test:** Simulate a rover with intermittent communications and compare scripted autonomy with adaptive local planning.

**Status:** RAW

---

## OF-I-008 — Emergent Machine Communication

**Capability:** Multiple machines invent a compact communication protocol suited to their task and environment instead of receiving a human-designed protocol.

**Key unknown:** Do emergent protocols remain robust, interpretable, and transferable when channel conditions change?

**First test:** Cooperative agents solve a task through a deliberately constrained/noisy channel and must learn their own message representation.

**Status:** RAW

---

## OF-I-009 — Adaptive Digital Twin

**Capability:** A digital twin recognizes when its own model has stopped matching reality and autonomously repairs or replaces the model.

**Key unknown:** Can a twin distinguish sensor error, parameter drift, structural change, and model inadequacy from observations alone?

**First test:** Couple a simulated twin to a physical or simulated plant whose dynamics change unexpectedly.

**Status:** RAW

---

## OF-I-010 — Universal Scientific Instrument Agent

**Capability:** An AI learns to operate unfamiliar instruments from documentation, feedback, and safe experimentation.

**Key unknown:** Can an agent acquire reliable operational competence without a custom integration for every instrument?

**First test:** Expose an agent to a simulated instrument with documentation and an action API it has never seen.

**Status:** RAW

---

## OF-I-011 — Autonomous Diagnostic Experimentation

**Capability:** When uncertain about a machine failure, an autonomous system actively performs the most informative safe diagnostic action.

**Key unknown:** Can information-seeking actions materially improve diagnosis under limited time and resources?

**First test:** Give a simulated machine several indistinguishable failure hypotheses and compare active diagnosis against passive monitoring.

**Status:** RAW

---

## OF-I-012 — Machine-Generated Scientific Instruments

**Capability:** AI designs not only experiments but also the sensing/instrument configuration needed to extract the most useful information.

**Key unknown:** Can an optimizer invent measurement layouts that outperform intuitive human arrangements under cost constraints?

**First test:** Optimize placement/type of virtual sensors for identifying an unknown dynamical system.

**Status:** RAW

---

## OF-I-013 — Cognitive Exocortex

**Capability:** A persistent AI system becomes an extension of a person's memory and reasoning rather than a separate chatbot consulted manually.

**Key unknown:** What interaction loop genuinely improves human reasoning instead of merely outsourcing it?

**First test:** Build one narrow closed-loop memory/reasoning function and measure decision quality or recall over several weeks.

**Status:** RAW

---

## OF-I-014 — Learnable Artificial Spatial Perception

**Capability:** A person learns a nonvisual representation of nearby geometry and can navigate using it.

**Key unknown:** Which encoding lets spatial information become intuitive with the least training?

**First test:** Distance sensors or simulated spatial data mapped to haptic/audio patterns in a controlled navigation task.

**Status:** RAW

---

## OF-I-015 — Perceptual Compression for Synthetic Reality

**Capability:** Artificial environments create convincing presence while rendering/stimulating only the information the brain actually needs.

**Key unknown:** Which sensory cues dominate perceived physical presence, and which can be omitted?

**First test:** Manipulate latency, spatial audio, visual/parallax, or haptic cues independently and quantify perceived presence.

**Status:** RAW

---

## OF-I-016 — Adaptive Human–Machine Co-Learning

**Capability:** A machine interface changes its encoding while the human learns it, so both sides jointly converge on a better communication scheme.

**Key unknown:** Is co-adaptation faster or more expressive than holding the interface fixed?

**First test:** Human controls a simple virtual system through an unfamiliar mapping while the mapping itself adapts to performance.

**Status:** RAW

---

## OF-I-017 — Passive Radio Perception

**Capability:** A machine extracts useful environmental state from ordinary radio propagation without relying on conventional cameras.

**Key unknown:** How much robust physical information can be recovered from cheap RF measurements outside carefully controlled laboratories?

**First test:** Collect benign occupancy/motion data from a controlled room and test whether RF channel variations provide reliable state information.

**Status:** RAW

---

## OF-I-018 — Neuromorphic Wearable Intelligence

**Capability:** A wearable processes continuous sensory streams with extremely low power using event-driven / brain-inspired computation.

**Key unknown:** Where does neuromorphic processing provide a real system-level advantage over conventional low-power inference?

**First test:** Compare event-driven and conventional processing on a small continuous sensing task using public data or affordable hardware.

**Status:** RAW

---

## OF-I-019 — Self-Sensing Structures

**Capability:** A structure continuously infers its own mechanical condition and localizes changes or damage from sparse embedded sensing.

**Key unknown:** How little sensing is sufficient for useful structural self-awareness?

**First test:** Instrument a simple beam or 3D-printed structure with cheap sensors and infer changes in load, stiffness, or geometry.

**Status:** RAW

---

## OF-I-020 — Reconfigurable Machine Architecture

**Capability:** A machine changes its functional architecture when goals, damage, or environmental conditions change.

**Key unknown:** Can reconfiguration decisions be generated dynamically rather than selected from predesigned modes?

**First test:** Build a simulated modular system whose sensors, compute nodes, and control paths can be recombined under failures or changing goals.

**Status:** RAW

---

## OF-I-021 — Cooperative Autonomous Construction

**Capability:** Multiple simple robots coordinate to build useful structures without centralized micromanagement.

**Key unknown:** How much global structure can emerge from local sensing, local rules, and limited communication?

**First test:** Simulate small agents assembling modular blocks under communication and localization constraints.

**Status:** RAW

---

## OF-I-022 — Autonomous Infrastructure Maintenance

**Capability:** Robots inspect infrastructure, decide what degradation matters, plan interventions, and verify that the intervention worked.

**Key unknown:** Can inspection and repair planning be closed into one autonomous reasoning loop?

**First test:** Simulated inspection environment with multiple defects, limited energy, and repair actions.

**Status:** RAW

---

## OF-I-023 — Physical Reservoir Computer

**Capability:** Exploit the natural dynamics of a cheap physical system as computation instead of simulating everything digitally.

**Key unknown:** Can a simple analog/mechanical/electronic substrate perform a useful inference task with less computational overhead?

**First test:** Build or simulate a small nonlinear dynamical circuit and train only its readout layer on a temporal task.

**Status:** RAW

---

## OF-I-024 — AI-Designed Biosensor (In Silico)

**Capability:** AI proposes sensing architectures that translate a safe target molecule or environmental signal into an easily measurable output.

**Key unknown:** Can computational design meaningfully narrow the experimental search space for programmable sensing?

**First test:** Restrict the work to safe public biological datasets/models and benchmark computationally proposed sensor components against known examples.

**Status:** RAW

---

## OF-I-025 — Smart Energy Storage Diagnosis

**Capability:** An energy-storage system infers hidden degradation from minimal measurements and actively chooses diagnostic tests.

**Key unknown:** How early can useful internal-state information be inferred without expensive instrumentation or full lifetime testing?

**First test:** Use open battery datasets to compare passive prediction with active selection of informative measurements.

**Status:** RAW

---

## OF-I-026 — Autonomous Swarm Repair

**Capability:** A group of robots collectively recognizes that one unit or structure is damaged and redistributes tasks to restore overall capability.

**Key unknown:** Can mission functionality be recovered without a centralized complete model of every failure?

**First test:** Multi-agent simulation with random unit failures and dynamically reassigned roles.

**Status:** RAW

---

## OF-I-027 — Constraint-Aware AI Engineering

**Capability:** An AI engineer reasons simultaneously about performance, physics, safety, cost, manufacturability, and uncertainty while generating designs.

**Key unknown:** Can explicit multi-domain constraints produce designs that survive contact with reality better than unconstrained generative approaches?

**First test:** Choose one small engineering design problem with a reliable simulator and compare constrained versus unconstrained design agents.

**Status:** RAW

---

## OF-I-028 — Autonomous Model Discovery

**Capability:** A system derives compact mathematical laws from observations and deliberately seeks data that distinguish competing explanations.

**Key unknown:** Can symbolic/model discovery remain reliable when measurements are noisy and several models explain existing observations?

**First test:** Hide a known dynamical law behind noisy simulated/physical measurements and evaluate active model discrimination.

**Status:** RAW

---

## OF-I-029 — Human–AI Shared Control

**Capability:** Human intent and machine autonomy dynamically share control rather than forcing either manual control or full automation.

**Key unknown:** Can authority transfer adapt to uncertainty and competence without confusing or fighting the human operator?

**First test:** A simulated vehicle/robot task with variable AI confidence and measurable human intervention.

**Status:** RAW

---

# Next Step

Perform a **Frontier Check** on OF-I-001 through OF-I-005:

1. What is the current state of the art?
2. What has already been solved?
3. What remains genuinely difficult?
4. Why does the limitation remain?
5. What meaningful subproblem is accessible with €0–500?
6. What would be novel enough to justify a project?
7. What knowledge and equipment would the first experiment require?

Only after that check will one idea become **Outerform Project 01**.

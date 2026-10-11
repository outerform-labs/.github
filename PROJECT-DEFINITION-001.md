# Project Definition 001 — Machine Scientist

**Outerform Labs**  
**Status:** Selected for Stage A validation  
**Date:** 2026-10-11

---

# 1. Vision

Build toward a machine that can investigate an unfamiliar physical system by:

1. deciding what experiment to perform;
2. applying an input or intervention;
3. observing the result;
4. updating its beliefs about the system;
5. deciding what to test next;
6. eventually producing a useful model of how the system behaves.

The long-term ambition is a reusable experimental intelligence rather than a laboratory automation script tied to one instrument or scientific domain.

This project does **not** begin by attempting to build a general autonomous scientist.

It begins by testing one concrete claim.

---

# 2. Exact Stage-A Research Question

> **Can one common sequential experimental-reasoning loop identify structurally different unknown dynamical systems more sample-efficiently than non-adaptive experimentation, while explicitly representing uncertainty?**

The same reasoning core should operate through a standardized interface rather than contain a separate hand-written experiment strategy for every benchmark.

---

# 3. What Is and Is Not New

Active experiment design, Bayesian experimental design, active learning, and adaptive system identification already exist.

Therefore this project must **not** claim novelty merely because the system chooses its next experiment.

The potential research direction is instead:

> **generality of the experimental-reasoning layer across different classes of physical systems with minimal domain-specific decision logic.**

Stage A is a validation platform, not yet a claim of original scientific contribution.

Only later experiments can determine whether there is genuine novelty.

---

# 4. Falsifiable Hypothesis

## H1

A shared sequential experiment-selection architecture can reach a predefined identification target using **at least 30% fewer experimental samples on median** than both:

- random valid excitation; and
- a fixed preplanned sweep,

on **at least two structurally different benchmark system families**, without materially degrading final model accuracy.

## H0

The shared adaptive architecture does not produce a meaningful sample-efficiency advantage, or only succeeds after substantial domain-specific customization.

If H0 is supported, the proposed general experimental-reasoning architecture is not yet justified.

---

# 5. Stage-A Scope

Stage A is **simulation only**.

No hardware.

No LLM required.

No robotics.

No graphical interface.

No attempt to generate scientific papers automatically.

The purpose is to test the decision loop itself as cheaply and cleanly as possible.

---

# 6. Experimental Abstraction

Every experimental environment must expose the same minimal contract:

```
reset()
available_actions()
apply(action) -> observation
observation_history()
action_history()
constraints()
```

The reasoning layer should see:

```
Prior / current beliefs
        ↓
Candidate experiment actions
        ↓
Estimate expected usefulness
        ↓
Choose action
        ↓
Environment executes experiment
        ↓
Noisy observation
        ↓
Update model / posterior
        ↓
Evaluate stopping criterion
        └────────────── repeat
```

The environment knows the true hidden system.

The experimental agent does not.

---

# 7. Initial Benchmark Families

Do not start with ten systems.

Use two first, then add a third only after the loop works.

## Benchmark A — First-order system

A simple first-order dynamical system analogous to an RC or thermal process.

Example form:

```
dx/dt = -a x + b u
y = x + noise
```

Unknown parameters may include:

- time constant;
- gain;
- observation noise.

Purpose:

- debug the complete loop;
- establish metrics;
- verify posterior/model updates.

---

## Benchmark B — Second-order oscillatory system

A damped second-order system analogous to an RLC circuit or mass-spring-damper.

Example form:

```
d²x/dt² + 2ζωₙ dx/dt + ωₙ²x = k u
```

Unknown parameters may include:

- natural frequency;
- damping ratio;
- gain.

Purpose:

- test whether the same reasoning core handles qualitatively different dynamics;
- require more informative excitation choices.

---

## Benchmark C — Nonlinear system [conditional]

Add only after A and B work.

Potential choices:

- nonlinear pendulum;
- saturating actuator;
- nonlinear thermal model.

Purpose:

- test whether the architecture survives departure from linear models.

This benchmark is **not required for the first go/no-go decision**.

---

# 8. Experimental Strategies

At minimum compare three strategies.

## Baseline 1 — Random

Select a valid experiment/input randomly from the same allowed action space.

Purpose:

establish the simplest exploration baseline.

---

## Baseline 2 — Fixed Design

Use the same predetermined experiment sequence for every run.

Examples:

- amplitude sweep;
- frequency sweep;
- predefined pulse sequence.

Purpose:

represent ordinary non-adaptive experimentation.

---

## Candidate — Adaptive Information-Seeking Strategy

Select the next experiment based on current uncertainty.

Initial implementation should use a principled method such as:

- expected information gain;
- expected entropy reduction;
- posterior variance reduction;
- another well-defined Bayesian experimental-design utility.

Do not use an LLM to decide experiments in Stage A.

The decision process must initially be measurable and reproducible.

---

# 9. State of Knowledge

For the first version, the agent may know:

- the admissible action space;
- measurement constraints;
- candidate model family;
- prior ranges over unknown parameters.

It must **not** know:

- true parameter values;
- hidden system instance;
- future observations.

Later versions can relax the assumption that the correct model family is known.

That is a substantially harder problem and should not be mixed into the first experiment.

---

# 10. Metrics

The primary metric is:

## Samples to target

Number of experimental measurements required before the inferred model reaches the target identification quality.

Secondary metrics:

### Parameter error

Normalized error between inferred and true parameters.

### Predictive error

Model error on a held-out excitation trajectory not seen during identification.

### Uncertainty calibration

Whether reported uncertainty is consistent with actual estimation error.

### Success rate

Fraction of runs that reach the target before exhausting the experiment budget.

### Experimental cost

Optional weighted cost if different actions later have different energy/time/risk costs.

### Compute time

Recorded but not optimized in the first version.

---

# 11. Initial Success Criterion

Across at least **100 randomized hidden-system instances per benchmark family**:

The adaptive strategy should:

1. achieve the identification target in at least 90% of runs;
2. require at least **30% fewer median samples** than random exploration;
3. require at least **30% fewer median samples** than the fixed design on at least two benchmark families;
4. achieve held-out predictive accuracy no worse than the best baseline by more than a predefined tolerance;
5. produce uncertainty estimates that are not obviously overconfident.

The exact numerical prediction-error threshold must be fixed before running the final benchmark suite.

Do not change it after observing the results.

---

# 12. Failure / Kill Criteria

Stage A fails if, after reasonable implementation/debugging:

- adaptive selection provides less than a 10% sample advantage over both baselines;
- performance depends on hand-crafted experiment rules unique to each benchmark;
- the method becomes computationally impractical relative to the experiment budget;
- uncertainty estimates are consistently misleading;
- the comparison reveals that our formulation is simply a weaker reimplementation of a standard method with no useful architectural insight.

Failure is an acceptable result.

If the core hypothesis fails, record why and either:

- redesign the hypothesis once;
- narrow the research question;
- or kill Project 01 and return to the Idea Vault.

Do not keep a dead project alive because effort has already been invested.

---

# 13. Go Criteria for Stage B

Move to physical hardware only if Stage A demonstrates:

1. measurable adaptive sample-efficiency;
2. one reasoning implementation working across at least two system families;
3. clean separation between:
   - environment;
   - model/inference;
   - experiment selection;
   - evaluation;
4. reproducible benchmark results;
5. a clear reason why physical noise and instrumentation will teach something simulation cannot.

If these are satisfied, Stage B will identify a cheap physical system.

Likely first candidates:

- unknown RC/RLC network;
- thermal response system;
- low-cost motor dynamics.

Hardware is chosen **after** Stage A, not before.

---

# 14. Minimum Stage-A Architecture

Keep the codebase small.

```
machine-scientist/
├── README.md
├── pyproject.toml
├── src/
│   ├── environments/
│   ├── inference/
│   ├── policies/
│   └── evaluation/
├── experiments/
└── tests/
```

### environments/

Hidden dynamical systems implementing the shared experiment interface.

### inference/

Parameter/posterior estimation.

### policies/

- random;
- fixed;
- adaptive information-seeking.

### evaluation/

Metrics, repeated trials, plots, benchmark comparison.

### experiments/

Reproducible experiment configurations and result manifests.

---

# 15. First Implementation Milestone

The first milestone is deliberately tiny.

## MS-001

**One hidden first-order system.**

The program must:

1. sample unknown parameters;
2. allow a policy to select an input experiment;
3. simulate the response with noise;
4. update parameter beliefs;
5. repeat;
6. estimate the hidden parameters;
7. plot uncertainty shrinking over experiments;
8. compare random versus adaptive experiment selection.

Nothing else.

No second benchmark.

No LLM.

No hardware.

No elaborate agent framework.

No web application.

When MS-001 works and is reproducible, add Benchmark B.

---

# 16. What Daniele Needs to Learn First

Do **not** complete full courses before coding.

For MS-001, only the following concepts are initially required:

## Essential

- probability distributions;
- Bayes' rule;
- parameter estimation;
- basic dynamical systems / differential equations;
- numerical simulation;
- experimental design intuition;
- entropy or another uncertainty measure.

## Learn when required

- expected information gain;
- Monte Carlo approximation;
- state-space models;
- Kalman / particle filtering;
- symbolic regression;
- optimal control;
- nonlinear system identification.

The project determines when each topic becomes necessary.

---

# 17. AI Usage

AI should be used aggressively as a research and engineering accelerator for:

- explaining mathematics;
- reviewing derivations;
- finding literature;
- challenging assumptions;
- generating test cases;
- implementing scaffolding;
- debugging;
- suggesting alternative models;
- analyzing results;
- reviewing experiment validity.

However:

- the benchmark protocol must be deterministic/reproducible;
- important mathematical claims must be independently checked;
- Stage-A experiment selection should initially use explicit algorithms, not opaque LLM judgement;
- AI-generated code is not evidence that the scientific hypothesis is correct.

---

# 18. Research Log

Every major experiment records:

```
Question
Hypothesis
Code/config version
Hidden-system distribution
Policy
Experiment budget
Noise model
Metrics
Result
Interpretation
Unexpected observations
Next action
```

Results must be reproducible from configuration and seed.

---

# 19. Immediate Work Order

Do these in order.

## Task 1

Implement the first-order hidden environment.

## Task 2

Implement random and fixed policies.

## Task 3

Implement basic Bayesian parameter inference.

## Task 4

Implement the first adaptive uncertainty-reduction policy.

## Task 5

Run repeated simulations and plot:

- parameter error vs experiment count;
- posterior uncertainty vs experiment count;
- samples-to-target distribution.

## Task 6

Only after the above works, introduce Benchmark B.

---

# 20. Current Decision

**Project 01 is approved for Stage A.**

The project is not yet claiming a new invention.

The immediate objective is to determine whether a reusable, uncertainty-aware experimental reasoning core has enough technical merit to justify deeper research.

The next action is:

> **Create the Project 01 repository and implement MS-001.**

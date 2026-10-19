# OUTERFORM LABS — PROJECT PROCESS

> **Build what should not exist yet.**

This is the reusable invention process for every Outerform Labs project.

For **how to organize projects, learning, weekly work, and 30-day research cycles**, see [STRATEGY.md](STRATEGY.md).

The method is intentionally simple:

# IMAGINE → REDUCE → ATTACK → BUILD → DISCOVER

Do not create unnecessary documents for every stage.

Use this file as the guide.  
Create a project repository only when a real project has been selected.

---

# 1. IMAGINE

## Goal

Choose a future capability worth bringing into reality.

Do not start from:
- available tools;
- current products;
- what seems easy;
- what fits existing skills.

Start from:

> **What should exist that does not exist yet?**

Sources of imagination may include:
- science fiction;
- physics;
- biology;
- AI;
- robotics;
- cybersecurity;
- space;
- defence and resilience;
- human augmentation;
- computation;
- materials;
- energy;
- strange natural phenomena;
- cross-domain collisions;
- deliberate absurdity.

## Questions

- What new power would this give humans, machines, or civilization?
- Why is that capability exciting or important?
- Does it feel meaningfully ahead of today's normal technology?
- If it existed at maturity, would the future look different?

## Output

A short capability statement.

Example:

> Machines that can physically reorganize themselves to acquire different functions.

## Rule

**Do not research the state of the art before the capability is imagined clearly.**

---

# 2. REDUCE

## Goal

Understand what reality would require for the imagined capability to exist.

Ask:

> **What must be true?**

Strip away today's conventional implementation.

Reduce the capability into:
- required functions;
- physical requirements;
- information requirements;
- energy requirements;
- computation;
- sensing;
- actuation;
- materials;
- communication;
- control;
- biological constraints;
- environmental constraints;
- dependencies.

## First-principles questions

- Which constraints come from physics?
- Which constraints are merely current engineering conventions?
- What assumptions are we making?
- What happens if those assumptions are removed?
- What are the dependencies?
- What do we understand poorly?

## Classify every important unknown

### K — Known

We understand it sufficiently.

### L — Learn

Humanity knows it, but we do not.

→ Study it just in time.

### E — Engineering Unknown

The science is known, but implementation under our constraints is unsolved.

→ Design and experiment.

### S — Scientific Unknown

It may genuinely be unresolved by current science.

→ Research.

### F — Fundamental Constraint

Physics, mathematics, information theory, biology, or another fundamental principle may limit the idea.

→ Test this early.

## Output

A dependency map and a list of the most important unknowns.

Do not turn the map into bureaucracy.

It exists only to expose where reality can kill the idea.

---

# 3. ATTACK

## Goal

Find the **crux**.

The crux is:

> **The uncertainty whose resolution would most change our belief that the capability can be made real.**

Do not attempt to build the entire futuristic system.

Find the bottleneck.

## Now research deeply

Only now investigate:
- scientific papers;
- patents;
- textbooks;
- laboratories;
- companies;
- existing products;
- previous failed attempts;
- NASA / ESA / DARPA / academic programs;
- relevant open-source work.

Research should answer:

- What already exists?
- What has already been demonstrated?
- What approaches failed?
- Why does the full capability still not exist?
- Is our supposed bottleneck actually the bottleneck?
- Where is there genuine room for invention?

## Possible outcomes

### GO

There is a meaningful uncertainty worth attacking.

### PIVOT

The vision remains interesting, but our mechanism or attack point is wrong.

Return to REDUCE.

### KILL

The idea is already solved, fundamentally impossible under the intended assumptions, trivial, or not worth pursuing.

Return to IMAGINE.

## Define the technical thesis

A useful project has a statement approximately like:

> **Mechanism X may enable capability Y because principle Z could overcome bottleneck B.**

## Output

One clearly defined **crux** and one technical thesis.

---

# 4. BUILD

## Goal

Ask reality the smallest decisive question.

Before building, define:

### Hypothesis

What exactly do we believe?

### Experiment

What is the smallest system that can test it?

### Baseline

What are we comparing against?

### Metrics

What will we measure?

### Success condition

What result would make the hypothesis more credible?

### Failure condition

What result would make us reject or substantially change it?

Then build.

The artifact may be:
- software;
- simulation;
- mechanism;
- robot;
- circuit;
- sensor;
- material sample;
- experimental apparatus;
- mathematical model;
- biological model;
- hybrid system.

## Rule

> **Huge vision. Small decisive experiment.**

Do not build features that do not help answer the crux.

## Learning loop

When blocked:

**build → identify knowledge gap → learn → modify → test**

The project determines the curriculum.

---

# 5. DISCOVER

## Goal

Understand what reality actually told us.

Do not ask only:

> "Did it work?"

Ask:

- Why did it work?
- Why did it fail?
- Did the result match our model?
- Which assumption was wrong?
- Is the effect reproducible?
- Does it beat the baseline?
- What happens at the limits?
- Did we discover an unexpected phenomenon?
- Did the experiment reveal a better problem than the one we started with?

## Outcomes

### ITERATE

The thesis still looks promising.

Attack the next uncertainty.

### SCALE

The primitive works strongly enough to build a more capable prototype.

### PIVOT

Reality revealed a different mechanism or more important bottleneck.

Return to REDUCE or ATTACK.

### KILL

The path is not worth further effort.

Record the lesson and move on.

### BRANCH

The experiment revealed a new capability worth pursuing.

Return to IMAGINE with the new insight.

---

# PROJECT HIERARCHY

Never confuse these levels.

## Grand Vision

**What future should exist?**

Example:

> Machines capable of radically changing their physical embodiment.

## Project

**What concrete new capability are we trying to create?**

Example:

> A modular physical substrate capable of changing between multiple load-bearing morphologies.

## Crux

**What decisive uncertainty is blocking that capability?**

Example:

> Can one reversible connection mechanism provide both high load capacity and low-energy detachment?

## Experiment

**What is the smallest real test of that uncertainty?**

Example:

> Fabricate a small set of connector prototypes and measure strength, energy, cycle life, and reconfiguration reliability.

The Grand Vision may take decades.

The experiment may take days.

They are part of the same trajectory.

---

# OUTERFORM PROJECT CHECK

Before committing significant time to a project, ask:

- Does the mature capability feel like something that **should not exist yet**?
- Does it create a genuinely new power rather than merely another product feature?
- Are we thinking from capability rather than technology?
- Have we identified what reality actually requires?
- Do we know the crux?
- Are we learning because the project demands it?
- Is there a real experiment that can challenge our assumptions?
- Are we building rather than hiding inside research?
- Is the first prototype a true ancestor of the grand vision rather than an unrelated toy?

If the answers become weak, reconsider the project.

---

# WORKING PRINCIPLES

## Imagination before precedent

Do not let today's technology define tomorrow's imagination.

Use today's technology to determine where to place the first stepping stone.

## First principles before convention

"That is how it is normally done" is evidence, not law.

## Learn on demand

Do not attempt to master every prerequisite before beginning.

Go deep wherever the crux requires depth.

## Reality over narrative

A beautiful concept that fails experimentally is less valuable than an ugly experiment that reveals something true.

## Build early

Research should eventually terminate in an experiment.

## Kill freely

Do not protect an idea because time has already been spent on it.

## Follow surprises

Unexpected results can be more important than the original hypothesis.

## Cross disciplines

Fields are tools, not identities.

If the problem requires mechanics, learn mechanics.

If it requires neuroscience, learn neuroscience.

If it requires cryptography, materials science, control theory, biology, or orbital mechanics, go there.

## Keep documentation proportional

Document decisions, experiments, results, and knowledge worth preserving.

Do not document every thought.

Outerform exists to create technology, not paperwork.

---

# THE LOOP

```
                IMAGINE
                   │
                   ↓
                 REDUCE
                   │
                   ↓
                 ATTACK
                   │
                   ↓
                  BUILD
                   │
                   ↓
                DISCOVER
               ↙   ↓    ↘
          ITERATE PIVOT  KILL
             │      │
             └──────┴──────→ IMAGINE
```

Repeat until one of three things happens:

1. the capability becomes real;
2. reality reveals something more important;
3. the idea deserves to die.

Then begin again.

---

# THE OUTERFORM STANDARD

> **Imagine further ahead than current technology.**  
> **Reduce the impossible thing to what reality requires.**  
> **Attack the uncertainty that matters most.**  
> **Build the smallest thing that can prove you wrong.**  
> **Let reality decide what comes next.**

# Build what should not exist yet.

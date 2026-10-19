# OUTERFORM LABS — KNOWLEDGE DISCOVERY

> **You cannot know in advance everything you need to know. Learn how to discover what you are missing.**
>
> Practical field guide for researching an invention when the relevant disciplines, mechanisms, search terms, and connections are not yet obvious.

**Read alongside:** [PROCESS.md](PROCESS.md) for the invention method and [STRATEGY.md](STRATEGY.md) for how to organize projects and learning.

## The problem: unknown unknowns

An extraordinary capability can be easy to imagine and hard to investigate. You may not know:
- Which scientific principles govern it.
- Which functional requirements or failure modes matter.
- Which mechanisms have already been invented.
- Which search terms scientists and engineers use.
- Which cross-disciplinary connections could make an unconventional approach possible.

**This is normal.** A researcher does not begin with a complete map. The map is itself a research result.

Start with the *capability you want*, expressed in ordinary language — **not** with a list of disciplines you think you need to master. Discover the relevant subjects as you investigate.

This guide is part of **REDUCE** and **ATTACK**, and should be reused whenever **BUILD** or **DISCOVER** exposes a new gap. It is **not an extra bureaucratic phase**.

---

## The six-step knowledge-discovery loop

### 1. Describe the desired effect in plain language

Write:
- What should happen?
- To what, and in which environment?
- What would count as an observable demonstration?
- Why would that capability matter?

**Avoid committing to a mechanism too soon.** Saying "a robot constructs structures from local planetary materials" leaves room for fundamentally different solutions. Saying "a wheeled FDM printer" prematurely assumes an architecture.

**Output:** A 2–4 sentence capability statement.

### 2. Work backward from the effect to the functions

Ask **"What must physically or computationally happen for this effect to occur?"**

Discover functions before selecting disciplines or components:
- What must be **moved, transformed, sensed, estimated, transmitted, stored, supplied with energy, constrained, or controlled**?
- What enters and leaves the system? (matter, energy, forces, information)
- What must happen in what order?
- What environmental conditions or safety limits apply?
- Which parts are essential to the capability, and which are only one possible implementation?

Sketch a **rough function or dependency map**. It may be incomplete or wrong; revise it as evidence appears. List several possible mechanisms rather than automatically choosing the familiar one.

**Output:** A small functional diagram and a list of open questions. Do not attempt a complete architecture yet.

### 3. Discover terminology, existing mechanisms, and adjacent fields

Use a **broad-to-narrow search**:

1. Search in ordinary language for the desired effect or function.
2. Find technical overviews, textbooks, review papers, system diagrams, and existing implementations.
3. Extract the **precise terminology** used by experts.
4. Search again using that terminology and the specific failure mode or limitation.
5. Follow cited references *backward* and later papers that cite the promising work *forward*.
6. Look for **alternative mechanisms** in neighboring disciplines and similar problems solved in different settings.

For each useful source, ask:
- What has **actually been demonstrated** versus merely proposed?
- Under what assumptions, scale, input conditions, and measurement methods?
- What controls its performance? What makes it fail?
- What does it explain that I did not know to ask about?
- Where are the primary sources, data, equations, and specifications?

**Output:** New search terms, important principles, a few credible sources, and competing approaches.

### 4. Follow the dependencies without getting trapped in them

For every unfamiliar term, write:
- **What is it?** Explain it in your own words.
- **Why does it matter here?** Name the design decision, quantity, or hypothesis it affects.
- **What prerequisite blocks my understanding?** Only pursue what is needed to reason correctly.
- **How can I check it?** A calculation, worked problem, datasheet, simulation, expert critique, or measurement.

Use this classification from [PROCESS.md](PROCESS.md):

| Type | Meaning | Next action |
| --- | --- | --- |
| **K — Known** | Understood sufficiently for now | Apply it |
| **L — Learn** | Established knowledge that is new to us | Learn the relevant concept and test understanding |
| **E — Engineering unknown** | Working implementation under our constraints is uncertain | Model, design, prototype, measure |
| **S — Scientific unknown** | Possibly unresolved in research | Examine current literature; form an investigable hypothesis |
| **F — Fundamental constraint** | A physical or theoretical limit may block the idea | Quantify and challenge this constraint early |

Do not label something an unsolved scientific problem simply because you personally do not understand it. Do not follow an endless chain of prerequisites when a simpler experiment can provide useful evidence.

**Output:** A revised knowledge map, with the gaps that matter *now* marked clearly.

### 5. Hunt blind spots and cross-disciplinary connections

A useful challenge session asks:

- **Conservation:** Where do energy, momentum, charge, matter, and information go?
- **Limits:** What scales badly with size, time, distance, temperature, noise, or error?
- **Interfaces:** How do subsystems couple? What must cross their boundaries?
- **Control:** What can actually be observed and commanded? What feedback is missing?
- **Materials and environment:** What fails under realistic conditions?
- **Alternatives:** Can another physical effect or architecture perform the same function?
- **Analogy:** Where else has a mathematically similar problem appeared (biology, control, optics, networks, mechanics, etc.)?
- **Disconfirmation:** What observation would show the proposed mechanism is inadequate?
- **Novelty:** Is this truly untried, or simply unfamiliar to us?

**An analogy generates hypotheses; it is not proof.** Check units, equations, boundary conditions, performance, and experimental evidence before transferring a solution between fields.

Use colleagues, technical communities, domain experts, and AI for criticism — not only for enthusiasm.

**Output:** A more complete list of plausible mechanisms, risks, and critical assumptions.

### 6. Stop mapping and test the decisive question

Knowledge discovery must converge on action.

Choose **one crux**: the uncertainty whose resolution would most change the next engineering or research decision.

Define:
- **Question:** What specifically do we need to find out?
- **Prediction:** What should happen if our model is correct?
- **Test:** What is the smallest safe, useful calculation, simulation, or experiment?
- **Metric and baseline:** What will we measure and compare?
- **Decision:** What result would make us continue, redesign, or abandon this mechanism?

Then **BUILD → MEASURE → DISCOVER**. New experimental results will expose new unknowns; re-enter this guide whenever useful.

**Stop rule:** You do *not* need a complete disciplinary knowledge map to begin. You need enough understanding to conduct a meaningful, safe test and interpret its limitations.

---

## Where to look — a practical source ladder

| When you are stuck on… | Start with… | Then deepen with… |
| --- | --- | --- |
| "I don't even know the right words" | Explanatory overviews, reference textbooks, AI-assisted terminology exploration | Review papers and terminology from methods sections |
| "What science governs this?" | Core physics/mathematics books, technical lecture notes | Specialized textbooks and original papers |
| "Has anyone demonstrated this?" | [Google Scholar](https://scholar.google.com/), [arXiv](https://arxiv.org/), institutional repositories | Original experimental papers, data, and follow-up citations |
| "Is there a similar invention?" | [Google Patents](https://patents.google.com/), [GitHub](https://github.com/), technical reports | Designs, patents, failure analyses, direct comparisons |
| "How is this built?" | Manufacturer datasheets, application notes, open hardware and software documentation | Schematics, CAD, engineering manuals, measured reference designs |
| "What is known in space systems?" | [NASA Technical Reports Server](https://ntrs.nasa.gov/), relevant agency technical publications | Test campaigns, standards, mission design reports |
| "Is my hypothesis correct?" | Equations, order-of-magnitude estimates, simulation | Controlled experiments and independent replication |

**Source discipline:** Prioritize textbooks, peer-reviewed papers, primary experimental reports, manufacturer specifications, and reproducible implementations. Preprints may be valuable but are not automatically peer reviewed; patents describe claimed inventions, not necessarily working demonstrations. Confirm important claims in primary sources. Record the paper title, author, year, link, assumptions, and key evidence rather than hoarding PDFs.

**Search pattern:**

```text
desired effect / function
→ existing implementations and review articles
→ technical mechanism and vocabulary
→ performance limitation or failure mode
→ governing physics and measurable parameters
→ specific hypothesis or experiment
```

---

## Worked example: PHOTON — optical wireless power transfer

**Observation:** A laser pointer illuminated a photovoltaic panel, but no useful electrical output was observed.

**Initial hypothesis:** Perhaps the beam is too small relative to the panel.

**Discover variables rather than guessing a single cause:**
- Optical power actually delivered to the panel, not just spot diameter.
- Spot size, irradiance, incidence angle, and alignment.
- Wavelength and the photovoltaic cell's spectral response.
- Electrical load, I–V curve, and maximum-power point.
- Optical and electrical losses, ambient illumination, and measurement sensitivity.

**Fields that emerge naturally:** optics, semiconductor devices, electrical circuits, energy conversion, metrology.

**New research terms:** "photovoltaic spectral response", "irradiance", "maximum power point", "photovoltaic I–V curve", "optical wireless power transfer efficiency".

**First useful question:** How much **electrical power under load** does this panel produce under controlled illumination, relative to ambient light?

- Measure voltage **across a known suitable load** and determine current through it; for a resistive load, `P = V² / R` (equivalently `P = V × I`).
- Compare illumination and dark/ambient baselines with the same setup, and record conditions.
- **Open-circuit voltage alone is not useful delivered power.**
- Treat a laser's optical hazard separately; never look into a beam or its specular reflections. Low-power non-laser sources can be safer for initial comparative tests.

**Lesson:** You didn't have to know photovoltaic spectral response before starting. Investigation of a disappointing result *revealed* the concept and what to measure next.

---

## How to use AI without outsourcing your scientific thinking

AI can help **discover vocabulary, map functions, propose alternative mechanisms, explain unfamiliar concepts, and identify possible blind spots**. It can also be wrong or confidently invent references. Use its output as a set of leads, never as final evidence.

### Prompt: map my unknown unknowns

```text
OUTERFORM LABS — KNOWLEDGE DISCOVERY

Capability I wish existed:
[describe in ordinary language]

Act as a multidisciplinary scientist and research engineer.
Assume I may not know which disciplines, physical mechanisms,
terminology, and constraints matter.

1. Work backward from the capability to the required functions.
2. Identify competing mechanisms and the scientific principles behind them.
3. Show cross-disciplinary connections I may be overlooking.
4. Distinguish established knowledge, my learning gaps, engineering
   uncertainties, potentially open scientific questions, and physical limits.
5. Give specific technical search terms and types of authoritative sources.
6. Challenge your own assumptions and identify the largest blind spots.
7. Propose the smallest decisive question worth testing first.

Do not assume the idea is novel. Do not invent citations.
Explain *why* each concept matters, not merely which subject to study.
Keep the initial map concise and expand only when asked.
```

### Prompt: challenge the proposed experiment

```text
My hypothesis, model, and proposed test are:
[describe them]

Act as a skeptical interdisciplinary reviewer.
What important physical effects, missing variables, confounders,
alternative explanations, scaling problems, safety risks,
and existing solutions might I be missing?
What is the single most informative next measurement?
Separate evidence from speculation and suggest how to verify claims.
```

After receiving an AI answer:
1. Explain the proposed mechanism **in your own words**.
2. Verify critical physics and factual claims using credible sources.
3. Make at least one prediction or calculation yourself.
4. Compare the prediction with a model or experiment.
5. Record what you learned and the next question.

The goal is to become **less dependent** on AI over time, not more.

---

## How scientific intuition and connections develop

Maintain systematic foundational learning **independently of the active project**. For now, that can mean progressively studying physics with mathematics as a companion, solving problems and deriving results — while using targeted resources for the active invention.

Over time, deliberately notice shared models:
- **Energy and power balances** appear in motors, batteries, optical transfer, and propulsion.
- **Differential equations and feedback** appear in mechanisms, electronics, biological regulation, and spacecraft.
- **Noise, uncertainty, and estimation** appear in sensors, navigation, and communication.
- **Geometry and scaling** appear in optics, structures, heat transfer, and manufacturing.

When you notice a connection, ask: *Do the equations and constraints genuinely match, or is this just an evocative analogy?*

Original connections arise from repeated exposure, deeper understanding, careful comparison, and experimentation — not from needing to memorize all disciplines first.

---

## Minimal knowledge-discovery note

Do not produce a giant report for every question. In the project notebook, write:

```markdown
### Knowledge discovery — [question]

Desired effect:
What I currently think happens:
Unknown concepts / useful search terms:
Relevant mechanisms and alternative approaches:
What sources actually demonstrate:
Critical assumptions / blind spots:
Most important question to test next:
Next concrete action:
```

Update only what changes as you investigate.

## Remember

- **Begin with the capability, not an assumed curriculum.**
- **Functions reveal mechanisms; mechanisms reveal disciplines.**
- **Research reveals terminology; experiments reveal missing assumptions.**
- **Never mistake your own unfamiliarity for genuine scientific novelty.**
- **You will miss connections. Use sources, specialists, criticism, and measurement to expose them.**
- **Map only enough to choose the next useful experiment.**
- **Keep studying foundations so that, over time, more connections become visible to you.**

> **The polymath is not someone who already knows everything. The polymath is someone who can enter an unfamiliar problem, discover what matters, learn it, and test an original idea against reality.**

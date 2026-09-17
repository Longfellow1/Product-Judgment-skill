# Yu Jun Skill · Product Judgment

**Judge the demand before writing the PRD.**

This skill turns core ideas from *Yu Jun's Product Methodology* into an executable demand-review workflow for AI agents.

It does not exist to make an idea sound more complete. It exists to answer a harder question first: **does this demand deserve to be built?**

[中文](README.md) · [SKILL.md](SKILL.md) · [Examples](examples/) · [Methodology](references/yu-jun-methodology.md)

---

## Why this exists

AI makes PRDs, prototypes, and code cheaper. It also makes **bad demand cheaper to implement**.

Many projects fail not because they cannot be built, but because nobody answered these questions early enough:

- Who is the real user?
- At what specific moment are they stuck?
- How do they solve the problem today?
- Does the new experience outweigh the old experience and switching cost?
- Is the evidence strong enough for the resource commitment?

Yu Jun Skill moves these questions in front of the roadmap, PRD, and engineering work.

---

## A typical example

### Input

> Our competitor launched AI Search. We should ship it too or users will leave.

### It does not start with

- which model to use
- where the search entry should live
- how fast the team can ship
- how to write the PRD

### It starts with judgment

```text
Verdict: VALIDATE FIRST
Evidence: L0
Pattern: Competitor Anxiety

The trigger is “the competitor shipped it,” not an observed user problem in a search task.
“Users will leave” is still an assumption, not evidence.
```

Then it asks what is actually failing in the current search experience, whether users abandon tasks because of it, whether the failures cluster in high-value scenarios, and whether a lower-cost solution already exists.

→ [Full example: competitor feature](examples/competitor-feature.md)

---

## Core judgment framework

### 1. Anchor the user and the moment

Before judging any demand, answer three questions:

```text
Who is using it?
At what specific moment are they stuck?
How do they solve it today?
```

### 2. Evaluate user value

```text
User Value = New Experience - Old Experience - Replacement Cost
```

A stronger feature does not automatically create more user value. Migration, learning, trust, and workflow change all carry real cost.

### 3. Interrogate critical assumptions

The skill makes the assumptions behind a demand explicit and grades the evidence behind them:

| Level | Evidence |
|---|---|
| L0 | Internal opinion, executive preference, competitor move |
| L1 | User statements, interviews, complaints |
| L2 | Small-sample behavioral observation, usability testing |
| L3 | Real usage data, conversion, A/B testing |
| L4 | Payment, renewal, commercial validation |

### 4. Forecast the failure

Instead of saying “there are risks,” it describes **how the product is likely to fail over the coming months if the current logic is wrong**, from a user and product perspective.

### 5. Produce a clear verdict

```text
BUILD
VALIDATE FIRST
DE-SCOPE
REFRAME
KILL
```

No “it depends.” A verdict should change only when new evidence appears.

---

## Three modes

### Quick Judgment

For everyday product discussions, ideas, and demand sanity checks.

> “We want to build an AI weekly-report feature. Is it worth doing?”

Give the context to an agent running this skill. It anchors the user scenario first, then executes the judgment workflow.

### Formal Review

For project gates, team reviews, or decisions that need a durable record.

```bash
python scripts/demand-check.py
python scripts/demand-check.py --scan
python scripts/demand-check.py --from docs/prd.md
python scripts/demand-check.py --feature "AI meeting assistant"
```

It outputs `JUDGMENT.md`, preserving *why* a demand was approved, reframed, delayed, or rejected.

### Direction Setting

For situations where the direction is resisted, scope is expanding, or the current solution feels wrong but the next direction is unclear.

The skill first identifies whether the resistance comes from evidence, communication, resources, or the direction itself, then recommends the next move.

---

## When to use it

**Good fit:**

- before starting a new feature or product
- before writing the PRD
- roadmap trade-offs
- “our competitor has it, should we build it too?”
- “leadership wants it, but user value is unclear”
- scope convergence
- demand gates in fast AI / agent product development

**Not for:**

- writing a full PRD
- technical architecture review
- pure UI or copy polish
- engineering implementation after demand is already validated

---

## Install and use

```bash
git clone https://github.com/Longfellow1/Yujun-skill.git
cd Yujun-skill
```

The core skill is [`SKILL.md`](SKILL.md). It can be used with Claude Code, Codex, or other agent workflows that support reusable skills or system-instruction injection.

Repository structure:

```text
Yujun-skill/
├── SKILL.md
├── README.md
├── README.en.md
├── references/
├── examples/
├── scripts/
│   └── demand-check.py
└── templates/
    ├── JUDGMENT.md
    └── CLAUDE.md
```

---

## Method source and attribution

This skill is **inspired by core ideas from *Yu Jun's Product Methodology* and related public product thinking**, especially the user model, user value, transaction model, and product decision-making.

It is not a summary of the book and does not reproduce the original text. It is an independent implementation that reorganizes those ideas into an executable agent workflow for practical demand review.

**This is an unofficial project and is not affiliated with, authorized by, or endorsed by Yu Jun.**

See [`references/yu-jun-methodology.md`](references/yu-jun-methodology.md) for the methodology notes used by the skill.

---

## Companion skill

When the demand is valid and the problem becomes “which layer should own this badcase?”, use:

**[Principled Simplicity · 大道至简 Skill](https://github.com/Longfellow1/principled-simplicity)**  
*Fix the layer, not the case.*

---

## License

Apache-2.0

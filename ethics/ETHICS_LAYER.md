---
id: ethics-layer
version: "1.0"
status: canonical
category: system
uri: https://ontology.cuqou.com/ethics
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Cuqou Ethics Layer

## What This Layer Is

The Ethics Layer is the fourth structural layer of the Cuqou Relationship Ontology:

| Layer | Answers | Location |
|---|---|---|
| **Ontology** | What is this? | `vocabulary/`, `knowledge/` |
| **Grammar** | How do concepts relate? | `knowledge/taxonomy/` |
| **Decision** | What should be done? | `decision/` |
| **Ethics** | What must AI never do? | `ethics/` |

---

## Why Ethics Is a Separate Layer

Most AI systems define what they can do. Cuqou defines what it must not do.

This is a philosophical difference, not a technical one.

The Decision Layer contains **logical constraints** — things that cannot be inferred because the ontology does not support them (e.g., "Relationship State does not determine Protocol").

The Ethics Layer contains **ethical constraints** — things that must not be done even if they are technically possible (e.g., "AI must not send a Greeting Card without the user's explicit approval").

| Layer | Constraint type | Example |
|---|---|---|
| Decision / `constraints.yaml` | Logical — *cannot* be inferred | "CRP does not require conflict" |
| Ethics / `rules.yaml` | Ethical — *must not* be done | "AI must not send autonomously" |

Conflating these two types would obscure the reasoning behind each constraint. A logical constraint says "this conclusion does not follow." An ethical constraint says "this action is prohibited regardless of whether it would work."

---

## The Core Question

The Ethics Layer exists to answer one question, consistently, across every feature:

> *Does this action respect the human whose relationship this is?*

If the answer is "no" — the action is prohibited, regardless of technical capability, user engagement benefit, or business value.

---

## Layer Structure

```
ethics/
├── ETHICS_LAYER.md        — This document
└── rules.yaml             — Ethical rules (E001–E00N)
```

Rules are not organized by domain — they are organized by priority:
- `priority: constitutional` — equivalent to Tier 0 in FOUNDER_DECISIONS; cannot be overridden
- `priority: core` — strong default; deviation requires Maintainer approval
- `priority: recommended` — default behavior; may be adjusted by implementation context

---

## Relationship to FOUNDER_DECISIONS

Every rule with `priority: constitutional` in this layer corresponds to a Tier-0 Founder Decision.

| Ethics Rule | Founder Decision |
|---|---|
| E001 — Human Contribution | §25 — Human Voice Preservation |
| E005 — No Autonomous Action | §25.5 — No auto-send |

---

## How AI Systems Should Load This Layer

1. Load `ethics/rules.yaml` before any action that involves another person
2. Check if the proposed action is prohibited by any rule at `constitutional` priority
3. If prohibited — stop; do not proceed regardless of user intent
4. If permitted — proceed through the Decision Layer

The Ethics Layer is loaded before the Decision Layer. A prohibited action does not become permitted because a Decision Layer rule recommends it.

---

## Stability

Ethics rules at `constitutional` priority are the most stable documents in the ontology. They change less often than canonical concept definitions.

Changes to `constitutional` rules require:
1. An RFC documenting the change
2. Explicit Founder decision
3. Amendment to the corresponding FOUNDER_DECISIONS section

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/ethics*  
*License: CC BY 4.0 — Attribution required*

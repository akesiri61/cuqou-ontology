---
version: "1.0"
status: canonical
uri: https://ontology.cuqou.com/flow
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Relationship Flow

## The Horizontal View of How a Relationship Expression Moves

This document describes how a relationship expression moves through the Cuqou system — from the moment a human decides to act, to the moment an expression reaches another person.

The Architecture (`ARCHITECTURE_OF_RELATIONSHIP.md`) describes *what layers exist*.  
This document describes *how a single expression flows through those layers*.

Two documents, two perspectives, one coherent system.

---

## The Flow

```
┌─────────────────────────────────────────────────────────────────┐
│                    RELATIONSHIP TRUTH                           │
│              (Axiom — governs the entire flow)                  │
└─────────────────────────────┬───────────────────────────────────┘
                              │
                    ┌─────────▼─────────┐
                    │  Human Decision   │ ← A human chooses to act
                    │  Intent Provenance│   Is the intent human-originated?
                    └─────────┬─────────┘
                              │
                    ┌─────────▼─────────┐
                    │     Intent        │ ← What does the person want?
                    │                   │   prepare / maintain / celebrate /
                    └─────────┬─────────┘   reconnect / resolve / support…
                              │
                    ┌─────────▼─────────┐
                    │    Decision       │ ← What does the system recommend?
                    │                   │   Protocol selection, constraints,
                    └─────────┬─────────┘   artifact suggestions
                              │
                    ┌─────────▼─────────┐
                    │    Protocol       │ ← How will the expression travel?
                    │                   │   CPP (sync) or CRP (async)
                    └─────────┬─────────┘
                              │
                    ┌─────────▼─────────┐
                    │   Expression      │ ← What form will care take?
                    │                   │   message / card / memory /
                    └─────────┬─────────┘   voice / presence
                              │
                    ┌─────────▼─────────┐
                    │Human Contribution │ ← Whose voice is present?
                    │    (Spectrum)     │   The human contributes, modifies,
                    └─────────┬─────────┘   or replaces AI-assisted content
                              │
                    ┌─────────▼─────────┐
                    │  Human Agency     │ ← Who approves the final action?
                    │  (Final Approval) │   The human reviews and confirms
                    └─────────┬─────────┘   before anything is sent
                              │
                    ┌─────────▼─────────┐
                    │     Medium        │ ← Through what channel?
                    │                   │   LINE / App / Email / In-person
                    └─────────┬─────────┘
                              │
                    ┌─────────▼─────────┐
                    │   Experience      │ ← What does the recipient receive?
                    │                   │   And what does the sender feel?
                    └───────────────────┘
```

---

## What the Flow Is Not

This is not a UI flow. It does not describe screens, buttons, or interactions.

This is not a database schema. It does not describe models, fields, or queries.

This is the **conceptual sequence** that every relationship expression follows — regardless of how it is implemented, which platform delivers it, or which AI model assists with it.

Any implementation of a Cuqou experience must be able to map itself to this flow.

---

## Where Each Principle Enters

| Flow Stage | Governing Concept | Layer |
|---|---|---|
| Human Decision | [Intent Provenance](knowledge/concepts/intent-provenance.md) | 1 — Stewardship |
| Intent | [Intent Taxonomy](knowledge/taxonomy/intent-taxonomy.md) | 2 — Language |
| Decision | [Decision Layer](decision/DECISION_LAYER.md) | 3 — Intelligence |
| Protocol | [CPP](knowledge/protocols/cpp.md) / [CRP](knowledge/protocols/crp.md) | 2 — Language |
| Expression | [Relationship Grammar](knowledge/taxonomy/RELATIONSHIP_GRAMMAR.md) | 2 — Language |
| Human Contribution | [Human Contribution](knowledge/concepts/human-contribution.md) | 1 — Stewardship |
| Human Agency | [Human Agency](knowledge/principles/human-agency.md) | 1 — Stewardship |
| Medium | [Relationship Grammar](knowledge/taxonomy/RELATIONSHIP_GRAMMAR.md) | 2 — Language |
| Experience | [Experience Patterns](experience-patterns/) | 4 — Experience |

---

## The Stewardship Check

At two points in the flow, the Stewardship Principles intervene:

**At the start — Intent Provenance:**
> "Did a human decide to reach out? Or is this AI acting autonomously?"  
> If Intent Provenance is absent → the flow stops here.

**Before send — Human Agency + Human Contribution:**
> "Is the human the final authority on this action?"  
> "Is the human's own voice present in this expression?"  
> If either check fails → the system must return to the Expression stage, not proceed.

---

## A Note on AI

AI may participate at every stage of this flow — suggesting the intent, recommending the protocol, drafting the expression, selecting the medium.

But AI participates as an **assistant** at each stage, not as the **decision-maker**.

The human is the one who decides to reach out.  
The human is the one who chooses what to say.  
The human is the one who approves before anything is sent.

AI amplifies the human's capacity at every stage.  
AI does not replace the human at any stage.

---

## Using This Flow

**For ontology contributors:** any new concept must map to a stage in this flow.

**For product designers:** any feature must be traceable to one or more stages in this flow.

**For AI system builders:** the flow defines where AI assistance is appropriate and what form it may take at each stage.

**For Experience Pattern authors:** an Experience Pattern describes how a specific context enters the flow and how the result is delivered to the person.

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/flow*  
*License: CC BY 4.0 — Attribution required*

---
version: "1.0"
status: canonical
uri: https://ontology.cuqou.com/conformance-checklist
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Ontology Conformance Checklist

## Definition of Done

A feature may be merged when it passes all four reviews below.

This checklist is not a bureaucratic gate. It is the proof that the Living Ontology — which governs design, AI behavior, product decisions, and code review — has been honored in this implementation.

---

## Before Starting: The 4 Questions

Every feature begins here — before a line of code, before a wireframe, before a spec.

> **1. Human Problem**  
> What recurring human problem does this solve?  
> *(If this cannot be named, the feature is not ready to build.)*

> **2. Relationship Truth**  
> How does this problem connect to the authenticity of human relationships?  
> *(If it doesn't, it's out of scope.)*

> **3. Existing Foundation**  
> Can the existing ontology cover this — without adding new layers, axioms, or principles?  
> *(If yes, proceed. If no, open an RFC before continuing.)*

> **4. Implementation**  
> Given the foundation exists, what is the best experience for this human problem?  
> *(Only ask this after the first three are answered.)*

---

## Review 1 — Traceability

Every user action in this feature must trace back to the ontology.

- [ ] **Relationship Truth** — the feature can be traced back to the Axiom
- [ ] **Stewardship Principles** — Human Agency, Human Contribution, and Intent Provenance all apply or are explicitly noted as not applicable (with reason)
- [ ] **Experience Pattern** — the feature fits within a defined canonical Experience Pattern, or a new Pattern has been written and approved
- [ ] **Decision Rules** — the system's recommendations and constraints reference existing Decision Layer rules
- [ ] **TRACEABILITY_MATRIX.md** — a row has been added for each new user action in this feature

*Failure here = Implementation Drift or Foundation Gap. Diagnose before proceeding.*

---

## Review 2 — Human Review

The feature must preserve the three Stewardship Principles in practice — not just in theory.

**Human Agency**
- [ ] The person can choose not to engage
- [ ] No action reaches another person without explicit per-action human approval
- [ ] The person can cancel at any stage before an expression is sent

**Human Contribution**
- [ ] The person's own words, memories, or intentions are present in any expression sent
- [ ] AI-generated content is transparently distinguished from human-authored content
- [ ] The human can modify or replace any AI-contributed content
- [ ] `human_contribution_score` is tracked internally (never shown as gamification)

**Intent Provenance**
- [ ] The system can distinguish between human-initiated intent and AI-triggered intent
- [ ] No expression is sent based on an automated trigger without human decision at the time of sending

---

## Review 3 — Experience Review

The feature must not become one of the named Anti-patterns.

**The feature must not:**
- [ ] Manufacture guilt, obligation, or urgency ("You haven't contacted them in 47 days")
- [ ] Manipulate the recipient's emotional state in ways the sender did not intend
- [ ] Create a streak counter or gamify relationship regularity
- [ ] Assign a relationship health score or grade
- [ ] Become a task manager or obligation inbox
- [ ] Send any relationship expression autonomously
- [ ] Fabricate memories, emotions, or experiences on behalf of the user
- [ ] Position the system as the judge of relationship quality

**Verify against the relevant Experience Pattern's Anti-patterns section.**

---

## Review 4 — Foundation Review

The feature must not require expanding the foundation.

- [ ] No new structural layer was added
- [ ] No new Axiom was added
- [ ] No new Stewardship Principle was added (without RFC)
- [ ] No canonical Concept was redefined to fit this feature
- [ ] No Experience Pattern template was altered (new fields require Maintainer approval)

**If any of the above required a change:**
- [ ] An RFC was opened *before* the change was made
- [ ] The RFC is referenced in this PR
- [ ] The Maintainer reviewed and accepted the RFC

*Fixing a bug or clarifying a definition does not require an RFC.*  
*Adding to the Foundation does.*

---

## The Development Pipeline

Every feature follows this pipeline. No exceptions.

```
Human Problem identified
        ↓
4 Questions answered
        ↓
TRACEABILITY_MATRIX.md row added
        ↓
Experience Pattern confirmed (or new Pattern written)
        ↓
Implementation built
        ↓
Conformance Checklist completed
        ↓
Merge
```

If a step is skipped, the checklist will catch it. The checklist exists so that skipping is visible — not invisible.

---

## What This Checklist Proves

When this checklist is completed for a feature, it proves one thing:

> **The feature was built from the ontology — not around it.**

This is the difference between a Living Ontology and a document library.

A document library is referenced when convenient.  
A Living Ontology governs every decision — design, AI, product, and code — and every feature can prove it.

---

## Ontology KPI Tracking

Each completed checklist contributes to Phase II KPIs:

| KPI | Updated by this checklist |
|---|---|
| **Ontology Coverage** | Was the feature traceable without new concepts? |
| **Foundation Stability** | Did this feature require opening an RFC? |
| **Decision Traceability** | Were all Decision Rules cells in the matrix filled? |
| **Pattern Reusability** | Did the feature use an existing Experience Pattern? |

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/conformance-checklist*  
*License: CC BY 4.0 — Attribution required*

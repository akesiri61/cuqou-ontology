---
version: "1.0"
status: canonical
uri: https://ontology.cuqou.com/traceability
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Traceability Matrix

## Purpose

Every user action in a Cuqou implementation must trace back to the ontology.

This document is the working tool for Phase II Behavioral Validation. It has one job:

> **Prove that Cuqou Ontology v1.0.0 is Executable Knowledge.**

"Executable Knowledge" means: the ontology does not just describe relationships — it can be traced into design decisions, system behavior, and user experience in a verifiable chain.

---

## The Traceability Test

Before every feature, PR, or user flow is accepted:

**1. Relationship Truth**
> "Can this user action be traced back to the Axiom — Relationship Truth?"  
> If no → the feature does not belong in Cuqou.

**2. Principles**
> "Does this use the Stewardship Principles already defined (Human Agency, Human Contribution, Intent Provenance)?"  
> If no → before adding a new principle, prove the existing ones cannot cover it.

**3. Pattern**
> "Does this fit within a defined Experience Pattern?"  
> If no → either the action is outside scope, or a new Pattern is needed (via the canonical template).

**Scoring:**
- All 3 YES → Foundation validated for this action. Proceed.
- Any NO → Stop. Diagnose: is this Implementation Drift, or a genuine Foundation Gap?
  - Implementation Drift → fix the implementation, not the ontology
  - Foundation Gap → open an RFC before adding anything to the foundation

---

## How to Read the Matrix

| Column | What it records |
|---|---|
| **User Action** | What the person does in the UI |
| **Experience Pattern** | Which Layer 4 pattern governs this action |
| **Decision Rules** | Which Layer 3 rules apply |
| **Protocol** | Which Layer 2 protocol is activated |
| **Principles** | Which Layer 1 Stewardship Principles apply |
| **Axiom** | Always: Relationship Truth |
| **Trace** | ✅ if all columns connect; ⚠️ if a gap is found |

---

## Reference Implementation: Cuqou LINE Mini App

The flows below represent the Phase II Reference Implementation.  
Each row is a Traceability Test result.

### Flow A — Attention: WFM Discovery

*The person encounters Waiting For Me and sees a relationship that needs attention.*

| User Action | Experience Pattern | Decision Rules | Protocol | Principles | Axiom | Trace |
|---|---|---|---|---|---|---|
| Receives LINE Digest | Waiting For Me | Recommendation Rules (P001–P005) | CRP / CPP | Intent Provenance — the system surfaces; human decides | Relationship Truth | ✅ |
| Opens Mini App from Digest | Waiting For Me | — | — | Human Agency — person chose to open | Relationship Truth | ✅ |
| Views WFM list | Waiting For Me | State-aware surfacing (C001, C005) | CRP / CPP | Human Agency — no action taken yet | Relationship Truth | ✅ |
| Taps a relationship to view | Waiting For Me | Artifact Suggestion (A001–A005) | CRP / CPP | Intent Provenance — person initiates inquiry | Relationship Truth | ✅ |

---

### Flow B — Action: Sending a Greeting Card (CRP)

*The person chooses to send a CRP expression — a Greeting Card.*

| User Action | Experience Pattern | Decision Rules | Protocol | Principles | Axiom | Trace |
|---|---|---|---|---|---|---|
| Selects "Send Greeting Card" | Waiting For Me | Artifact Selection (A001) | CRP | Human Agency — person selects action | Relationship Truth | ✅ |
| Views AI-suggested card message | Waiting For Me | Human Contribution Check (C006) | CRP | Human Contribution — contribution_score surfaced internally | Relationship Truth | ✅ |
| Edits AI message with own words | Waiting For Me | — | CRP | Human Contribution ↑ (score increases toward 1.0) | Relationship Truth | ✅ |
| Reviews card before sending | Waiting For Me | Human Approval (E005) | CRP | Human Agency — explicit per-action review | Relationship Truth | ✅ |
| Presses Send | Waiting For Me | Human Approval confirmed | CRP | Human Agency + Human Contribution | Relationship Truth | ✅ |
| Cancels — decides not to send | Waiting For Me | — | — | Human Agency — right to cancel preserved | Relationship Truth | ✅ |

---

### Flow C — Relationship: CPP Preparation

*The person prepares for a difficult conversation using CPP.*

| User Action | Experience Pattern | Decision Rules | Protocol | Principles | Axiom | Trace |
|---|---|---|---|---|---|---|
| Selects "Prepare for conversation" | Waiting For Me | Protocol Selection (P002) | CPP | Intent Provenance — person initiates | Relationship Truth | ✅ |
| Answers the 4 Standard Questions | Waiting For Me | — | CPP | Human Contribution — answers are person's own | Relationship Truth | ✅ |
| Views AI-suggested answer | Waiting For Me | Human Contribution Check | CPP | Human Contribution — modifiable; not mandatory | Relationship Truth | ✅ |
| Modifies AI suggestion | Waiting For Me | — | CPP | Human Contribution ↑ | Relationship Truth | ✅ |
| Saves preparation | Waiting For Me | — | CPP | Human Agency — person decides when ready | Relationship Truth | ✅ |

---

### Flow D — Management: Relationship Context

*The person views or updates a relationship's context (CPP notes, history).*

| User Action | Experience Pattern | Decision Rules | Protocol | Principles | Axiom | Trace |
|---|---|---|---|---|---|---|
| Opens Relationship Profile | (context, not a pattern) | C001 (State ≠ Protocol trigger) | — | Human Agency — reading, no action | Relationship Truth | ✅ |
| Views past CPP notes | (context) | — | CPP | Human Contribution — content was person's own | Relationship Truth | ✅ |
| Adds a manual note | (context) | — | — | Human Contribution — fully human-authored | Relationship Truth | ✅ |
| Views relationship state | (context) | C005 (State = observed, not assigned) | — | Intent Provenance — state is observed, never manufactured | Relationship Truth | ✅ |

---

## Traceability Failure Examples

These are signals that should stop implementation and trigger diagnosis.

| User Action | Trace | Reason for Failure | Diagnosis |
|---|---|---|---|
| "Auto-send birthday card at midnight" | ❌ | No Human Agency — system acts without human decision | Implementation Drift — violates E005 |
| "Relationship health score shown to user" | ❌ | No Principle covers AI-assigned quality judgment | Implementation Drift — system becoming judge |
| "Day streak counter on WFM" | ❌ | Contradicts WFM Anti-pattern: Streak Counter | Implementation Drift — violates Pattern Resolution |
| "Notify user because they haven't contacted in 47 days" | ❌ | Manufactures obligation — violates Attention Layer CR3 | Implementation Drift — guilt engine |
| "AI selects which protocol to use without human confirmation" | ❌ | Intent Provenance broken — human didn't initiate | Implementation Drift — violates stewardship |

---

## Gap vs. Drift Diagnosis

When a Traceability Test fails, determine which kind of failure:

| | Implementation Drift | Foundation Gap |
|---|---|---|
| What it means | The feature was designed in a way that conflicts with the ontology | The ontology doesn't have the concepts needed to describe this feature |
| What to do | Redesign the feature to fit the existing ontology | Open an RFC; document the gap; do not add to foundation without review |
| Phase II Rule | Fix the implementation | Do not expand the foundation — verify it's a true gap first |
| How common | Common (most failures are drift) | Rare — by design; v1.0.0 was built to be sufficient |

---

## Adding Rows

When a new feature or user action is designed, add a row to this matrix before implementation begins.

**Template:**

```
| [User Action] | [Experience Pattern] | [Decision Rules] | [Protocol] | [Principles] | Relationship Truth | [✅ or ⚠️ + note] |
```

If any column cannot be filled — the feature requires a Traceability Test before proceeding.

---

## What "Executable Knowledge" Means

The chain below is the proof of Phase II:

```
Ontology (v1.0.0)
        ↓
Traceability Matrix
        ↓
User Flow (design)
        ↓
UI (implementation)
```

If every row in this matrix traces cleanly, and new rows continue to trace without expanding the foundation, then `cuqou-ontology v1.0.0` is proven Executable Knowledge: a knowledge system that can be translated into verifiable design and behavior — not just described in documents.

---

## Ontology KPI Tracking

| KPI | Measured by | Current |
|---|---|---|
| **Ontology Coverage** | % of matrix rows with ✅ trace | — (Phase II in progress) |
| **Foundation Stability** | RFC count during Phase II | 0 |
| **Decision Traceability** | % of Decision Rules cells filled in matrix | — |
| **Pattern Reusability** | All rows covered by existing Experience Patterns | — |

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/traceability*  
*License: CC BY 4.0 — Attribution required*

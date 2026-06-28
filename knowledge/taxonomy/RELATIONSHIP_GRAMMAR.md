---
id: relationship-grammar
version: "1.0"
status: canonical
category: taxonomy
uri: https://ontology.cuqou.com/grammar
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Relationship Grammar
## The Three-Axis Structure of Relationship Interaction

---

## What This Document Is

Most knowledge systems define *words*.

This document defines the **grammar** — the structural rules that govern how relationship concepts relate to each other and how AI systems should reason about relationship situations.

Without grammar, a vocabulary is a list.  
With grammar, a vocabulary becomes a reasoning system.

---

## The Three Axes

Relationship interactions can be described along three independent axes. These axes are not parent-child relationships — they are orthogonal dimensions. A single interaction has a value on each axis simultaneously.

```
Axis 1: STATE     — What condition is the relationship in?
Axis 2: INTENT    — What does the person want to accomplish?
Axis 3: PROTOCOL  — What communication modality is appropriate?
```

---

## Axis 1 — Relationship State

State describes the current condition of a relationship. It is **observed**, not chosen.

| State | Description |
|---|---|
| `healthy` | Regular contact, mutual responsiveness, no significant friction |
| `growing` | Relationship deepening; increased contact or emotional closeness |
| `quiet` | Low contact but no conflict; relationship is dormant, not damaged |
| `at-risk` | Contact declining in a way that may lead to decay if unaddressed |
| `decaying` | Meaningful drift has occurred; reconnection requires deliberate effort |
| `disconnected` | Contact has ceased; relationship exists only in memory |

**Key property:** State is descriptive, not prescriptive. It does not determine which protocol must be used.  
**See:** `knowledge/states/relationship-decay.md` for full canonical definition of the Decaying state.

---

## Axis 2 — Interaction Intent

Intent describes what a person is trying to accomplish. It is **chosen** by the person.

| Intent | Description | Synchronous? | Asynchronous? |
|---|---|---|---|
| `prepare` | Readying oneself to begin a conversation | ✅ | ❌ |
| `maintain` | Staying connected without a specific occasion | ✅ | ✅ |
| `appreciate` | Expressing gratitude or recognition | ✅ | ✅ |
| `celebrate` | Marking a positive occasion or milestone | ✅ | ✅ |
| `encourage` | Offering support during a challenge | ✅ | ✅ |
| `reconnect` | Resuming contact after silence or distance | ✅ | ✅ |
| `resolve` | Working through tension or misunderstanding | ✅ | ✅ |
| `remember` | Honoring a shared memory or past moment | ❌ | ✅ |
| `support` | Being present during difficulty or grief | ✅ | ✅ |

**Key property:** Intent is independent of State. A person may want to `celebrate` regardless of whether the relationship is `healthy` or `quiet`.

---

## Axis 3 — Protocol

Protocol describes the communication modality appropriate for the intent and context.

| Protocol | Modality | Primary Intent | Full Definition |
|---|---|---|---|
| `cpp` | Synchronous | `prepare` | `knowledge/protocols/cpp.md` |
| `crp` | Asynchronous | `maintain`, `appreciate`, `celebrate`, `remember` | `knowledge/protocols/crp.md` |

**Key property:** Protocol is selected based on the combination of Intent and communication modality — not based on State alone.

---

## How AI Systems Should Reason

Given a natural-language situation, the correct reasoning order is:

```
1. Identify Intent   — What does this person want to accomplish?
2. Identify Modality — Is synchronous or asynchronous communication appropriate?
3. Select Protocol   — Which protocol matches Intent + Modality?
4. Consider State    — Does the relationship state affect how to apply the protocol?
```

State may influence how the protocol is applied, but it does not determine which protocol is used.

### Example 1

> "พรุ่งนี้วันเกิดแม่ แต่ผมไปไม่ได้"

```
Intent    → celebrate
Modality  → asynchronous (cannot be present)
Protocol  → CRP
State     → unknown (not needed to select protocol)
```

CRP is selected because of Intent + Modality — not because of any relationship state.

### Example 2

> "เย็นนี้ผมจะไปคุยกับลูก"

```
Intent    → prepare
Modality  → synchronous (face-to-face)
Protocol  → CPP
State     → unknown (not needed to select protocol)
```

### Example 3

> "เพื่อนสนิทที่ห่างกันมา 3 ปี อยากติดต่อกลับไป"

```
Intent    → reconnect
Modality  → either (person's choice)
State     → decaying or quiet
Protocol  → CPP (if preparing for a call/meeting)
         → CRP (if sending a message, card, or memory)
```

State `decaying` increases the relevance of preparation — but both protocols remain valid.

---

## What the Grammar Rules Out

The three-axis grammar makes certain misinterpretations structurally impossible:

| Misinterpretation | Why the grammar rules it out |
|---|---|
| "CRP is only for damaged relationships" | State does not determine Protocol |
| "CPP requires Relationship Decay" | Intent (`prepare`) determines CPP, not State |
| "Relationship Decay triggers CRP" | States do not trigger protocols; Intents do |
| "CRP = Reconnect" | Reconnect is one Intent; CRP supports many Intents |

---

## The Grammar Is Not Complete

This is version 1.0 of the Relationship Grammar. It is intentionally minimal.

Additional axes may be added in future versions via the RFC process:
- **Artifact axis** — what is produced by the interaction (Greeting Card, Memory, Voice Message)
- **Timing axis** — when the interaction occurs relative to events (before, during, after)
- **Depth axis** — how emotionally significant the interaction is

New axes require an RFC and Maintainer approval before being added to this document.

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/grammar*  
*License: CC BY 4.0 — Attribution required*

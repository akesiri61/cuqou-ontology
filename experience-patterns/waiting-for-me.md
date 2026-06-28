---
id: waiting-for-me
version: "1.0"
status: canonical
category: experience-pattern
layer: 4
uri: https://ontology.cuqou.com/experience-patterns/waiting-for-me
license: CC BY 4.0 — Cuqou (https://cuqou.com)
reference_pattern: true
---

# Waiting For Me

> **Reference Experience Pattern** — the first canonical Experience Pattern in the Cuqou Relationship Ontology.  
> All future Experience Patterns follow the structure established here.

---

## Purpose

Surface the relationships that are waiting for a person's care — at the right moment, in a way that reduces hesitation rather than inducing guilt.

---

## Human Problem

People often delay caring for important relationships — not because they have stopped caring, but because nothing asks for their attention at the right moment.

The relationship stays in their mind as a vague intention: *"I should reach out sometime."*

That intention ages. It accumulates weight. The longer it waits, the harder it becomes to start. Not because the care is gone, but because the hesitation has grown.

The person is not neglectful. They are without a signal.

---

## Human Transformation

**Before:**
> *"I should contact my father someday. I've been meaning to for weeks. It feels harder the longer I wait."*

**After:**
> *"I know exactly who is waiting for my care. I can respond in my own words, today."*

The transformation is not about completing a task. It is about moving from a diffuse, heavy sense of relational obligation into a clear, actionable, and human moment of care.

When Waiting For Me works well, the person does not feel managed. They feel *reminded of who they are* — someone who cares.

---

## Tension

The problem persists because two real forces are in conflict:

```
The person genuinely cares about the relationship
            ↓
Life fills the available attention — no natural signal arrives
            ↓
The relationship goes quiet
            ↓
Guilt accumulates — starting feels increasingly weighted
            ↓
The hesitation itself becomes a barrier
            ↓
The person cares more, acts less
```

This is not a motivation problem. It is a signal problem.

The person does not need to be reminded that they care. They need a moment when the system says: *here is someone who matters to you, and here is a way to reach them today.*

---

## Resolution

**Surface only meaningful opportunities for care.**

Not a list of neglected contacts. Not a score of relationship health. Not a reminder that time has passed. Not a streak to maintain.

A moment. One person. A question: *do you want to reach out today?*

The system presents. The human decides. The system does not make the hesitation worse by measuring it.

**What this means in practice:**
- Show relationships where the person's care is most likely to matter
- Present one meaningful opportunity at a time, not an inbox of obligations
- Ask only: "Do you want to reach out?" — not "You haven't contacted them in 47 days"
- Surface the moment without explaining why the moment was selected
- Disappear once the person has acted or chosen not to

---

## Layer Dependencies

| Layer | Concept / Principle | Role in this pattern |
|---|---|---|
| 0 — Axiom | [Relationship Truth](../axioms/relationship-truth.md) | Every expression surfaced must be capable of carrying genuine human intent |
| 1 — Stewardship | [Human Agency](../knowledge/principles/human-agency.md) | The person chooses whether to act — WFM never initiates action on their behalf |
| 1 — Stewardship | [Human Contribution](../knowledge/concepts/human-contribution.md) | If the person reaches out, their words must be present in the expression |
| 1 — Stewardship | [Intent Provenance](../knowledge/concepts/intent-provenance.md) | The system surfaces the moment; the human decides to act |
| 2 — Language | [CRP](../knowledge/protocols/crp.md) | The most likely action from WFM is a CRP expression (async care signal) |
| 2 — Language | [CPP](../knowledge/protocols/cpp.md) | WFM may also surface a relationship where direct conversation is needed |
| 2 — Language | [State Taxonomy](../knowledge/taxonomy/state-taxonomy.md) | Relationship state informs which relationships surface and in what order |
| 2 — Language | [Intent Taxonomy](../knowledge/taxonomy/intent-taxonomy.md) | The system may suggest an intent (maintain, appreciate, reconnect) — the human confirms |
| 3 — Intelligence | [Decision Layer](../decision/DECISION_LAYER.md) | Selects which relationships to surface; applies constraints on what to recommend |
| 3 — Intelligence | [Constraint C003](../decision/constraints.yaml) | CPP does not require relationship decay — WFM may surface any meaningful moment |
| 3 — Intelligence | [Ethics E005](../ethics/rules.yaml) | No action is taken autonomously — WFM surfaces; it does not send |

---

## Flow Entry Point

Waiting For Me enters the Relationship Flow at the **Human Decision** stage.

```
[System detects a meaningful moment in a relationship]
            ↓
[WFM surfaces the opportunity — no action taken]
            ↓
Human Decision  ← The person enters the flow HERE
            ↓
Intent Provenance verified (the person chose to act)
            ↓
Intent (what do they want to do?)
            ↓
Decision (which protocol fits?)
            ↓
Protocol → Expression → Human Contribution → Human Agency → Medium → Send
```

The system's role ends at the surface. Everything after is the person's.

---

## Human Agency Check

- [x] The person can choose not to engage — WFM disappears if ignored or dismissed
- [x] The person has full control over whether any action results
- [x] No action reaches another person without explicit per-action human approval
- [x] The pattern presents one opportunity — it does not pressure, rank, or score

---

## Relationship Truth Check

- [x] The pattern does not manufacture obligation, expectation, or guilt
- [x] Human Contribution is required before any expression is sent
- [x] Intent Provenance is preserved — the person's decision to act is their own
- [x] AI surfaces the moment; AI does not make the relational decision
- [x] **Relationship Truth Review PASS:** WFM reduces friction to authentic human care. It does not increase convenience by replacing human intention.

---

## Anti-patterns

These are the failure modes that Waiting For Me must never become, regardless of product pressure:

| Anti-pattern | Why it violates the Resolution |
|---|---|
| **Task Manager** | Converts relationships into items to clear. Implies completion is the goal. Relationships are not tasks. |
| **Notification Feed** | Volume replaces meaning. When everything surfaces, nothing matters. The signal is lost in the noise. |
| **Streak Counter** | Gamifies regularity, not care. A person may have a 0-day streak and a deeply meaningful relationship. |
| **Relationship Score** | Reduces the complexity of a human relationship to a number. Positions the system as the judge of relationship quality. |
| **Guilt Engine** | Uses the passage of time to manufacture urgency. "You haven't contacted them in 47 days." This is not Cuqou. |
| **Obligation List** | Shows every relationship that could be attended to. Replaces the feeling of meaningful attention with the anxiety of an inbox. |

---

## What AI May Do

- Identify which relationships are most likely to benefit from attention at this moment
- Surface one relationship at a time — not a ranked list
- Suggest an intent once the person has chosen to act (maintain, appreciate, celebrate, reconnect)
- Offer a starting point for CRP or CPP once the person decides to proceed
- Help the person draft their own words after the intent is confirmed

---

## What AI Must Not Do

- Decide which relationship deserves the person's attention (AI surfaces; the human decides)
- Explain *why* it selected a relationship ("You haven't spoken in 47 days")
- Send any message, card, or signal autonomously
- Show multiple relationships simultaneously in a way that creates obligation pressure
- Assign a health score, relationship grade, or urgency indicator

---

## Success Criteria

Success is measured in human outcomes.

**Success is NOT:**
- More notifications opened
- More messages sent
- Higher session frequency
- Longer streaks

**Success IS:**
- **Reduced hesitation** — the person reaches out who previously would not have
- **Increased authentic care** — the person's words, not AI's, reach the other person
- **Preserved relationship continuity** — a relationship that was drifting is reconnected by human choice
- **No new guilt** — the person who does not act today does not feel worse for having seen WFM

The last criterion is as important as the first three. A person who dismisses Waiting For Me should feel neither judged nor reminded. They chose to attend to other things today. That is their right.

---

## Future Extensions

These extensions are consistent with the Resolution and do not violate the Anti-patterns:

- **Time-of-day awareness** — surface WFM when the person is most likely to have a quiet moment (evening, weekend morning)
- **Occasion-aware surfacing** — surface a relationship when a meaningful date is approaching (birthday, anniversary, shared memory)
- **Multi-channel delivery** — WFM may surface in the app, via LINE Digest, or via native widget — all using the same pattern
- **Intent suggestion** — once the person decides to act, the system suggests the most likely intent based on relationship context
- **CRP pre-fill** — suggest a Greeting Card or Memory as a starting point, with full human contribution required before sending

These extensions add capability. They do not change the Resolution: *surface only meaningful opportunities for care.*

---

## Related Patterns

- **Attention Layer** — the delivery system that brings WFM to the person's existing context (LINE, widget, email)
- **Daily Reflection** — a contemplative pattern for reviewing the state of meaningful relationships
- **Silent Reminder** — a lightweight pattern for relationships where presence matters more than words

---

## Related Concepts

- **[Relationship Truth](../axioms/relationship-truth.md)** — the Axiom this pattern serves
- **[Human Agency](../knowledge/principles/human-agency.md)** — who decides whether to act
- **[Human Contribution](../knowledge/concepts/human-contribution.md)** — whose voice reaches the other person
- **[Intent Provenance](../knowledge/concepts/intent-provenance.md)** — that the decision to act was human
- **[CRP](../knowledge/protocols/crp.md)** — the most likely protocol activated from this pattern
- **[CPP](../knowledge/protocols/cpp.md)** — also possible when direct conversation is the right next step
- **[RELATIONSHIP_FLOW.md](../RELATIONSHIP_FLOW.md)** — the flow this pattern enters and exits

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/experience-patterns/waiting-for-me*  
*License: CC BY 4.0 — Attribution required*

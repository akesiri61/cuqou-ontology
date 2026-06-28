---
version: "3.0"
status: canonical
uri: https://ontology.cuqou.com/experience-patterns/guide
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Experience Pattern Guide

## What Is an Experience Pattern?

An Experience Pattern describes the shape of a specific human experience within a relationship system.

It is not a feature. It is not a protocol. It is not a concept.

It answers two questions:

> **"What recurring human problem exists here?"**  
> **"When this experience ends, how has the human changed?"**

See: `PATTERN_LANGUAGE.md` for the philosophy behind this approach.

---

## Domain vs. Product

| | Domain (Layers 0–3) | Product (Layer 4) |
|---|---|---|
| What it describes | What is universally true about relationships | What a person experiences in a specific system |
| Uniqueness | One canonical definition per concept | Multiple Experience Patterns may apply the same Domain concepts |
| Examples | Relationship Truth, CPP, CRP, Human Agency | Waiting For Me, Daily Reflection, Silent Reminder |

Experience Patterns live at Layer 4. They *apply* Layers 0–3. They do not define them.

---

## The Relationship Truth Review

Before any Experience Pattern may become `canonical`, it must pass the Relationship Truth Review:

> **"Does this experience increase convenience at the expense of Relationship Truth?"**

If the answer is yes — the pattern does not become canonical, regardless of how useful it seems.

Convenience and Relationship Truth are not always in tension. Many patterns can be both convenient and authentic. But when they conflict, Relationship Truth takes precedence.

This review is not a checklist. It is a judgment call made by the Ontology Maintainer. The pattern author must make the case in the Human Agency Check and Relationship Truth Check fields.

---

## The Template

Every Experience Pattern must use this structure.

```markdown
---
id: [kebab-case-id]
version: "1.0"
status: [draft | proposed | canonical]
category: experience-pattern
layer: 4
uri: https://ontology.cuqou.com/experience-patterns/[id]
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# [Pattern Name]

## Purpose

One sentence: what this pattern is for.

---

## Human Problem

What recurring human situation does this pattern address?
Not a feature gap — the real human experience that leaves relationships
worse than they could be, again and again.

---

## Human Transformation

When this experience ends well, how has the human changed?

**Before:**
> "[Describe the person's state before encountering this pattern]"

**After:**
> "[Describe the person's state after the pattern resolves well]"

This is the measure of success. Not clicks, not retention — 
but the change in the human's relationship to the people they care about.

---

## Tension

What opposing forces create this problem?
Show the cycle or conflict that makes the problem persist.

```
[Force A]
    ↓
[What happens]
    ↓
[Force B]
    ↓
[What worsens]
```

---

## Resolution

How does this pattern resolve the tension?
Not a feature list — a philosophy.

What is the minimum intervention that resolves the tension
without creating new ones, and without sacrificing Relationship Truth?

---

## Layer Dependencies

Which layers this pattern relies on:

| Layer | Concept / Principle | Role in this pattern |
|---|---|---|
| 0 — Axiom | Relationship Truth | [how it applies] |
| 1 — Stewardship | Human Agency | [how it applies] |
| 1 — Stewardship | Human Contribution | [how it applies] |
| 1 — Stewardship | Intent Provenance | [how it applies] |
| 2 — Language | [Protocol / State / Intent] | [how it applies] |
| 3 — Intelligence | [Decision rule / Constraint] | [how it applies] |

---

## Flow Entry Point

Where does this pattern enter the Relationship Flow?
Reference: `RELATIONSHIP_FLOW.md`

```
[Which stage triggers this pattern, and where does the human re-enter the flow?]
```

---

## Human Agency Check

- [ ] The person can choose not to engage with this pattern
- [ ] The person has control over what action (if any) results
- [ ] No action reaches another person without explicit human approval
- [ ] The pattern presents information — it does not pressure action

---

## Relationship Truth Check

- [ ] The pattern does not manufacture obligation, expectation, or guilt
- [ ] Human Contribution is required before any expression is sent
- [ ] Intent Provenance is preserved — the person's decision to act is their own
- [ ] AI augments; it does not replace human intention
- [ ] **Relationship Truth Review:** This pattern does not increase convenience at the expense of Relationship Truth

---

## Anti-patterns

What must this experience never become?
Name the failure modes explicitly — these protect against
product drift under feature pressure.

| Anti-pattern | Why it violates the Resolution or Relationship Truth |
|---|---|
| [name] | [reason] |

---

## What AI May Do

What AI assistance is appropriate within this pattern.

---

## What AI Must Not Do

What would push this pattern toward its Anti-patterns.

---

## Success Criteria

Success is measured in human outcomes — not product metrics.

**Success is NOT:**
- [metric that would be measurable but wrong]

**Success IS:**
- [human outcome that reflects the Transformation]

---

## Future Extensions

What could this pattern become over time — without violating its Resolution or Anti-patterns?

---

## Related Patterns

Other Experience Patterns that share conditions, intents, or protocols with this one.

## Related Concepts

Links to the Domain concepts this pattern applies.
```

---

## How to Propose a New Experience Pattern

1. Identify the **Human Problem** — a recurring situation, not a feature gap
2. Write the **Human Transformation** — before/after in human terms
3. Name the **Tension** — the opposing forces that make the problem persist
4. Write the **Resolution** — the philosophy, not the implementation
5. Name the **Anti-patterns** — what this must never become
6. Trace all **Layer Dependencies** explicitly
7. Verify both checks pass: Human Agency + Relationship Truth
8. Verify the **Relationship Truth Review**: does this increase convenience at the expense of Relationship Truth?
9. Add to `CANONICAL_MAP.md` with `status: draft`
10. Submit for Maintainer review

---

## The First Canonical Pattern

The first Experience Pattern in the Cuqou ontology is **Waiting For Me** — the Reference Experience Pattern that proves Pattern Language works end-to-end.

See: `experience-patterns/waiting-for-me.md`

---

## Version History

| Version | Change |
|---|---|
| 1.0 | Initial guide with basic template |
| 2.0 | Template expanded with Pattern Language: Human Problem, Tension, Resolution, Anti-patterns |
| 3.0 | Human Transformation added; Success Criteria reframed as Human Outcome; Relationship Truth Review added as canonical gate |

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/experience-patterns/guide*  
*License: CC BY 4.0 — Attribution required*

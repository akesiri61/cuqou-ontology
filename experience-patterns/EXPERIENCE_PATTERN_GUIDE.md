---
version: "2.0"
status: canonical
uri: https://ontology.cuqou.com/experience-patterns/guide
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Experience Pattern Guide

## What Is an Experience Pattern?

An Experience Pattern describes the shape of a specific human experience within a relationship system.

It is not a feature. It is not a protocol. It is not a concept.

It answers: **"What recurring human problem exists here — and how should the system resolve it without losing Relationship Truth?"**

See: `PATTERN_LANGUAGE.md` for the philosophy behind this approach.

---

## Domain vs. Product

| | Domain (Layers 0–3) | Product (Layer 4) |
|---|---|---|
| What it describes | What is universally true about relationships | What a person experiences in a specific system |
| Uniqueness | One canonical definition per concept | Multiple Experience Patterns may apply the same Domain concepts |
| Examples | Relationship Truth, CPP, CRP, Human Agency | Waiting For Me, Daily Reflection, Silent Reminder |

Experience Patterns live at Layer 4. They *apply* Layers 0–3. They do not define them.

CPP has one canonical definition.  
CRP has one canonical definition.  
But five different Experience Patterns could all use CRP — each with a different human problem, trigger, and form.

---

## The Template

Every Experience Pattern must use this structure. The fields correspond to the seven elements of Pattern Language described in `PATTERN_LANGUAGE.md`.

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

## Human Problem

What recurring human situation does this pattern address?
Not a feature gap — the real human experience that leaves relationships
worse than they could be, again and again.

## Tension

What opposing forces create this problem?
Show the cycle or the conflict that makes the problem persist.

```
Force A
    ↓
[what happens]
    ↓
Force B
    ↓
[what worsens]
```

## Resolution

How does this pattern resolve the tension?
Not a feature list — a philosophy.
What is the minimum intervention that resolves the tension
without creating new ones?

The resolution must preserve both Relationship Truth
and human autonomy. It does not eliminate the tension
by eliminating one side of it.

---

## Purpose

One sentence: what this pattern is for.

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

## Flow Entry Point

Where does this pattern enter the Relationship Flow?

```
[Which stage in RELATIONSHIP_FLOW.md does this pattern trigger from?]
```

## Anti-patterns

What must this experience never become?
Name the failure modes explicitly — these protect against
product drift under feature pressure.

| Anti-pattern | Why it fails |
|---|---|
| [name] | [how it violates the Resolution or Relationship Truth] |

## Human Agency Check

- [ ] The person can choose not to engage with this pattern
- [ ] The person has control over what action (if any) results
- [ ] No action reaches another person without explicit human approval
- [ ] The pattern presents information — it does not pressure action

## Relationship Truth Check

- [ ] The pattern does not manufacture obligation, expectation, or guilt
- [ ] Human Contribution is required before any expression is sent
- [ ] Intent Provenance is preserved — the person's decision to act is their own
- [ ] AI augments; it does not replace human intention

## What AI May Do

What AI assistance is appropriate within this pattern.

## What AI Must Not Do

What would push this pattern toward its Anti-patterns.

## Success Criteria

How does a person feel when the pattern works well?
Not clicks or retention — the human experience of the tension being resolved.

## Related Patterns

Other Experience Patterns that share conditions, intents, or protocols.

## Related Concepts

Links to the Domain concepts this pattern applies.
```

---

## How to Propose a New Experience Pattern

1. Identify the **Human Problem** — a recurring situation, not a feature gap
2. Name the **Tension** — the opposing forces that make the problem persist
3. Write the **Resolution** — the philosophy, not the implementation
4. Name the **Anti-patterns** — what this must never become
5. Trace all **Layer Dependencies** explicitly
6. Verify both checks pass: Human Agency + Relationship Truth
7. Add to `CANONICAL_MAP.md` with `status: draft`
8. Submit for Maintainer review

A pattern becomes `canonical` when:
- The Human Problem is real and recurring
- The Tension is named clearly
- The Resolution preserves Relationship Truth
- Anti-patterns are named and principled
- All Layer Dependencies are explicit
- At least one reference implementation exists or is specced

---

## The First Canonical Pattern

The first Experience Pattern in the Cuqou ontology is **Waiting For Me** — the reference implementation for how a person should experience the moment when relationships are waiting for their attention.

See: `experience-patterns/waiting-for-me.md`

---

## Version History

| Version | Change |
|---|---|
| 1.0 | Initial guide with basic template |
| 2.0 | Template expanded with Pattern Language structure: Human Problem, Tension, Resolution, Anti-patterns |

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/experience-patterns/guide*  
*License: CC BY 4.0 — Attribution required*

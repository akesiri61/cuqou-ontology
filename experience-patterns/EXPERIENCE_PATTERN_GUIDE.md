---
version: "1.0"
status: canonical
uri: https://ontology.cuqou.com/experience-patterns/guide
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Experience Pattern Guide

## What Is an Experience Pattern?

An Experience Pattern describes the shape of a specific human experience within a relationship system.

It is not a feature. It is not a protocol. It is not a concept.

It is the answer to: **"What experience should a person have when a specific condition is true about their relationships?"**

---

## Domain vs. Product

The Cuqou Relationship Ontology distinguishes between:

| | Domain | Product |
|---|---|---|
| What it describes | What is universally true about relationships | What a person sees and uses in a specific system |
| Layers | 0 — Axiom, 1 — Stewardship, 2 — Language, 3 — Intelligence | 4 — Experience |
| Examples | Relationship Truth, CPP, CRP, Human Agency | Waiting For Me, Relationship Inbox, Daily Reflection |
| Uniqueness | One canonical definition | Multiple implementations possible |
| Changes when? | Almost never | Can evolve with product design |

Experience Patterns live at Layer 4. They *apply* Layers 0–3. They do not *define* them.

CPP has one canonical definition.  
CRP has one canonical definition.  
But a system could implement five different Experience Patterns that all use CRP — each with a different surface, trigger, and form.

---

## What Makes a Good Experience Pattern

A good Experience Pattern:

1. **Answers one clear experience question** — "What should a person experience when X is true?"
2. **Is reusable** — other systems or implementations could apply this pattern, not just Cuqou
3. **References the layers that govern it** — it is explicit about which principles, protocols, and decision rules apply
4. **Passes the Relationship Truth check** — the experience preserves human agency and contribution
5. **Has a clear success criterion** — how does the person feel when the pattern works well?

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

## Experience Question

> "What experience should a person have when [condition]?"

## One Sentence

What this pattern provides, in one sentence.

## The Condition

What must be true in the system for this pattern to be relevant.
This is observable state — not user action.

## The Experience Goal

What the person should feel or understand after encountering this pattern.
Not "they should click X" — but "they should feel Y" or "they should know Y."

## Layer Dependencies

Which layers this pattern relies on:

| Layer | Concept / Principle | Role in this pattern |
|---|---|---|
| 0 — Axiom | Relationship Truth | The pattern must preserve authentic human intent |
| 1 — Stewardship | [Principles used] | [How they apply] |
| 2 — Language | [Protocols / States / Intents] | [How they apply] |
| 3 — Intelligence | [Decision rules] | [How they apply] |

## Flow Entry Point

Where does this pattern enter the Relationship Flow?
Reference: `RELATIONSHIP_FLOW.md`

## Human Agency Check

- [ ] The person can choose not to engage with this pattern
- [ ] The person has control over what action (if any) results
- [ ] No action is taken without explicit human approval

## Relationship Truth Check

- [ ] The pattern does not manufacture obligation, expectation, or guilt
- [ ] The pattern presents information — it does not pressure action
- [ ] Human Contribution is required before any expression is sent
- [ ] Intent Provenance is preserved — the person's decision to act is their own

## What AI May Do in This Pattern

What AI assistance is appropriate within this pattern.

## What AI Must Not Do in This Pattern

What would violate the Stewardship Principles within this context.

## Success Criteria

How to know the pattern is working well:
- The person feels [Y] when they encounter this pattern
- The person is able to [Z] without [negative outcome]

## Related Patterns

Other Experience Patterns that share conditions, intents, or protocols with this one.

## Related Concepts

Links to the ontology concepts this pattern applies.
```

---

## How to Propose a New Experience Pattern

1. Verify the experience question cannot be answered by an existing pattern
2. Identify which Domain layers (0–3) the pattern depends on
3. Write the pattern using the template above with `status: draft`
4. Add to `CANONICAL_MAP.md` with `status: proposed`
5. Submit for Maintainer review

A pattern becomes `canonical` when:
- The experience question is clearly and uniquely defined
- All layer dependencies are explicit
- Both the Human Agency Check and Relationship Truth Check pass
- At least one reference implementation exists or is specced

---

## The First Canonical Pattern

The first Experience Pattern in the Cuqou ontology is **Waiting For Me** — the reference implementation for how a person should experience the discovery that relationships are waiting for their attention.

See: `experience-patterns/waiting-for-me.md`

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/experience-patterns/guide*  
*License: CC BY 4.0 — Attribution required*

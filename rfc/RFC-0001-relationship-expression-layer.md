---
rfc: "0001"
title: Relationship Expression Layer
status: accepted-modified
proposed_by: Founder
date: "2026-06-28"
affects:
  - crp
  - cpp
  - decision-layer
  - artifact-suggestion
  - intent-taxonomy
  - relationship-grammar
---

# RFC-0001 — Relationship Expression Layer

## Proposed Change

Replace the single `Artifact` concept with a two-level structure:

```
Intent → Protocol → Expression → Medium
```

Where:
- **Expression** is the form of relationship communication (Greeting, Memory, Encouragement, etc.)
- **Medium** is the specific channel or object (Greeting Card, Voice Memory, Future Letter, etc.)

---

## Canonical Question This RFC Addresses

> "When a person chooses CRP, what determines the form of the signal they send?"

Currently the ontology jumps from Protocol directly to specific artifacts (Greeting Card, Voice Memory). This RFC proposes an intermediate layer — Expression — that clarifies the *why* before selecting the *what*.

---

## One-Sentence Proposal

A Relationship Expression is an intentional form of relationship communication — the structured shape a relationship signal takes before a specific medium is chosen.

---

## Why Existing Terminology Is Insufficient

**The problem with "Artifact":**

An artifact is an object. The word implies a created thing — a card, a file, a message.

What Greeting Cards, Voice Memories, Future Letters, and Shared Memories have in common is not that they are objects. It is that they are *expressions* — intentional acts of communicating care within a relationship.

Naming them all "artifacts" treats them as outputs rather than as communicative acts. This is architecturally incorrect: the ontology should describe *what a person is doing* (expressing care), not *what object results* (an artifact).

**The problem with a flat artifact list:**

A flat list like `[greeting_card, voice_memory, future_letter, memory_surface]` implies these are all the same kind of thing. They are not.

- A Greeting Card and a Voice Greeting are both *Greetings* — the same Expression, different Mediums
- A Memory Card and a Voice Memory are both *Memory* expressions — same Expression, different Mediums
- A Future Letter and a Scheduled Voice Message are both *Future* expressions

Without the Expression layer, the Decision Layer must select directly from a flat list of mediums — losing the reasoning step that makes AI recommendations coherent.

---

## Canonical Independence Check

> If every Cuqou application disappeared tomorrow, would the concept of a Relationship Expression still be meaningful to someone studying or maintaining human relationships?

**Answer: Yes.**

Handwritten letters and postcards are Greetings. Photo albums and journals are Memory expressions. Recorded messages for future occasions are Future expressions. These expression forms exist across all human cultures, independent of any digital product.

The Expression layer names a pattern that already exists in human behavior — it does not invent one.

---

## Proposed Structure

### Layer 1 — Expression (new canonical category)

| Expression ID | Name | Description |
|---|---|---|
| `greeting` | Greeting | Expressing presence, warmth, or acknowledgment to someone |
| `memory` | Memory | Honoring or sharing a past experience |
| `encouragement` | Encouragement | Offering support, motivation, or presence during difficulty |
| `celebration` | Celebration | Marking a positive occasion or milestone |
| `gratitude` | Gratitude | Expressing thanks or appreciation |
| `apology` | Apology | Taking responsibility and seeking reconciliation |
| `future` | Future | A message or expression intended for a future moment |

### Layer 2 — Medium (existing artifacts, renamed and clarified)

| Medium ID | Parent Expression | Examples |
|---|---|---|
| `greeting_card` | greeting, celebration, gratitude | Digital or physical card |
| `voice_memory` | memory, encouragement, support | Recorded voice message |
| `memory_surface` | memory | Curated collection of shared moments |
| `future_letter` | future | Message to be received at a later time |
| `digital_gift` | celebration, gratitude | A purposeful digital object |

---

## Affected Existing Concepts

| Concept | How it is affected |
|---|---|
| `crp` | `produces_artifacts` field → `produces_expressions` + `supported_mediums` |
| `decision/artifact-suggestion.yaml` | Rename to `expression-selection.yaml` + add `medium-selection.yaml` |
| `relationship-grammar` | Add Expression and Medium to the grammar diagram |
| `intent-taxonomy` | Add Expression column to Intent × Protocol matrix |
| `CANONICAL_MAP.md` | Add Expression category; rename Artifacts section |

---

## Updated Decision Layer Flow

```
Step 1 — Protocol Selection   (intent + modality → protocol)
Step 2 — Expression Selection (intent + protocol → expression)
Step 3 — Medium Selection     (expression + context → medium)
```

Current `artifact-suggestion.yaml` handles Step 2 and Step 3 simultaneously.
After this RFC: split into `expression-selection.yaml` and `medium-selection.yaml`.

---

## Negative Definition (preliminary)

A Relationship Expression is NOT:
- A medium or channel (that is Medium, one layer below)
- An artifact in the traditional sense (a thing produced as a byproduct)
- A content type (text, audio, image — those describe the medium)
- A feature in a product (Expression is protocol-layer, not implementation-layer)

---

## Proposed Category

New category: `expression`  
(Sits between `protocol` and `medium` in the grammar)

Medium becomes a sub-taxonomy under Expression, not a standalone concept category.

---

## Implementation Plan (if accepted)

1. Add `expression` category to `CANONICAL_MAP.md`
2. Create `knowledge/expressions/` directory with one file per Expression
3. Create `vocabulary/` entries for each Expression (YAML)
4. Rename `decision/artifact-suggestion.yaml` → `decision/expression-selection.yaml`
5. Add `decision/medium-selection.yaml` for Step 3
6. Update `crp.yaml`: replace `produces_artifacts` with `produces_expressions` + `supported_mediums`
7. Update `relationship-grammar.md`: add Expression and Medium axes
8. Update `intent-taxonomy.md`: add Expression column

---

## Reviewer Notes

The proposed structure `Intent → Protocol → Expression → Medium` is architecturally correct.

However, it is missing the most important principle of Cuqou: **Human Voice Preservation**.

Every relationship communication produced through CPP or CRP must preserve an explicit opportunity for authentic human contribution. AI may recommend, assist, and organize — but must never become the speaker.

This principle must be added as an axis before Medium is selected.

## Decision

Status: **accepted-modified**  
Maintainer: Cuqou Founders  
Date: 2026-06-28

### Modification

The accepted structure is:

```
Intent → Protocol → Expression → Human Contribution → Medium
```

**Human Contribution** is added as a first-class layer between Expression and Medium.

This is not a UX requirement. It is an Ontology Principle.

Definition: Every meaningful relationship communication must preserve an authentic human contribution. AI may assist. AI must not replace the person's own expression.

### What this changes

- `RELATIONSHIP_GRAMMAR.md` — add Human Contribution axis
- `decision/` — add `human-contribution.yaml` constraint rules
- `knowledge/concepts/human-contribution.md` — new canonical concept
- `CANONICAL_MAP.md` — add to Core Concepts
- `FOUNDER_DECISIONS.md §25` — Human Voice Preservation (Tier 0)

### What remains unchanged from the original proposal

- Expression layer is accepted
- Medium taxonomy is accepted
- The 3-step → 5-step Decision Layer expansion is accepted
- All concept names (Expression, Medium) are accepted

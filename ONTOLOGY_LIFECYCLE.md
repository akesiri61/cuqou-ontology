# Cuqou Ontology — Concept Lifecycle

**Version:** 1.0  
**Status:** Canonical

This document defines the lifecycle of a concept from initial idea to canonical status, and the conditions under which a concept may be deprecated or archived.

---

## Lifecycle Stages

```
Idea
 │
 ▼
Draft
 │
 ▼  ← Canonicalization Gate (all 4 checks must pass)
Proposed
 │
 ▼
Canonical
 │
 ▼  ← only with documented replacement
Deprecated
 │
 ▼
Archived
```

---

## Stage 1 — Idea

**What it is:** An observation that a concept may be worth naming.

**Who can propose:** Anyone — founders, contributors, researchers, AI agents.

**What is required:**
- A working name
- One sentence describing what the concept addresses
- The Canonical Question it answers

**What is NOT required at this stage:** Full definition, examples, or structured metadata.

**How to record:** Add a row to `CANONICAL_MAP.md` with status `draft`.

---

## Stage 2 — Draft

**What it is:** A concept under active development. The maintainer is writing the files.

**Files being created:**
- `vocabulary/{id}.yaml` (partial)
- `knowledge/{category}/{id}.md` (in progress)

**Status in CANONICAL_MAP:** `draft`

No external systems should reference draft concepts. A draft may change significantly or be abandoned.

---

## Stage 3 — Proposed

**What it is:** The concept author believes the concept is ready for canonicalization. All required files are complete.

**Files required before proposing:**
- [ ] `vocabulary/{id}.yaml` — complete with all required fields
- [ ] `knowledge/{category}/{id}.md` — canonical definition complete
- [ ] `knowledge/{category}/{id}.reasoning.md` — design history written
- [ ] `knowledge/{category}/{id}.examples.md` — at least 2 examples
- [ ] `schema/{id}.schema.json` — validation schema
- [ ] `exports/{id}.jsonld` — JSON-LD export

**Status in CANONICAL_MAP:** `proposed`

---

## Canonicalization Gate

A proposed concept becomes canonical only after passing **all 4 checks**:

### Check 1 — Constitution compliance
> Does this concept comply with all 9 principles of the CONSTITUTION.md?

Required: scope boundary (P1), naming authority (P4), human readability (P5), machine readability (P6).

### Check 2 — Canonical Concept Test
> Does this concept answer one enduring human problem, remain meaningful without any specific product, and is it defined clearly enough that both humans and AI interpret it consistently?

All three conditions must be true.

### Check 3 — Negative Definition completeness
> Does the concept clearly define what it is NOT?

Required: at least 5 items with reasons in the Negative Definition table.

### Check 4 — Canonical Independence
> Would this concept be meaningful and useful to someone studying or maintaining human relationships if every Cuqou application ceased to exist?

Required: explicit "yes" answer documented in the concept file.

### Approval
The Cuqou Ontology Maintainer reviews the 4 checks and changes status to `canonical`.

No automated process may change a concept status to `canonical`.

---

## Stage 4 — Canonical

**What it is:** The concept is officially part of the Cuqou Relationship Ontology.

**Rules:**
- The Concept ID never changes
- The definition may be refined through versioning (minor version: clarification, major version: significant change)
- All changes must be documented in the concept's change history
- External systems may safely reference canonical concepts

**Status in CANONICAL_MAP:** `canonical`

---

## Stage 5 — Deprecated

**What it is:** The concept is no longer recommended for use. It has been superseded by a more precise or better-named concept.

**When to deprecate:**
- A more precise concept covers the same problem
- The concept was found to violate the Canonical Independence Test after canonicalization
- The concept definition was found to be ambiguous in practice

**Rules:**
- Deprecation MUST document the replacement concept
- Deprecated concepts remain readable — they are never deleted
- External references to deprecated concepts remain valid but should migrate to the replacement

**Files updated on deprecation:**
- `vocabulary/{id}.yaml`: status → `deprecated`, add `replaced_by` field
- `knowledge/{category}/{id}.md`: add deprecation notice at the top
- `CANONICAL_MAP.md`: update status

**Status in CANONICAL_MAP:** `deprecated`

---

## Stage 6 — Archived

**What it is:** The concept has been deprecated long enough that active migration is complete. It is preserved for historical reference only.

**Rules:**
- Archived concepts are read-only
- No new references should be created to archived concepts
- The files remain in the repository

**Status in CANONICAL_MAP:** `archived`

---

## Versioning

Every canonical concept has a version number in `{major}.{minor}` format.

| Change type | Version increment | Example |
|---|---|---|
| Clarification of wording without changing meaning | Minor | 1.0 → 1.1 |
| Addition of new FAQ, examples, or LLM hints | Minor | 1.0 → 1.1 |
| Change to the canonical question or one-sentence definition | Major | 1.0 → 2.0 |
| Change to the scope or core meaning | Major | 1.0 → 2.0 |
| Correction of factual error | Minor | 1.0 → 1.1 |

All version changes MUST be documented in the concept's reasoning file under a `## Change History` section.

---

## Registry

The `CANONICAL_MAP.md` is the authoritative registry of all concepts and their current status.

Future: when the number of canonical concepts exceeds 20, a machine-readable registry (`registry.yaml`) will be generated from the vocabulary files.

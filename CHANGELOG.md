# Cuqou Relationship Ontology — Changelog

This file records every significant change to the ontology: concepts added, promoted, deprecated, or redefined. It is the authoritative history of how the Cuqou Relationship Ontology has evolved.

Format: each entry records what changed, why it changed, and what was affected.

---

## v0.4.0 — *pending* (CRP Canonicalization)

*To be filled when CRP is promoted to canonical.*

---

## v0.3.1 — 2026-06-28

**Canonical Source Rule added to CONSTITUTION.md**

`cuqou-ontology` is now formally declared the sole canonical source for all relationship concept definitions. Other repositories may reference but must not redefine canonical concepts.

**Affected:** All repositories in the Cuqou ecosystem.

---

## v0.3.0 — 2026-06-28

**Meta Ontology established (Sprint 2.5)**

Added governance infrastructure:
- `STYLE_GUIDE.md` — writing standards for all concept files
- `ONTOLOGY_LIFECYCLE.md` — 6-stage lifecycle with Canonicalization Gate
- `RFC_PROCESS.md` — RFC process for new concept proposals
- `templates/` — concept, reasoning, and examples templates

**Impact:** All future concepts use the Blueprint. CRP will be the first concept canonicalized under the full process.

---

## v0.2.1 — 2026-06-28

**Ontology Alignment Sprint (ADR-0086)**

Aligned 142 documentation files across `Cuqou Project` and `cuqou-mvp` with canonical definitions.

Key alignment:
- **CRP** — corrected scope from "conflict resolution only" to "asynchronous relationship communication for maintenance, appreciation, and reconnection"
- **Relationship Decay** — corrected from "CRP trigger" to "Relationship State"
- **cpp.md** — corrected CRP description that incorrectly described it as mid-conversation

Files changed: 8. ADRs added: 1 (ADR-0086).

---

## v0.2.0 — 2026-06-28

**CPP canonicalized — first canonical concept (Reference Implementation)**

Conversation Preparation Protocol (CPP) v1.0 promoted to `canonical`.

Files created:
- `vocabulary/cpp.yaml` — Machine Truth
- `knowledge/protocols/cpp.md` — Human Truth
- `knowledge/protocols/cpp.reasoning.md` — Design History
- `knowledge/protocols/cpp.examples.md` — Real-world examples
- `schema/cpp.schema.json` — Validation schema
- `exports/cpp.jsonld` — JSON-LD for AI/Search

**Canonical Question:** "How should I prepare before starting a conversation that matters?"

**Canonical Independence confirmed:** Applicable by therapists, coaches, HR professionals, teachers, researchers, and individuals — without any Cuqou product.

**Canonical Concept Test** added to CONSTITUTION.md:
> *A canonical concept should answer one enduring human problem, remain meaningful without any specific product, and be defined clearly enough that both humans and AI interpret it consistently.*

---

## v0.1.0 — 2026-06-28

**Foundation established**

Repository created with:
- `MANIFESTO.md` — philosophy: why Cuqou names relationship concepts
- `CONSTITUTION.md` — 9 principles governing canonical concepts
- `CANONICAL_MAP.md` — index of 14 proposed concepts across 5 categories
- `README.md` — North Star statement + structure guide
- `LICENSE` — CC BY 4.0
- `CITATION.cff` — standard citation format

**North Star declared:**
> *This repository does not define software features. It defines enduring concepts about maintaining meaningful human relationships. Applications may change. AI models may change. Technologies may change. The ontology should remain.*

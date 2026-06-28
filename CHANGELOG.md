# Cuqou Relationship Ontology — Changelog

This file records every significant change to the ontology: concepts added, promoted, deprecated, or redefined. It is the authoritative history of how the Cuqou Relationship Ontology has evolved.

Format: each entry records what changed, why it changed, and what was affected.

---

## v1.0.0 — 2026-06-28

**The First Canonical Experience Pattern Has Been Established**

`waiting-for-me.md` — Reference Experience Pattern for the Cuqou Relationship Ontology.

This version marks the completion of the ontology's foundational architecture. Every layer is now present and populated:

| Layer | What it contains |
|---|---|
| 0 — Axiom | Relationship Truth |
| 1 — Stewardship | Human Agency, Human Contribution, Intent Provenance |
| 2 — Language | CPP, CRP, Grammar, States, Intents |
| 3 — Intelligence | Decision Layer, Constraints, Ethics |
| Architecture | ARCHITECTURE_OF_RELATIONSHIP.md |
| Flow | RELATIONSHIP_FLOW.md |
| Pattern Language | PATTERN_LANGUAGE.md |
| 4 — Experience | Waiting For Me (Reference Pattern) |

**Waiting For Me — canonical:**
- Human Problem: people delay care not because they stopped caring, but because no signal arrives at the right moment
- Human Transformation: from "I should contact them someday" to "I know who is waiting, I can respond today"
- Tension: caring → no signal → silence → guilt → more silence
- Resolution: surface only meaningful opportunities for care. Never induce guilt. Never gamify neglect.
- Anti-patterns: Task Manager, Notification Feed, Streak Counter, Relationship Score, Guilt Engine, Obligation List
- Relationship Truth Review: PASS

**EXPERIENCE_PATTERN_GUIDE.md v3.0:**
- Human Transformation field added
- Success Criteria reframed as Human Outcome (not product metric)
- Relationship Truth Review established as canonical gate for all future patterns

All future Experience Patterns (Attention Layer, Silent Reminder, Daily Reflection, Relationship Inbox) will follow the structure established by this Reference Pattern.

---

## v0.7.0 — 2026-06-28

**Relationship Truth + Intent Provenance — Root Principles of the Ontology**

Two canonical concepts added that form the philosophical foundation from which all other concepts derive.

Concepts promoted to `canonical`:
- `relationship-truth` — the root principle: expressions must faithfully represent authentic human intention, regardless of how much technology assists
- `intent-provenance` — the traceability of a relationship expression's intent to a genuine human decision; must be verified before Protocol selection

**Relationship Authenticity Crisis** defined: not a technical failure, but a failure of human trust infrastructure — arising when recipients cannot know whether a human or AI sent a message.

**Cuqou as Trust Infrastructure** established: Cuqou does not prohibit AI assistance; it provides the structural commitment that every meaningful expression within the ecosystem remains traceable to genuine human intent.

Grammar extended:
- `RELATIONSHIP_GRAMMAR.md` updated: Intent Provenance added as a structural prerequisite check before the three-axis Grammar begins
- Full expression flow documented: Human Decision → Intent Provenance → Intent → Protocol → Expression → Human Contribution → Medium → Send

FOUNDER_DECISIONS §25.6 added:
> "The purpose of Cuqou is not to automate relationships. The purpose of Cuqou is to preserve the authenticity of relationships in the age of AI."

MANIFESTO.md updated:
- "Cuqou as Trust Infrastructure" section added (HTTPS/Git analogy)
- Relationship Truth and Intent Provenance introduced as the mechanism behind the civilizational purpose

Files added:
- `knowledge/concepts/relationship-truth.md` — canonical
- `knowledge/concepts/intent-provenance.md` — canonical

Files updated:
- `CANONICAL_MAP.md` — relationship-truth and intent-provenance added as canonical Core Concepts
- `knowledge/taxonomy/RELATIONSHIP_GRAMMAR.md` — Intent Provenance + full expression flow
- `MANIFESTO.md` — Trust Infrastructure section
- `FOUNDER_DECISIONS.md §25.6` — civilizational purpose declaration

---

## v0.5.0 — *pending* (CRP Canonicalization)

*To be filled when CRP is promoted to canonical.*

---

## v0.4.5 — 2026-06-28

**Relationship Grammar established — three-axis taxonomy**

Added the structural layer that governs how all concepts in the ontology relate to each other.

Three axes defined:
- **State** — what condition the relationship is in (observed)
- **Intent** — what the person wants to accomplish (chosen)
- **Protocol** — which communication modality is appropriate (derived from Intent + context)

Files added:
- `knowledge/taxonomy/RELATIONSHIP_GRAMMAR.md` — grammar with AI reasoning examples
- `knowledge/taxonomy/intent-taxonomy.md` — 9 intents with Intent × Protocol matrix and LLM hints
- `knowledge/taxonomy/state-taxonomy.md` — 6 states with transition model

**Key structural correction this grammar formalizes:**
- State does NOT determine Protocol
- Relationship Decay does NOT trigger CRP
- CRP supports many Intents (`celebrate`, `maintain`, `appreciate`, `remember`, etc.) — not only `reconnect`
- Intent + Modality → Protocol is the correct reasoning order for AI systems

**Impact:** CRP (v0.5.0) will be the first concept that formally references the taxonomy rather than explaining its own scope internally.

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

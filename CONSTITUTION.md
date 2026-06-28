# Cuqou Relationship Ontology — Constitution

**Version:** 1.0  
**Status:** Canonical  
**Maintainer:** Cuqou Ontology Maintainer  
**Last Updated:** 2026-06-28

---

## Purpose

The purpose of this Constitution is to define the principles governing the Cuqou Relationship Ontology.

It does not define every concept.  
It defines **what is allowed to become a canonical concept** — and what is not.

---

## Principle 1 — Scope Boundary

Cuqou does not attempt to define every aspect of human relationships.

Cuqou defines only concepts that help people **maintain, restore, or strengthen meaningful relationships**.

**Outside scope:**
- Psychology in general
- Personality theories
- Romance advice
- Parenting theories
- Philosophy unrelated to relationship maintenance

**Inside scope:**
- Communication preparation
- Relationship attention
- Relationship memory
- Relationship continuity
- Relationship recovery
- Meaningful interaction

The ontology describes the **mechanics of maintaining relationships** — not every aspect of human emotion.

---

## Principle 2 — Canonical Ownership

Every canonical concept has **exactly one canonical definition**.

Concepts may be proposed by founders, contributors, researchers, or AI assistants.

However, a concept becomes Canonical **only after explicit approval** by the Cuqou Ontology Maintainer.

Canonical concepts must never be silently modified.  
All changes must be versioned and logged.

---

## Principle 3 — Versioning

Concepts evolve. Definitions may become more precise over time.

Each concept therefore has:

- **Concept ID** — permanent, never changes
- **Version** — increments with each approved change
- **Status** — `draft` | `proposed` | `canonical` | `deprecated`
- **Change History** — log of every version change with rationale

Older versions remain referenceable.  
The Concept ID never changes. Only the version changes.

---

## Principle 4 — Naming Authority

Cuqou introduces new terminology **only when all of the following are true:**

1. The concept cannot be expressed precisely using existing terminology.
2. The concept appears repeatedly across multiple relationship situations.
3. The concept improves communication between humans, or between humans and AI.
4. The concept has a stable definition independent of any specific product implementation.

**What is not ontology:**
- Feature names
- UI labels
- Marketing slogans
- Temporary product terms

Only **reusable conceptual language** belongs to the ontology.

---

## Principle 5 — Human First

Every canonical concept must be understandable by a human reader without requiring technical knowledge.

Machine-readable representations exist to support interoperability — not to replace human understanding.

**Human meaning is the primary source of truth.**

---

## Principle 6 — Machine Readability

Every canonical concept must also expose structured metadata.

Structured representations may include:
- YAML (vocabulary layer)
- JSON / JSON-LD
- Schema.org
- RDF
- MCP Resources
- Embeddings

These representations are **derived from** the canonical concept and must never redefine its meaning.

---

## Principle 7 — Separation of Layers

The ontology consists of separate but connected layers.

| Layer | Responsibility |
|---|---|
| **Vocabulary** | Defines identifiers and structured metadata |
| **Knowledge** | Explains concepts in human language |
| **Articles** | Communicates ideas to general audiences |
| **Implementations** | Applies concepts in specific products |

Each layer has a distinct responsibility and must not duplicate another.  
The Knowledge layer does not replace the Vocabulary layer.  
The Article layer does not replace the Knowledge layer.

---

## Principle 8 — Stability

Canonical concepts are expected to remain stable **over many years**.

Applications may change.  
User interfaces may change.  
AI models may change.

The ontology should remain meaningful **regardless of implementation technology**.

This stability is one of Cuqou's core long-term assets.

---

## Principle 9 — Canonical Independence

Many canonical concepts originate inside products, research projects, or software implementations.  
Their origin does not determine their eligibility.

A concept becomes eligible for the Cuqou Ontology **only when it can be defined independently** of any specific application, platform, interface, or implementation.

### The Canonical Independence Test

> *"If every Cuqou application disappeared tomorrow, would this concept still be meaningful and useful to someone studying or maintaining human relationships?"*

- If **yes** → the concept may become canonical.
- If **no** → it remains a product term, not an ontology concept.

The ontology preserves **enduring ideas**, not temporary implementations.

---

## Canonical Concept Test

Before any concept is accepted as canonical, it must satisfy the following test:

> *A canonical concept should answer one enduring human problem, remain meaningful without any specific product, and be defined clearly enough that both humans and AI interpret it consistently.*

This test supersedes all other considerations. A concept that fails any of the three conditions — enduring problem, product independence, consistent interpretability — is not ready for canonicalization regardless of how useful it appears in the current context.

---

## Canonical Source Rule

This repository is the **sole canonical source** for all relationship concepts defined herein.

All other repositories — including `cuqou-mvp`, `cuqou-web`, `cuqou-miniapp`, product specs, ADRs, MCP Servers, and any future projects — MAY reference or implement these concepts, but MUST NOT redefine them.

If a discrepancy exists between this repository and any other source, `cuqou-ontology` is authoritative.

This rule applies to all concepts with status `canonical` in `CANONICAL_MAP.md`.

---

## Amendment Process

This Constitution may be amended only by the Cuqou Ontology Maintainer, with explicit rationale documented in the change history.

No agent, contributor, or automated system may modify this Constitution without explicit human authorization.

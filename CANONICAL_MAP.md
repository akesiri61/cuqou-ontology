# Canonical Map
## Cuqou Relationship Ontology — Index of Canonical Concepts

**Version:** 1.0  
**Status:** Canonical  
**Last Updated:** 2026-06-28

This map is the authoritative index of all concepts that belong — or are proposed to belong — to the Cuqou Relationship Ontology.

Before writing any concept file, verify the concept appears here with status `canonical` or `proposed`.  
Concepts not listed here are not part of the ontology.

---

## Architecture

The ontology is organized into four layers. Each concept belongs to exactly one layer.

```
Layer 0 — Axiom         — The foundational principle all other layers serve
Layer 1 — Stewardship   — Principles that govern AI behavior within the ecosystem
Layer 2 — Language      — Vocabulary: protocols, grammar, states, intents
Layer 3 — Intelligence  — Reasoning: decision rules, constraints, recommendations
Layer 4 — Experience    — What people see and use: patterns, surfaces, artifacts
```

See: `ARCHITECTURE_OF_RELATIONSHIP.md`

## Categories

```
Axioms            — The foundational principle (Layer 0)
Stewardship       — Governing principles for AI behavior (Layer 1)
Taxonomy          — The grammar: axes that govern how all concepts relate (Layer 2)
Protocols         — How to act within relationships (Layer 2)
Concepts          — What exists in relationships (Layer 2)
States            — Conditions a relationship can be in (Layer 2)
Decision          — Reasoning rules and constraints (Layer 3)
Experience        — Patterns, surfaces, and artifacts (Layer 4)
```

---

## Axioms (Layer 0)

The Foundational Axiom — all other concepts derive their purpose from this.

| ID | Name | Status | File |
|---|---|---|---|
| `relationship-truth` | Relationship Truth | `axiom` | `axioms/relationship-truth.md` |

---

## Stewardship Principles (Layer 1)

Principles that govern how AI operates within the ecosystem. These protect the Axiom.

| ID | Name | Thai | Status | File |
|---|---|---|---|---|
| `human-agency` | Human Agency | อำนาจในการตัดสินใจของมนุษย์ | `canonical` | `knowledge/principles/human-agency.md` |
| `human-contribution` | Human Contribution | การมีส่วนร่วมของมนุษย์ | `canonical` | `knowledge/concepts/human-contribution.md` |
| `intent-provenance` | Intent Provenance | ที่มาของเจตนา | `canonical` | `knowledge/concepts/intent-provenance.md` |

---

## Taxonomy (Layer 2)

The grammar layer that defines axes and classification systems. Concepts in other categories reference the taxonomy — not the reverse.

| ID | Name | Status | File |
|---|---|---|---|
| `relationship-grammar` | Relationship Grammar | `canonical` | `knowledge/taxonomy/RELATIONSHIP_GRAMMAR.md` |
| `intent-taxonomy` | Interaction Intent Taxonomy | `canonical` | `knowledge/taxonomy/intent-taxonomy.md` |
| `state-taxonomy` | Relationship State Taxonomy | `canonical` | `knowledge/taxonomy/state-taxonomy.md` |

---

## Concepts (Layer 2)

Fundamental ideas about the nature of relationships.

| ID | Name | Thai | Status | File |
|---|---|---|---|---|
| `relationship` | Relationship | ความสัมพันธ์ | `proposed` | `knowledge/concepts/relationship.md` |
| `attention` | Attention | ความสนใจ / การให้ความใส่ใจ | `proposed` | `knowledge/concepts/attention.md` |
| `memory` | Relationship Memory | ความทรงจำในความสัมพันธ์ | `proposed` | `knowledge/concepts/memory.md` |
| `silence` | Silence | ความเงียบ | `proposed` | `knowledge/concepts/silence.md` |
| `meaning` | Meaning | ความหมาย | `proposed` | `knowledge/concepts/meaning.md` |

---

## Protocols

Named methods for navigating specific relationship challenges.

| ID | Name | Thai | Status | File |
|---|---|---|---|---|
| `cpp` | Conversation Preparation Protocol | โปรโตคอลการเตรียมบทสนทนา | `canonical` | `knowledge/protocols/cpp.md` |
| `crp` | Conversation Resolution Protocol | โปรโตคอลการส่งสัญญาณความสัมพันธ์ | `canonical` | `knowledge/protocols/crp.md` |

---

## States (Layer 2)

Conditions a relationship can enter or exist in.

| ID | Name | Thai | Status | File |
|---|---|---|---|---|
| `waiting-for-me` | Waiting For Me | กำลังรอฉัน | `proposed` | `knowledge/states/waiting-for-me.md` |
| `relationship-decay` | Relationship Decay | การเสื่อมถอยของความสัมพันธ์ | `proposed` | `knowledge/states/relationship-decay.md` |

---

## Experience Patterns (Layer 4)

What people see and use. Each Experience Pattern draws on Layers 0–3.  
All patterns must follow `experience-patterns/EXPERIENCE_PATTERN_GUIDE.md`.

| ID | Name | Thai | Status | File |
|---|---|---|---|---|
| `waiting-for-me` | Waiting For Me | กำลังรอฉัน | `canonical` | `experience-patterns/waiting-for-me.md` |
| `attention-layer` | Attention Layer | ชั้นความใส่ใจ | `proposed` | `experience-patterns/attention-layer.md` |
| `greeting-card` | Greeting Card | การ์ดทักทาย | `proposed` | `experience-patterns/greeting-card.md` |
| `memory-surface` | Memory Surface | พื้นที่ความทรงจำ | `proposed` | `experience-patterns/memory-surface.md` |

---

## Status Definitions

| Status | Meaning |
|---|---|
| `draft` | Being written — not yet proposed for review |
| `proposed` | Complete draft submitted for Maintainer review |
| `canonical` | Approved — this is the official definition |
| `deprecated` | No longer canonical — see replacement concept |

---

## Proposing a New Concept

Before proposing a new concept, verify it passes all of the following:

- [ ] Passes the **Scope Boundary** (Constitution Principle 1)
- [ ] Passes the **Naming Authority** test (Constitution Principle 4) — cannot be expressed by existing terminology
- [ ] Passes the **Canonical Independence Test** (Constitution Principle 9) — meaningful without any Cuqou product

Submit proposal by adding the concept to this map with status `draft` and creating the concept file.  
The Cuqou Ontology Maintainer will review and change status to `canonical` upon approval.

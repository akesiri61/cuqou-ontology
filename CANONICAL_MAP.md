# Canonical Map
## Cuqou Relationship Ontology — Index of Canonical Concepts

**Version:** 1.0  
**Status:** Canonical  
**Last Updated:** 2026-06-28

This map is the authoritative index of all concepts that belong — or are proposed to belong — to the Cuqou Relationship Ontology.

Before writing any concept file, verify the concept appears here with status `canonical` or `proposed`.  
Concepts not listed here are not part of the ontology.

---

## Categories

```
Core Concepts     — What exists in relationships (nouns)
Protocols         — How to act within relationships (methods)
States            — Conditions a relationship can be in
Artifacts         — Things produced within relationships
Systems           — Architectures that support relationships
```

---

## Core Concepts

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
| `cpp` | Conversation Preparation Protocol | โปรโตคอลการเตรียมบทสนทนา | `proposed` | `knowledge/protocols/cpp.md` |
| `crp` | Conversation Resolution Protocol | โปรโตคอลการแก้ไขบทสนทนา | `proposed` | `knowledge/protocols/crp.md` |

---

## States

Conditions a relationship can enter or exist in.

| ID | Name | Thai | Status | File |
|---|---|---|---|---|
| `waiting-for-me` | Waiting For Me | กำลังรอฉัน | `proposed` | `knowledge/states/waiting-for-me.md` |
| `relationship-decay` | Relationship Decay | การเสื่อมถอยของความสัมพันธ์ | `proposed` | `knowledge/states/relationship-decay.md` |

---

## Artifacts

Tangible or digital objects produced within a relationship context.

| ID | Name | Thai | Status | File |
|---|---|---|---|---|
| `greeting-card` | Greeting Card | การ์ดทักทาย | `proposed` | `knowledge/artifacts/greeting-card.md` |
| `memory-surface` | Memory Surface | พื้นที่ความทรงจำ | `proposed` | `knowledge/artifacts/memory-surface.md` |

---

## Systems

Architectural frameworks that organize how attention and meaning flow within relationships.

| ID | Name | Thai | Status | File |
|---|---|---|---|---|
| `attention-layer` | Attention Layer | ชั้นความใส่ใจ | `proposed` | `knowledge/systems/attention-layer.md` |
| `hros` | Human Relationship OS | ระบบปฏิบัติการความสัมพันธ์มนุษย์ | `proposed` | `knowledge/systems/hros.md` |
| `relationship-room` | Relationship Room | ห้องความสัมพันธ์ | `proposed` | `knowledge/systems/relationship-room.md` |

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

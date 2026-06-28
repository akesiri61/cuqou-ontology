---
id: crp
document: reasoning
version: "1.0"
date: "2026-06-28"
author: Cuqou Founders
---

# CRP — Design History and Reasoning

---

## Why "Resolution" and not other words

"Resolution" was locked as canonical terminology deliberately. Several alternatives were considered:

| Word considered | Why it was rejected |
|---|---|
| **Reconnection** | Too narrow — implies a broken or distant relationship. CRP is used for celebration and maintenance too. |
| **Response** | Implies CRP is reactive (triggered by something). CRP can be proactive. |
| **Relationship Signal Protocol** | More descriptive, but loses the parallel structure with CPP. |
| **Reach-out Protocol** | Colloquial. Does not carry the precision a canonical term requires. |
| **Async Protocol** | Describes the modality, not the function. |
| **Care Protocol** | Too vague. Does not differentiate from general communication. |

**"Resolution" was retained because:**
- It captures the idea of bringing something to a meaningful state — not necessarily fixing a problem, but completing an act of care
- It maintains structural parallel with CPP (Preparation → Resolution: the two moves in relationship communication)
- It was already established in early Cuqou documentation and changing it would break historical references
- It is neutral enough to apply to all nine intents

The meaning of "Resolution" in CRP is not "conflict resolution." It is "bringing a relational moment to meaningful completion through an asynchronous act."

---

## Why CRP is not defined by Relationship State

Early versions of CRP were described as a response to Relationship Decay — "what you do when the relationship has drifted." This definition was rejected for two reasons:

**1. It is empirically wrong.** Greeting Cards, voice memories, and meaningful asynchronous messages are sent in healthy relationships, growing relationships, and quiet relationships — not only decaying ones. Defining CRP by decay excluded the majority of its actual use cases.

**2. It creates harmful AI reasoning.** If CRP is associated with decay, an AI system will suggest CRP primarily when it detects relationship problems. This is the opposite of proactive relationship maintenance — which is Cuqou's primary purpose.

The canonical definition removes all state dependencies. Relationship state is context that may influence *how* CRP is applied. It does not determine *when* CRP is applicable.

---

## Why "asynchronous communication" and not "messaging"

"Messaging" implies a text channel. CRP is not limited to text.

CRP is defined as asynchronous communication because the defining characteristic is temporal — the sender and receiver are not present at the same moment. The form (text, voice, image, video, physical card) is a choice made within CRP, not part of CRP's definition.

This keeps the canonical definition applicable to:
- Digital messaging
- Voice recordings
- Physical cards and letters
- Curated memory collections
- Future letters
- Any asynchronous form that has not yet been invented

---

## The relationship between CPP and CRP

CPP and CRP are not opposites. They are parallel protocols covering the two communication modalities.

```
CPP = synchronous modality → preparation
CRP = asynchronous modality → signal of care
```

They share the same grammar. They serve the same purpose: helping relationships stay alive through intentional communication.

They were defined separately because:
1. A person can use CPP without ever using CRP
2. A person can use CRP without ever using CPP
3. The skills, preparation, and outputs of each are different
4. Combining them would obscure the distinct functions

The Grammar layer makes the relationship explicit without requiring either concept to describe the other.

---

## What was deliberately excluded from the definition

**Conflict resolution:** Excluded because CRP is not primarily a repair protocol. Including "resolution of conflict" in the definition would misrepresent the majority of CRP's use cases. The `resolve` intent is supported by CRP but does not define it.

**Specific artifacts:** The definition does not mention Greeting Cards, Voice Memories, or any other artifact. This preserves CRP's independence from any particular implementation. Artifacts are addressed in the Decision Layer and in the Artifact taxonomy — not in the canonical definition.

**Response requirement:** Explicitly excluded. A CRP signal does not require, expect, or request a response. Including a response expectation would create an obligation dynamic inconsistent with Cuqou's philosophy.

**Relationship state triggers:** Excluded. See above.

---

## Relationship to the Ontology Alignment Sprint (ADR-0086)

Before this canonical definition was established, several documents in the Cuqou ecosystem described CRP as:
- "conflict resolution"
- "relationship repair"
- limited to damaged relationships

ADR-0086 documented the alignment between the product-era descriptions and the canonical definition. The historical documents were updated with scope notes. The canonical definition in this file supersedes all prior product-era descriptions.

---

## Open questions at time of canonicalization

1. Should CRP have a minimum definition — a single essential element that distinguishes a CRP signal from an ordinary message? (Candidate: explicit intentionality — the sender consciously frames the message as a relationship signal.)

2. How does CRP relate to "relationship rituals" — recurring acts of care on a schedule? Are scheduled CRP signals still CRP? (Candidate answer: yes, if the intentionality is present each time.)

3. Should the Artifact taxonomy be part of CRP's canonical scope, or a fully independent concept? (Current decision: independent — see v0.5.1 Relationship Artifact.)

---

## Change History

| Version | Date | Change | Author |
|---|---|---|---|
| 1.0 | 2026-06-28 | Initial canonicalization | Cuqou Founders |

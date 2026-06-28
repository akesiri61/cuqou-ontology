---
id: intent-taxonomy
version: "1.0"
status: canonical
category: taxonomy
uri: https://ontology.cuqou.com/intent-taxonomy
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Interaction Intent Taxonomy

Interaction Intent describes **what a person wants to accomplish** when they engage with someone in their relationship network.

Intent is chosen by the person. It is independent of Relationship State.

For the full grammar showing how Intent relates to State and Protocol, see [`RELATIONSHIP_GRAMMAR.md`](RELATIONSHIP_GRAMMAR.md).

---

## Intent Definitions

### `prepare`
> The person is readying themselves before initiating a meaningful synchronous conversation.

- Appropriate protocol: **CPP**
- Modality: Synchronous only
- Example: "เย็นนี้จะโทรหาพ่อ อยากเตรียมตัวก่อน"

---

### `maintain`
> The person wants to stay in contact without a specific occasion or event as the reason.

- Appropriate protocol: CPP or **CRP**
- Modality: Synchronous or Asynchronous
- Example: "ไม่ได้คุยกับเพื่อนนานมาก แค่อยากทักไปบอกว่าคิดถึง"

---

### `appreciate`
> The person wants to express gratitude, recognition, or acknowledgment.

- Appropriate protocol: CPP or **CRP**
- Modality: Synchronous or Asynchronous
- Example: "อยากขอบคุณน้องที่ช่วยเรื่องนั้น"

---

### `celebrate`
> The person wants to mark a positive occasion, milestone, or achievement.

- Appropriate protocol: **CRP** (when presence is not possible) or CPP (when synchronous)
- Modality: Asynchronous common; Synchronous also valid
- Example: "พรุ่งนี้วันเกิดแม่ แต่ไปไม่ได้"

---

### `encourage`
> The person wants to offer support, motivation, or presence during a challenge the other person is facing.

- Appropriate protocol: CPP or **CRP**
- Modality: Synchronous or Asynchronous
- Example: "เพื่อนกำลังเครียดเรื่องงาน อยากส่งอะไรไปให้กำลังใจ"

---

### `reconnect`
> The person wants to resume contact after a period of silence or distance.

- Appropriate protocol: **CPP** (if planning a conversation) or **CRP** (if initiating via message/card)
- Modality: Synchronous or Asynchronous
- Example: "ไม่ได้คุยกับเพื่อนเก่ามา 3 ปี อยากติดต่อกลับ"
- Note: `reconnect` does NOT require `relationship-decay` state. Quiet relationships may also benefit from reconnection.

---

### `resolve`
> The person wants to address tension, misunderstanding, or unresolved friction in the relationship.

- Appropriate protocol: **CPP** (preparation is especially important here) or CRP
- Modality: Synchronous preferred; Asynchronous possible as first step
- Example: "เถียงกับแม่เมื่อวาน อยากคุยให้จบดี"

---

### `remember`
> The person wants to honor a shared memory, past moment, or someone who is no longer present.

- Appropriate protocol: **CRP** (asynchronous — memory as artifact)
- Modality: Asynchronous
- Example: "วันครบรอบที่เราเคยไปด้วยกัน อยากส่งรูปนั้นให้เขา"

---

### `support`
> The person wants to be present for someone who is going through difficulty, loss, or grief.

- Appropriate protocol: CPP (prepare to be with them) or **CRP** (send presence asynchronously)
- Modality: Synchronous or Asynchronous
- Example: "เพื่อนเพิ่งสูญเสียคนในครอบครัว อยากบอกว่าอยู่ตรงนี้"

---

## Intent × Protocol Matrix

| Intent | CPP (Sync) | CRP (Async) |
|---|---|---|
| `prepare` | ✅ | ❌ |
| `maintain` | ✅ | ✅ |
| `appreciate` | ✅ | ✅ |
| `celebrate` | ✅ | ✅ |
| `encourage` | ✅ | ✅ |
| `reconnect` | ✅ | ✅ |
| `resolve` | ✅ | ✅ |
| `remember` | ❌ | ✅ |
| `support` | ✅ | ✅ |

---

## LLM Hints — Intent Detection

When an AI receives a natural-language query, map it to an Intent before selecting a Protocol.

| Query pattern | Likely Intent |
|---|---|
| "วันเกิด / birthday / anniversary" | `celebrate` |
| "คิดถึง / thinking of / miss" | `maintain` |
| "ขอบคุณ / thank / appreciate" | `appreciate` |
| "ให้กำลังใจ / support / encourage" | `encourage` |
| "ไม่ได้คุย / haven't talked / long time" | `reconnect` |
| "เถียง / conflict / misunderstanding" | `resolve` |
| "เตรียม / prepare / before talking" | `prepare` |
| "ความทรงจำ / memory / reminisce" | `remember` |
| "เสียใจ / grief / loss / difficult time" | `support` |

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/intent-taxonomy*  
*License: CC BY 4.0 — Attribution required*

---
id: crp
version: "1.0"
status: canonical
category: protocol
uri: https://ontology.cuqou.com/crp
license: CC BY 4.0 — Cuqou (https://cuqou.com)
grammar_axis: asynchronous
---

# Conversation Resolution Protocol (CRP)

> **Grammar context:** CRP is the asynchronous protocol in the Cuqou Relationship Grammar.  
> For protocol selection logic, see [`decision/protocol-selection.yaml`](../../decision/protocol-selection.yaml).  
> For intent definitions, see [`knowledge/taxonomy/intent-taxonomy.md`](../taxonomy/intent-taxonomy.md).

---

## Canonical Question

> เมื่อยังไม่สามารถหรือยังไม่จำเป็นต้องพูดคุยกันโดยตรง ฉันจะส่งสัญญาณแห่งความใส่ใจอย่างมีความหมายได้อย่างไร?  
> *When direct conversation is not yet possible or necessary, how can I send a meaningful signal of care?*

---

## One Sentence

**EN:** CRP is a structured protocol for expressing meaningful relationship signals through asynchronous communication, enabling continuity, care, and connection without requiring a live conversation.

**TH:** CRP คือโปรโตคอลสำหรับการส่งสัญญาณแห่งความสัมพันธ์ที่มีความหมายผ่านการสื่อสารแบบไม่พร้อมกัน เพื่อคงไว้ซึ่งความต่อเนื่อง ความใส่ใจ และความเชื่อมโยง โดยไม่จำเป็นต้องเกิดการสนทนาแบบทันที

---

## Definition

The Conversation Resolution Protocol (CRP) is a structured approach to expressing care, attention, and presence in a relationship through asynchronous communication — when a live conversation is not possible, not yet appropriate, or simply not the right form for the moment.

CRP is not defined by what problem it solves. It is defined by **what it enables**: the ability to send a meaningful signal of care at the right moment, in the right form, with intention — across any distance, any time zone, any schedule conflict.

A relationship signal sent through CRP is not casual. It is intentional. It is structured to carry meaning rather than simply transmit information.

---

## What CRP Enables

CRP enables a person to:

- Mark a moment that matters to someone they care about (a birthday, a milestone, a difficulty)
- Express care when presence is not possible
- Maintain the continuity of a relationship between conversations
- Reconnect after silence without requiring an immediate response
- Send something that will be received in the other person's own time

CRP does not require the other person to be available. It does not require a reply. It does not require a conversation to follow. It stands alone as an act of care.

---

## Supported Intents

CRP supports multiple interaction intents. The intent shapes which artifact is most appropriate — not which protocol to use.

| Intent | Example |
|---|---|
| `maintain` | "แค่อยากให้รู้ว่าคิดถึง" |
| `appreciate` | "ขอบคุณที่ช่วยเรื่องนั้น" |
| `celebrate` | "วันเกิดนี้ขอให้มีความสุข" |
| `encourage` | "รู้ว่าช่วงนี้ยาก อยู่เคียงข้างเสมอ" |
| `reconnect` | "นานมากแล้ว อยากให้รู้ว่ายังคิดถึง" |
| `resolve` | "ยังคิดเรื่องที่คุยกันอยู่ อยากบอกว่า..." |
| `remember` | "วันนี้คิดถึงครั้งที่เราไปด้วยกัน" |
| `support` | "รู้ว่าช่วงนี้ไม่ง่าย ไม่ต้องพูดอะไร แค่อยู่ตรงนี้" |

For the full Intent taxonomy, see [`knowledge/taxonomy/intent-taxonomy.md`](../taxonomy/intent-taxonomy.md).

---

## Relationship Artifacts

CRP produces a Relationship Artifact — a purposeful, crafted expression of care. The artifact is what the other person receives.

| Artifact | When appropriate |
|---|---|
| Greeting Card | Celebration, appreciation, milestone |
| Voice Memory | Support, reconnection, intimacy |
| Memory Surface | Remembering, anniversary, shared past |
| Future Letter | Long-distance relationship, anticipation |
| Digital Gift | Celebration, encouragement |

For full artifact definitions, see [`knowledge/artifacts/`](../artifacts/).

---

## What CRP Is Not

| CRP is not... | Because... |
|---|---|
| Automated messaging | CRP is intentional. Automated messages are scheduled without intent. |
| Broadcast | CRP is directed to one specific person in one specific relationship. |
| Marketing communication | CRP exists to maintain relationships, not to create transactions. |
| General notifications | Notifications are operational. CRP signals are relational. |
| A replacement for conversation | CRP maintains connection until conversation is possible — it does not substitute for it. |
| Only for damaged relationships | CRP is used for celebration, appreciation, and maintenance in all relationship states. |
| Conflict resolution (exclusively) | Resolution is one of nine intents CRP can support. It is not CRP's definition. |

---

## Canonical Independence

CRP is meaningful independent of any product, platform, or technology.

The pattern of sending a meaningful asynchronous signal of care — a handwritten letter, a postcard, a recorded voice message, a birthday card — has existed across all human cultures long before any digital product. CRP names and structures this pattern precisely enough to apply consistently across any medium.

It can be applied by:
- Individuals managing long-distance relationships
- Family members separated by geography or schedule
- Therapists recommending structured ways to express care
- Educators teaching relationship maintenance
- AI systems helping users decide how to reach out
- Any product that enables meaningful asynchronous communication

CRP would be a useful concept even if Cuqou had never existed.

---

## Related Concepts

- **[CPP](cpp.md)** — the synchronous counterpart: preparation for a live conversation
- **[Relationship Grammar](../taxonomy/RELATIONSHIP_GRAMMAR.md)** — why CPP and CRP are parallel protocols, not opposites
- **[Intent Taxonomy](../taxonomy/intent-taxonomy.md)** — the nine intents CRP supports
- **[Waiting For Me](../states/waiting-for-me.md)** — the attention state that may surface the need for CRP
- **[Relationship Decay](../states/relationship-decay.md)** — one context where CRP may be used (but not the only one)

---

## Frequently Asked Questions

**Q: Does CRP require that the relationship be damaged or in conflict?**  
A: No. CRP is used across all relationship states and intents — including celebration, appreciation, and daily maintenance. Conflict is one of nine intents CRP can support, not its defining condition.

**Q: Is CRP the same as sending a message?**  
A: No. Any message can be sent without CRP. CRP is the protocol that makes a message intentional — structured around a specific intent, directed at a specific relationship, designed to carry meaning rather than transmit information.

**Q: Can CRP be used when the relationship is healthy?**  
A: Yes. CRP is especially valuable in healthy relationships for maintaining continuity, celebrating moments, and expressing care proactively — before any drift occurs.

**Q: Does CRP require a response from the other person?**  
A: No. A CRP signal stands alone. It does not require a reply, does not create an obligation, and does not demand immediate engagement. It is sent when the sender is ready, and received when the other person is ready.

**Q: Is CRP a substitute for having a conversation?**  
A: No. CRP maintains connection until a conversation is possible or appropriate. It is a bridge — not a destination.

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/crp*  
*License: CC BY 4.0 — Attribution required*

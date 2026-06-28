---
id: intent-provenance
version: "1.0"
status: canonical
category: concept
uri: https://ontology.cuqou.com/intent-provenance
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Intent Provenance

## Canonical Question

> เจตนาที่อยู่เบื้องหลังการสื่อสารนี้ — มาจากมนุษย์หรือ AI?  
> *The intent behind this communication — did it originate from a human or from AI?*

---

## One Sentence

**EN:** Intent Provenance is the traceability of a relationship expression's intent to a genuine human decision — the verifiable record that a human, not an AI, chose to reach out.

**TH:** Intent Provenance คือความสามารถในการติดตามที่มาของเจตนาในการสื่อสารในความสัมพันธ์กลับไปยังการตัดสินใจของมนุษย์จริง — บันทึกที่ยืนยันได้ว่ามนุษย์ ไม่ใช่ AI คือผู้ที่เลือกจะติดต่อ

---

## Definition

Intent Provenance is the principle that every meaningful relationship expression must be traceable to a human intention as its origin.

It answers the question: *whose decision was this?*

A relationship expression has valid Intent Provenance when:
- A human decided to reach out (not an AI agent acting on a schedule)
- A human chose the form of expression (even if AI suggested it)
- A human reviewed and approved the content (even if AI drafted it)

A relationship expression lacks Intent Provenance when:
- An AI agent sent it autonomously based on a trigger (e.g., "birthday detected → send card")
- No human made an active choice to reach out at this moment
- The recipient has no reason to believe a human thought of them

---

## The Provenance Metaphor

In academic research, provenance describes the chain of custody of a source: where it came from, who handled it, and whether it can be trusted.

In relationship communication, Intent Provenance describes the same chain of custody for human intention:
- Who initiated the decision to communicate?
- Was a human actively involved, or was this automated?
- Can the recipient trust that a human thought of them?

---

## Why This Matters

A birthday message carries relational weight not because of what it says, but because a human chose to send it today, to this person, from their own intention.

If the same message is sent automatically by an AI that "remembered" the birthday — the words are identical, but the meaning is different. The recipient is not being thought of by a person. They are being notified by a system.

As AI agents become more capable of autonomous relationship management, the distinction between "a person thought of me" and "an algorithm sent a message" will become one of the most important questions in human relationships.

Intent Provenance is Cuqou's answer to that question: a structural commitment that human intent is always at the origin of relationship expressions within the ecosystem.

---

## Position in the Grammar

Intent Provenance is a check that occurs before Protocol selection:

```
Human Decision    → Intent Provenance verified?
       ↓
    Intent        → What does the person want to accomplish?
       ↓
   Protocol       → Sync or Async?
       ↓
  Expression      → What form of care?
       ↓
Human Contribution → Is authentic human voice present?
       ↓
    Medium        → Through what channel?
       ↓
     Send
```

If Intent Provenance cannot be verified — if there is no active human decision at the origin — the expression should not proceed.

---

## AI's Role Within This Principle

AI may:
- Surface the right moment for a human to reach out (Attention Layer)
- Suggest that today might be a good time to send something (recommendation)
- Offer templates and examples once the human has decided to act
- Assist with composition after the human has initiated the intent

AI must not:
- Initiate the intent itself ("I noticed it's her birthday, I'll send a card")
- Replace the human's decision with a scheduled trigger
- Act on relationship data without a human choosing to act

The distinction: Cuqou may remind a person that it is someone's birthday. The person then decides whether to reach out. This is Intent Provenance intact.

An AI that automatically sends a birthday card because it detected the date does not preserve Intent Provenance — even if the card is beautiful and the words are perfect.

---

## Related Concepts

- **[Relationship Truth](relationship-truth.md)** — the root principle Intent Provenance serves
- **[Human Contribution](human-contribution.md)** — the complementary principle: the voice must be human, not just the intent
- **[Ethics E005](../../ethics/rules.yaml)** — No Autonomous Relationship Action (the rule that enforces this)
- **[Attention Layer](../systems/attention-layer.md)** — the system that surfaces moments for human action (without replacing human decision)

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/intent-provenance*  
*License: CC BY 4.0 — Attribution required*

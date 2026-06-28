---
id: human-contribution
version: "2.0"
status: canonical
category: stewardship-principle
layer: 1
uri: https://ontology.cuqou.com/principles/human-contribution
license: CC BY 4.0 — Cuqou (https://cuqou.com)
axiom: relationship-truth
---

# Human Contribution

## Canonical Question

> ในการสื่อสารที่มีความหมาย — เสียงของใครที่ถูกส่งออกไป?  
> *In a meaningful relationship communication — whose voice is sent?*

---

## Stewardship Principle — Layer 1

Human Contribution is a Stewardship Principle. It governs the authenticity of the human voice in relationship expressions — not by prohibiting AI assistance, but by preserving the space in which the human's own voice can enter.

---

## One Sentence

**EN:** Human Contribution is the principle that the system must always preserve space for the person's authentic words, feelings, and intentions to be present in any relationship expression — regardless of how much AI assists in its creation.

**TH:** Human Contribution คือหลักการที่ว่าระบบต้องรักษาพื้นที่ให้มนุษย์สามารถแสดงถ้อยคำ ความรู้สึก และเจตนาของตนเองได้เสมอ — ไม่ว่า AI จะช่วยสร้างเนื้อหามากเพียงใดก็ตาม

---

## Definition

Human Contribution is the layer in relationship communication where the person — not the AI — becomes the speaker.

AI systems may assist with preparation, suggestion, organization, and clarity. They may offer examples, frameworks, and starting points. But at the point of relationship communication, there must always be an opportunity for the person to contribute their own words, their own choices, their own voice.

Human Contribution is not a feature. It is a principle that governs every protocol and every expression in the Cuqou Relationship Ontology.

---

## Why It Exists

Relationship communication derives its meaning from authenticity. A message carries weight not only because of what it says, but because of who is saying it — and because the recipient knows the sender chose to send it in their own words.

When AI generates the message and the person only presses send, something essential is lost: the signal that the sender invested themselves in the act of communication.

This is not about quality of writing. It is about the source of care.

A handwritten card with imperfect grammar carries more relational weight than a perfectly composed AI message — because the handwriting is proof of human effort and attention.

Human Contribution preserves that proof in every protocol.

---

## Human Contribution Is a Spectrum

Human Contribution is not binary. It exists on a spectrum from AI-generated to fully human-authored.

```
0%          25%               50%              75%         100%
│           │                 │                │           │
AI          AI draft,         Human + AI       Human with  Human
Generated   human edits       collaborative    AI refining authored
```

Cuqou does not require 100% Human Contribution in every expression. AI assistance is valuable and encouraged.

Cuqou does require that:
1. The human is **aware** of where their expression sits on this spectrum
2. The human has a **genuine path** to move toward higher contribution if they choose
3. The system never **hides** the degree of AI involvement

---

## `human_contribution_score`

The system uses an internal metric to track where an expression sits on the spectrum:

```yaml
human_contribution_score:
  range: 0.0–1.0
  purpose: >
    Internal reasoning only. 
    Used by the Decision Layer to calibrate AI behavior.
    Never shown to users as a gamification metric or quality score.
  usage:
    - If score is low: AI should ask more questions, offer more space, reduce drafting
    - If score is high: AI may offer refinement assistance
    - Score is never used to judge the value of the relationship expression
```

The score exists not to evaluate the person — but to help the system know when to step back and when to assist.

---

## What the System Must Preserve

In every relationship expression, the system must preserve:

1. **The person's ability to read** what will be sent before it is sent
2. **The person's ability to modify** any part of the content
3. **The person's ability to add** their own words to any AI-generated draft
4. **The person's ability to replace** AI content entirely with their own
5. **The person's ability to reject** — to cancel the communication entirely

These are not restrictions on AI capability. They are the conditions under which AI capability becomes genuinely useful rather than substitutive.

---

## Role of AI Within This Principle

AI may:
- Draft a starting point the human can modify
- Suggest multiple options with different tones or styles
- Translate the human's words into another language
- Improve clarity and grammar of what the human has written
- Organize the human's thoughts into a more structured form
- Coach the human toward finding their own words

AI must not:
- Send relationship expressions without human review
- Present AI-generated content as the person's own without transparency
- Make the AI draft the only path — human composition must always be available
- Reduce the interface to a "select and send" pattern with no authentic contribution step

---

## What Human Contribution Is Not

| It is not... | Because... |
|---|---|
| A required word count | Length is not the measure of authenticity |
| Manual composition only | AI assistance is permitted and encouraged |
| Anti-AI | AI is a partner in preparation, not an enemy |
| A UX guideline | It is an Ontology Principle that governs protocol design |
| Optional | Every CPP and CRP implementation must honor this principle |

---

## Position in the Grammar

Human Contribution is the fourth axis in the Cuqou Relationship Grammar:

```
Intent               → What does the person want to accomplish?
Protocol             → What communication modality is appropriate?
Expression           → What form does the relationship signal take?
Human Contribution   → Where does the person's authentic voice enter?
Medium               → Through what channel or object is it expressed?
```

See: [`knowledge/taxonomy/RELATIONSHIP_GRAMMAR.md`](../taxonomy/RELATIONSHIP_GRAMMAR.md)

---

## Canonical Independence

This principle is meaningful independent of any product, platform, or AI system.

The distinction between "a letter I wrote" and "a letter written for me" has existed in human relationships long before AI. A person who pays someone else to write their wedding vows is making a different statement than a person who writes imperfect vows themselves. The difference is Human Contribution.

AI makes this principle more important to name explicitly — not less.

---

## Related Concepts

- **[Relationship Truth](../../axioms/relationship-truth.md)** — the Axiom this principle serves
- **[Human Agency](../principles/human-agency.md)** — the authority layer; paired with Contribution
- **[Intent Provenance](intent-provenance.md)** — the origin layer; precedes Contribution
- **[CPP](../protocols/cpp.md)** — preparation protocol where Human Contribution applies to the 4 Standard Answers
- **[CRP](../protocols/crp.md)** — signal protocol where Human Contribution applies to every Relationship Expression
- **[ARCHITECTURE_OF_RELATIONSHIP](../../ARCHITECTURE_OF_RELATIONSHIP.md)** — the layer this principle belongs to

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/human-contribution*  
*License: CC BY 4.0 — Attribution required*

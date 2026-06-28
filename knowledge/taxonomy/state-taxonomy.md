---
id: state-taxonomy
version: "1.0"
status: canonical
category: taxonomy
uri: https://ontology.cuqou.com/state-taxonomy
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Relationship State Taxonomy

Relationship State describes **the current condition of a relationship** as observed — not chosen.

State is determined by patterns of contact, responsiveness, and emotional connection over time. It is not assigned by a person; it is recognized.

For the full grammar showing how State relates to Intent and Protocol, see [`RELATIONSHIP_GRAMMAR.md`](RELATIONSHIP_GRAMMAR.md).

---

## State Definitions

### `healthy`
> Regular, mutual contact with no significant friction. Both people are responsive and engaged.

- Characteristics: Contact frequency matches both parties' expectations. Messages are reciprocated. There is no unresolved tension.
- Protocol relevance: All intents are available. No particular urgency for intervention.

---

### `growing`
> The relationship is deepening — characterized by increasing contact, emotional vulnerability, or mutual investment.

- Characteristics: More frequent contact than baseline. New shared experiences being created. Emotional intimacy increasing.
- Protocol relevance: CPP may help prepare for conversations that deepen the relationship further.

---

### `quiet`
> Low contact, but without conflict or damage. The relationship is dormant rather than deteriorating.

- Characteristics: Long periods between contact. When contact occurs, it is warm. Neither party feels negatively about the silence.
- Protocol relevance: CRP is well-suited to `maintain` or `reconnect` from a quiet state without requiring a full synchronous conversation.
- Note: Quiet is not a warning sign. Some meaningful relationships are naturally quiet.

---

### `at-risk`
> Contact is declining in a pattern that may lead to decay if unaddressed. One or both parties may sense the drift but have not acted.

- Characteristics: Contact frequency dropping below both parties' implicit expectations. Messages less likely to be reciprocated. Small frictions accumulating.
- Protocol relevance: Both CPP and CRP are appropriate. The `reconnect` or `maintain` intent is often relevant here.

---

### `decaying`
> Meaningful drift has occurred. The relationship has lost momentum and requires deliberate effort to restore.

- Characteristics: Extended silence with no clear reason. Prior attempts at contact may have gone unanswered. One or both parties may feel the relationship has become distant.
- Protocol relevance: Both CPP and CRP are appropriate. `Reconnect` and `maintain` intents are common. Relationship Decay does NOT determine which protocol must be used — it provides context.
- **See:** `knowledge/states/relationship-decay.md` for the full canonical definition.

---

### `disconnected`
> Contact has ceased. The relationship exists in memory rather than in active exchange.

- Characteristics: No contact for an extended period, with no expectation of future contact. The relationship is preserved in memory but is not active.
- Protocol relevance: CRP (specifically the `remember` intent) may be appropriate for honoring the relationship privately. CPP or CRP may be used if attempting to re-establish contact.

---

## What State Does NOT Determine

State is context — not a decision tree.

| Common misunderstanding | Correct understanding |
|---|---|
| "Relationship Decay triggers CRP" | Decay is a state; Intent triggers protocol selection |
| "CPP requires a decaying relationship" | CPP is for the `prepare` intent in any state |
| "Healthy relationships don't need protocols" | `celebrate`, `appreciate`, and `maintain` intents are common in healthy relationships |
| "Disconnected means the relationship is over" | A person may choose to `reconnect` or `remember` from any state |

---

## State Transitions

States are not fixed. A relationship moves between states over time.

```
healthy ↔ growing
healthy → quiet → at-risk → decaying → disconnected   (without intervention)
disconnected → at-risk → quiet → healthy               (with deliberate reconnection)
```

No tool or protocol can force a state transition. Protocols support the person's intent — the relationship responds in its own time.

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/state-taxonomy*  
*License: CC BY 4.0 — Attribution required*

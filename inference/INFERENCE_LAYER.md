---
id: inference-layer
version: "1.0"
status: canonical
category: system
uri: https://ontology.cuqou.com/inference
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Cuqou Inference Layer

## What This Is

The Inference Layer is the third structural layer of the Cuqou Relationship Ontology:

| Layer | Answers | Files |
|---|---|---|
| **Ontology** | What is this? | `vocabulary/`, `knowledge/` |
| **Grammar** | How do concepts relate? | `knowledge/taxonomy/` |
| **Inference** | What should be done? | `inference/` |

The Inference Layer contains **declarative rules** — structured knowledge that AI systems, MCP Servers, and applications can use to reason about relationship situations without hard-coding logic in each implementation.

---

## Why Declarative Rules, Not Code

A rule in code: `if state == "decaying" and intent == "reconnect": suggest("crp")`  
A rule in the ontology: the YAML file in this directory.

The difference is not technical — it is architectural:

- Code lives in one implementation. Rules live in the ontology.
- Code must be updated in every system when logic changes. Rules update once.
- Code is opaque to AI systems. Rules are readable by AI systems directly.
- Code creates divergence across products. Rules create convergence.

When a ChatGPT plugin, a Claude MCP Server, and a mobile app all reference the same inference rules, they reason identically — not because they share code, but because they share knowledge.

---

## Rule Types

The Inference Layer uses two distinct rule types. They must not be confused.

### Type 1 — Inference Rules (`type: inference`)

> "When X is true, then Y is recommended."

Used for: protocol selection, artifact suggestion, priority ordering.

```yaml
type: inference
when:
  conditions...
then:
  recommendation...
confidence: 0.0–1.0
```

### Type 2 — Constraint Rules (`type: constraint`)

> "X does NOT imply Y."

Used for: preventing incorrect AI reasoning. Constraints are as important as inferences — they define what the system must NOT conclude.

```yaml
type: constraint
prevents:
  from: {source concept}
  to:   {target concept}
rationale: "..."
```

Without constraint rules, an AI system may correctly apply inference rules but still reach wrong conclusions by assuming unspecified relationships.

---

## Rule Files

Rules are organized by domain:

| File | Domain |
|---|---|
| `protocol-selection.yaml` | Which protocol to use given Intent + Modality |
| `artifact-suggestion.yaml` | Which artifact to suggest given Protocol + Intent |
| `priority-ordering.yaml` | How to rank multiple recommendations |
| `constraints.yaml` | What may NOT be inferred (all negative rules) |

---

## How AI Systems Should Use This Layer

1. Load `knowledge/taxonomy/RELATIONSHIP_GRAMMAR.md` — understand the three axes
2. Load `inference/constraints.yaml` — know what NOT to infer
3. Load `inference/protocol-selection.yaml` — determine which protocol applies
4. Load `inference/artifact-suggestion.yaml` — determine which artifact to suggest
5. Present recommendation with confidence score

The order matters: constraints before inferences, so prohibited conclusions are blocked before positive rules are applied.

---

## Stability

Inference rules are expected to be more volatile than canonical concept definitions. A concept's meaning should remain stable for years. A rule may be refined as new contexts are discovered.

Rule versioning:
- Each rule has a `version` field
- Rule changes are logged in `CHANGELOG.md`
- Rules with `confidence: 1.0` are considered axiomatic and require Maintainer approval to change
- Rules with `confidence < 1.0` may be tuned without formal RFC

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/inference*  
*License: CC BY 4.0 — Attribution required*

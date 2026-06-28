---
version: "1.0"
status: canonical
uri: https://ontology.cuqou.com/architecture
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# The Architecture of Relationship

## What Cuqou Believes a Relationship System Must Contain

This document is not a technical specification.  
It is a map of what Cuqou believes must exist — at every level — for a system to genuinely serve human relationships in the age of AI.

Applications change. AI capabilities change. Technologies change.  
This architecture should remain.

---

## The Foundational Question

Before Cuqou defines any feature, protocol, or AI behavior, it asks:

> **Does this help authentic human relationships remain truthful, trustworthy, and continuous?**

Everything in the Cuqou ecosystem — every concept, every rule, every product decision — must be able to answer this question with "yes."

---

## Four Layers

A system that genuinely serves human relationships must operate at four distinct levels. Cuqou calls these layers. Each layer depends on the ones above it.

```
┌─────────────────────────────────────────────────────────┐
│                   LAYER 0 — AXIOM                       │
│              Relationship Truth                         │
│     "What must be true about every relationship         │
│      expression in this ecosystem?"                     │
└─────────────────────────┬───────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────┐
│              LAYER 1 — STEWARDSHIP                      │
│           Stewardship Principles                        │
│     "How does the system govern AI behavior             │
│      to protect what matters?"                          │
└─────────────────────────┬───────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────┐
│               LAYER 2 — LANGUAGE                        │
│     Protocols / Grammar / States / Intents              │
│     "What vocabulary describes relationships            │
│      precisely enough for both humans and AI?"          │
└─────────────────────────┬───────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────┐
│              LAYER 3 — INTELLIGENCE                     │
│     Decision Layer / Constraints / Recommendations      │
│     "How does the system reason about what              │
│      to suggest and what to prevent?"                   │
└─────────────────────────┬───────────────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────┐
│              LAYER 4 — EXPERIENCE                       │
│     Waiting For Me / Attention Layer / Greeting Card    │
│     "What does the person actually see and use?"        │
└─────────────────────────────────────────────────────────┘
```

Each layer is distinct. A concept or feature belongs to one layer, not multiple. The layer determines how a concept is defined and what it may reference.

---

## The Domain / Product Boundary

Layers 0–3 are **Domain**. They describe what is universally true about human relationships and how systems should reason about them. These layers exist independent of any product, platform, or interface.

Layer 4 is **Product**. It describes what people experience — and may take many forms across different implementations. Multiple Experience Patterns may exist, each applying Layers 0–3 in a specific context.

```
Layers 0–3  DOMAIN    ← universal, product-independent, rarely changes
════════════════════════════════════════════════════════
Layer 4     PRODUCT   ← implementation-specific, may have multiple patterns
```

This boundary matters because:
- A concept that belongs to Layers 0–3 has one canonical definition
- An Experience Pattern at Layer 4 can have multiple forms while using the same Domain concepts
- Changes to Domain layers affect all products built on the ontology; changes to Layer 4 do not

---

## Layer 0 — Axiom: Relationship Truth

**One sentence:** Meaningful relationship expressions must faithfully represent authentic human intention, regardless of how much technology assists in their creation or delivery.

**The Axiom is the single answer to:** "What must be true about every expression that travels through this system?"

It is not a rule that prohibits. It is the foundation that all rules protect.

All other layers exist in service of the Axiom.

**See:** `axioms/relationship-truth.md`

---

## Layer 1 — Stewardship: The Five Principles

The Stewardship Principles govern how AI operates within the system. They do not limit AI capability — they define the boundaries within which AI may fully exercise its capability.

Each principle answers a distinct question:

| Principle | Question answered |
|---|---|
| **Human Agency** | Who has final decision authority? |
| **Human Contribution** | Whose voice is present in the expression? |
| **Intent Provenance** | Where did the intent to reach out originate? |
| **Transparency** | Can the person see how AI participated? |
| **Human Approval** | Was this specific action explicitly approved? |

These principles are not prohibitions. They are the conditions under which AI assistance becomes genuine help rather than substitution.

**The governing test for any feature:**  
> "Does this augment human capacity, or replace it?"

AI may: suggest, draft, refine, translate, organize, coach, simulate, recommend.  
AI must not: decide, override, commit, send.

**See:** `knowledge/principles/`

---

## Layer 2 — Language: The Vocabulary of Relationships

Layer 2 provides the precise vocabulary that both humans and AI systems need to reason correctly about relationships.

Without shared language, AI cannot give useful advice. With shared language, AI can reason with precision.

| Category | What it contains |
|---|---|
| **Protocols** | Named methods for specific relationship actions (CPP, CRP) |
| **Grammar** | The axes that govern how all concepts relate (State × Intent × Protocol) |
| **States** | Conditions a relationship can be in (healthy, quiet, decaying…) |
| **Intents** | What a person wants to accomplish (prepare, maintain, celebrate…) |
| **Expressions** | The forms care can take (message, card, memory, presence) |

**See:** `knowledge/protocols/`, `knowledge/taxonomy/`

---

## Layer 3 — Intelligence: Reasoning and Recommendations

Layer 3 is where the system reasons. Given what is known about a relationship — its state, the person's intent, the history between them — what should be suggested? What should be prevented?

Intelligence without the layers above it is dangerous. It can optimize for engagement, not connection. It can recommend actions that violate human agency.

Intelligence constrained by Axiom + Stewardship + Language becomes genuinely useful.

| Component | What it does |
|---|---|
| **Decision Layer** | Inference rules: what protocol fits this situation? |
| **Constraints** | Logical rules: what cannot be true simultaneously? |
| **Recommendations** | Suggestions: what might help given this context? |
| **`human_contribution_score`** | Internal 0–1 metric: how much of this expression originated from the human? Used to calibrate AI behavior — never shown as gamification. |

**See:** `decision/`

---

## Layer 4 — Experience: What People See and Use

Layer 4 is where the person lives. Everything above it exists to make this layer trustworthy.

Experience Patterns in Cuqou are not standalone features. Each one is an expression of Layers 0–3 in a specific context. Defining an Experience Pattern requires specifying which Stewardship Principles apply, which protocols it draws from, and how the Decision Layer informs it.

| Pattern | What it surfaces |
|---|---|
| **Waiting For Me** | Relationships and moments that are waiting for the person's attention |
| **Attention Layer** | The delivery system that brings WFM to the person's existing context |
| **Greeting Card** | A structured form for CRP-based expressions |
| **Future Letter** | A time-deferred expression of memory and meaning |

Experience Patterns share a common template. Every pattern must pass the Human Agency Check and Relationship Truth Check before becoming canonical.

**See:** `experience-patterns/EXPERIENCE_PATTERN_GUIDE.md`

---

## Two Ways to Read the System

The Architecture gives the **vertical view** — what layers exist and what each layer contains.

The Flow gives the **horizontal view** — how a single relationship expression moves from human decision to delivery.

These are two perspectives on the same system. Together they form a complete picture.

**See:** `RELATIONSHIP_FLOW.md`

---

## The Vertical Test

For any proposed concept, feature, or AI behavior:

```
Does it serve Relationship Truth?                    (Layer 0 — Axiom)
         │
Does it respect the Stewardship Principles?         (Layer 1)
         │
Does it use or extend shared vocabulary correctly?  (Layer 2)
         │
Does it reason with appropriate constraints?        (Layer 3)
         │
Does it serve the person's actual relationship?     (Layer 4)
```

If the answer at any layer is "no" — redesign before proceeding.

---

## What This Architecture Is Not

| It is not... | Because... |
|---|---|
| A technical API design | Layer concerns are conceptual, not implementation boundaries |
| A product roadmap | The layers describe what must exist, not when |
| A list of restrictions | The layers define the shape of freedom, not its limits |
| Complete | v0.8.0 introduces this model; future RFCs will add to it |

---

## A Note on AI

The architecture above is designed for a world where AI is capable, useful, and increasingly autonomous.

Cuqou does not resist AI capability.  
Cuqou defines the architecture that ensures AI capability serves human relationships rather than substituting for them.

The question is not: *how capable should AI be?*  
The question is: *toward what end should AI capability be directed?*

Cuqou's answer: toward the authenticity, continuity, and meaning of human relationships — with humans remaining the authority over their own connections.

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/architecture*  
*License: CC BY 4.0 — Attribution required*

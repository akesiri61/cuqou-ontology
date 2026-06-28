---
version: "1.0"
status: canonical
uri: https://ontology.cuqou.com/pattern-language
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Pattern Language

## What This Is

Pattern Language is the sixth layer of the Cuqou knowledge system — the bridge between the Domain Model (Layers 0–3) and what people actually experience (Layer 4).

It answers a question that Architecture and Flow cannot:

> **"What recurring human problem does this experience solve — and what must it never become?"**

---

## The Six Layers of Cuqou Knowledge

| Layer | What it answers |
|---|---|
| Ontology (Concepts + Principles) | What exists? What governs? |
| Grammar | How do concepts relate? |
| Decision Model | What should the system recommend or prevent? |
| Architecture | What are the structural layers? |
| Flow | How does an expression move from decision to delivery? |
| **Pattern Language** | What human problem recurs? How do we resolve it without losing Relationship Truth? |

Each layer above this one describes the system.  
Pattern Language describes the **human problem the system exists to solve**.

---

## Inspiration: Christopher Alexander

In *A Pattern Language* (1977), architect Christopher Alexander observed that the most enduring designs — buildings, neighborhoods, cities — are not defined by features or specifications, but by their ability to resolve recurring human tensions.

A pattern is not "a room with a window."  
A pattern is "the recurring human need for light and privacy in a working space — and how to resolve the tension between them."

The pattern exists because the tension exists. The pattern endures because the tension is real, recurring, and human.

Cuqou applies this idea to relationship systems:

A Cuqou Experience Pattern is not "a notification with a list of people."  
A Cuqou Experience Pattern is "the recurring human situation where someone cares about a relationship but has no signal to act — and how to surface that moment without inducing guilt or obligation."

---

## Why Pattern Language Matters More Than Feature Specification

Feature specifications describe what to build.  
Pattern Language describes what problem to solve — and what failure looks like.

| Feature Specification | Pattern Language |
|---|---|
| "Show a list of relationships awaiting attention" | "Resolve the tension between caring and forgetting without manufacturing guilt" |
| "Send a push notification" | "Surface a meaningful moment at the right time without becoming noise" |
| "Add a streak counter" | **Anti-pattern**: this is what the experience must never become |
| "Display relationship health score" | **Anti-pattern**: this replaces human judgment with system judgment |

Feature specifications drift. Product pressure, A/B tests, and engagement metrics push features toward whatever increases usage.

Pattern Language creates a **principled boundary** — not by listing rules, but by naming the human problem, the tension, and the anti-patterns that represent failure. When a proposed feature would resolve the tension in a way that violates Relationship Truth, the Pattern Language makes that visible.

---

## The Structure of a Pattern

Every Cuqou Experience Pattern has seven elements:

### 1. Human Problem
What recurring human situation does this pattern address?  
Not "what feature gap does this fill?" — but "what do people experience again and again that leaves their relationships worse than they could be?"

### 2. Tension
What opposing forces create this problem?  
Most relationship problems exist because two real, valid human needs are in conflict. The pattern exists to resolve that tension — not eliminate either side of it.

```
Example — Waiting For Me:

Want to care
    ↓
Life takes over / No signal
    ↓
Relationship goes quiet
    ↓
Guilt makes starting harder
    ↓
Silence grows
```

### 3. Resolution
How does this pattern resolve the tension?  
Not a feature list — a philosophy. What is the minimum intervention that resolves the tension without creating new ones?

Resolution respects both Relationship Truth and the human's autonomy. It does not eliminate tension by eliminating one side of it.

### 4. Purpose
What is this pattern for? One clear sentence.

### 5. Layer Dependencies
Which Axiom, Principles, Protocols, and Decision rules does this pattern apply?  
A pattern that cannot trace its dependencies to Layers 0–3 is not a Cuqou pattern.

### 6. Anti-patterns
What must this experience never become?  
This is the most important element for long-term product integrity.

Anti-patterns name the failure modes before they happen. A team that knows the anti-patterns can resist feature pressure that would push the experience toward them.

### 7. Success Criteria
How does a person feel when the pattern works well?  
Not clicks, not retention, not engagement rate — but the human experience of the pattern resolving the tension it set out to resolve.

---

## Pattern Language and Relationship Truth

Every pattern must be evaluated against the Relationship Truth Axiom:

> "Does this pattern preserve authentic human intention, or does it substitute AI inference for human care?"

A pattern that passes this check may use AI extensively. A pattern that fails this check should not exist in Cuqou — regardless of how useful it might seem.

The Pattern Language is one of the mechanisms through which Relationship Truth governs the product, not just the ontology.

---

## How to Use Pattern Language

**For Experience Pattern authors:**  
Use the template in `experience-patterns/EXPERIENCE_PATTERN_GUIDE.md`. Every field in the template corresponds to one element in this document.

**For product designers:**  
When a new feature is proposed, ask: does it resolve a named Tension? Does it avoid the Anti-patterns? Can it trace its Layer Dependencies?

**For AI system builders:**  
The Human Problem, Tension, and Resolution tell you what the AI is actually trying to help with. The Anti-patterns tell you what the AI must not optimize for.

**For anyone evaluating whether a feature belongs in Cuqou:**  
If the feature cannot be mapped to an existing or proposed Pattern — or if it would push an existing Pattern toward its Anti-patterns — it does not belong here.

---

## Relationship to Other Documents

| Document | Relationship |
|---|---|
| `ARCHITECTURE_OF_RELATIONSHIP.md` | Describes the layers; Pattern Language is one of them |
| `RELATIONSHIP_FLOW.md` | Describes how an expression flows; Pattern Language describes the human problem the flow serves |
| `experience-patterns/EXPERIENCE_PATTERN_GUIDE.md` | The template that applies Pattern Language to specific experience patterns |
| `axioms/relationship-truth.md` | The Axiom that every pattern must preserve |

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/pattern-language*  
*License: CC BY 4.0 — Attribution required*

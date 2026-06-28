---
version: "2.0"
status: canonical
uri: https://ontology.cuqou.com/roadmap
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Cuqou Relationship Ontology — Roadmap

## What cuqou-ontology Is

`cuqou-ontology` is a **Living Ontology** — the **public Knowledge layer** of Cuqou.

> **Scope boundary:** This repository contains Knowledge (what concepts mean, how they relate, what principles govern). It does not contain Know-how (how the Runtime selects protocols, how relationships are scored or ranked, how signals are detected). Runtime logic lives in `cuqou-runtime` (private). See: `FOUNDER_DECISIONS §26`.


> **A Living Ontology is an executable body of knowledge that continuously governs product behavior, AI behavior, engineering decisions, and user experience.**

It is not a Wiki. It is not a Glossary. It is not a document library that is referenced when convenient.

It governs every stage of building:

```
UX Design          ← governed by Experience Patterns + Anti-patterns
AI Behavior        ← governed by Decision Layer + Ethics Layer
Product Decisions  ← governed by Relationship Truth + Stewardship Principles
Code Review        ← governed by Conformance Checklist
Team Decisions     ← governed by the 4 Questions
```

## The Complete Loop

```
Human Problem
        │
        ▼
Relationship Truth
        │
        ▼
Living Ontology
        │
        ▼
Traceability
        │
        ▼
Experience Pattern
        │
        ▼
Implementation
        │
        ▼
Conformance
        │
        ▼
Behavioral Evidence
        │
        └─────────────────┐
                          ▼
          Foundation proven (or RFC opened)
```

Phase II does not add knowledge.  
Phase II **collects evidence** — that the Living Ontology produces real behavioral change in real humans.

**The Development Pipeline:**

```
Human Problem
        ↓
4 Questions answered
        ↓
TRACEABILITY_MATRIX.md row added
        ↓
Experience Pattern confirmed
        ↓
Implementation built
        ↓
ONTOLOGY_CONFORMANCE_CHECKLIST.md completed
        ↓
Merge
```

**The 4 Questions (team rule — applied before every feature):**

> 1. **Human Problem** — What recurring human problem does this solve?
> 2. **Relationship Truth** — How does this connect to the authenticity of human relationships?
> 3. **Existing Foundation** — Can the existing ontology cover this without adding new layers?
> 4. **Implementation** — Given the foundation exists, what is the best experience?

Only after questions 1–3 are answered does the team move to question 4.

---

## Foundation Freeze Notice

**As of v1.0.0, the structural foundation of this ontology is frozen.**

This means:
- No new layers may be added without Maintainer review and an accepted RFC
- No existing Axiom, Stewardship Principle, or Grammar axis may be redefined
- The seven elements of Pattern Language are fixed

What continues to grow:
- New Experience Patterns (validated against the existing foundation)
- New proposed Concepts at Layer 2 (added via RFC process)
- CONFORMANCE criteria as implementations are validated
- Externalization tooling (MCP, JSON-LD, LLM packages)

---

## Phase II Rule — Foundation Freeze Enforcement

> **No new layers may be added during Phase II.**

Permitted during Phase II:
- Bug fixes and clarifications in existing ontology files
- Missing definitions proven necessary by real usage
- New Experience Patterns (using the existing template)

Not permitted during Phase II:
- New structural layers
- New Axioms
- New Stewardship Principles (without RFC)

**When the urge to add a new layer arises:**  
Ask first: *"Can the existing foundation address this?"*  
If yes — adjust the implementation, not the foundation.  
If no — open an RFC and document the gap before acting.

This rule exists so that Phase II remains a proof of foundation quality, not a continuation of foundation design.

---

## Roadmap

```
Phase I    Foundation         ✅ COMPLETE — v1.0.0 (2026-06-28)
              │
Phase II   Behavioral Validation   ← current
           LINE Mini App
              │
Phase III  Knowledge Validation
           cuqou-web
              │
Phase IV   External Ecosystem
           MCP · AI Plugin · Semantic API · Conformance
```

---

## Phase I — Foundation ✅ COMPLETE (v1.0.0 — 2026-06-28)

Build a complete, layered knowledge system for human relationships in the age of AI.

**Completed:**

| Layer | What was built |
|---|---|
| 0 — Axiom | Relationship Truth |
| 1 — Stewardship | Human Agency · Human Contribution · Intent Provenance |
| 2 — Language | CPP · CRP · Grammar · States · Intents |
| 3 — Intelligence | Decision Layer · Constraints · Ethics |
| Architecture | ARCHITECTURE_OF_RELATIONSHIP.md |
| Flow | RELATIONSHIP_FLOW.md |
| Pattern Language | PATTERN_LANGUAGE.md |
| 4 — Experience | Waiting For Me (Reference Pattern) |

**Foundation integrity test:**  
Every concept can answer: *"How does this serve Relationship Truth?"*  
Every Experience Pattern can answer: *"What human problem does this resolve — and what must it never become?"*

---

## Phase II — Behavioral Evidence Collection (current)

**Question:**

> "Can we prove with real users that this Living Ontology helps humans care for their relationships better — without losing Relationship Truth?"

This is the single measure of Phase II success. Not feature count. Not retention. Not session length.

**What Phase II collects:**

**Why LINE Mini App first:**  
A website proves that AI and humans *understand* Cuqou.  
A Mini App proves that Cuqou *changes human behavior*.  
Behavioral Validation has more weight than Knowledge Validation in Phase II.

**Reference Implementation:** Cuqou LINE Mini App

**Primary Goal:**

> **Prove that `cuqou-ontology v1.0.0` is Executable Knowledge.**

"Executable Knowledge" means: the ontology can be traced into design decisions, system behavior, and user experience in a verifiable chain:

```
Ontology → Traceability Matrix → User Flow → UI
```

If the chain holds without expanding the foundation, the ontology is proven.

**Success Criterion:**

> **Every user action must be traceable back to the ontology.**

Example — when a user presses "Send Greeting Card":

```
Relationship Truth (Axiom)
        ↓
Human Agency (Stewardship)
        ↓
Intent Provenance (Stewardship)
        ↓
CRP (Protocol — Layer 2)
        ↓
Decision Layer (Layer 3)
        ↓
Waiting For Me (Experience Pattern — Layer 4)
        ↓
Greeting Card (artifact)
```

If a user action cannot be traced to this chain — diagnose first:  
- **Implementation Drift** → fix the implementation (most common)  
- **Foundation Gap** → open an RFC; do not add to foundation without review

See: `TRACEABILITY_MATRIX.md` — the working tool for Phase II.

**Planned Experience Patterns (validated during this phase):**

| Pattern | Status | Human Problem |
|---|---|---|
| `waiting-for-me` | ✅ canonical | No signal when a relationship needs attention |
| `attention-layer` | proposed | WFM must reach the person in their existing context |
| `daily-reflection` | proposed | No structured moment to survey meaningful relationships |
| `relationship-inbox` | proposed | Multiple relationship signals with no prioritization |
| `silent-reminder` | proposed | Relationships where presence matters more than words |

---

## Phase III — Knowledge Validation (future)

**Question:** Does the world understand what Cuqou is?

**Reference Implementation:** cuqou-web

Website proves that:
- AI systems can reason correctly about Cuqou concepts
- Search engines surface Cuqou concepts when people ask about relationships
- People who read about Cuqou understand what it is and why it exists

**Planned artifacts:**

| Artifact | What it proves |
|---|---|
| Knowledge Center | Humans understand the ontology |
| `llms.txt` | LLMs find and apply Cuqou concepts |
| JSON-LD exports | Search and AI can reference canonical definitions |
| AI Plugin Docs | Developers can build on the ontology |
| FAQ | Edge cases are addressed without expanding the foundation |

---

## Phase IV — External Ecosystem (future)

**Question:** Can other systems build on the Cuqou Relationship Ontology?

Begins after Phase III — when the foundation has been proven by both behavioral and knowledge validation.

| Artifact | Purpose |
|---|---|
| `CONFORMANCE.md` | Defines what "Cuqou compatible" means structurally |
| MCP Server | Exposes ontology as tools for AI agents |
| Semantic API | Query-able access to concepts, patterns, decision rules |
| LLM Training Package | Curated definitions for fine-tuning or RAG |

---

## Ontology KPIs

These measure whether Foundation Freeze was architecturally sound — not whether the product is successful.

| KPI | Meaning | Target |
|---|---|---|
| **Ontology Coverage** | What % of features can be explained by the existing ontology without creating new concepts? | ≥ 90% during Phase II |
| **Foundation Stability** | How many new structural layers were added during Validation? | 0 |
| **Decision Traceability** | Can every system recommendation be traced back to the Axiom? | 100% |
| **Pattern Reusability** | Can new Experience Patterns use the existing template without modification? | Yes for all Phase II patterns |

If all four pass at the end of Phase II, Foundation Freeze is validated.  
If any fail, the RFC process opens to address the specific gap.

---

## Architecture: What Cuqou Is Building

```
Living Ontology  (Source Code)
        │
        ▼
Relationship Runtime  (Execution Layer)
        │
  ──────┼──────────────────────────────
        │
        ├── LINE Mini App      ← Reference Implementation
        ├── AI Chat Plugin
        ├── MCP Server
        ├── cuqou-web
        └── Future APIs, SDKs, Enterprise
```

**Ontology = Source Code.** Defines what is true, what governs, how to reason.  
**Relationship Runtime = Execution Layer.** Compiles the Ontology into Experience.  
**Products = Applications.** Each is an expression of the Runtime in a specific context.

Cuqou's product is not the Mini App. The Mini App is a Reference Implementation.  
Cuqou's product is the **Relationship Runtime** — the layer that transforms Living Ontology into verifiable human experience.

**The Feedback Loop:**

```
Living Ontology
        │
        ▼
Relationship Runtime
        │
        ▼
Experience
        │
        ▼
Human Behavior
        │
        ▼
Evidence
        │
        ▼
cuqou-cases
        │
        ▼
Ontology Refinement
        │
        └──────────────────┐
                           ▼
               Living Ontology (updated)
```

This loop is why the Ontology is *living*. Not because files are edited. Because human evidence continuously validates and refines the source.

**Phase III question (revised):**  
*"Can we make the Living Ontology into a Runtime that reliably produces authentic relationship experience?"*

When the answer is yes — the Ontology becomes a Platform.

## The Repository Ecosystem

```
cuqou-ontology          ← Living Ontology / Source (this repository)
        │
        ▼
cuqou-mvp (LINE Mini App)    ← Relationship Runtime / Reference Implementation
cuqou-web                    ← Knowledge Layer / Reference Implementation
        │
        ▼
Behavioral Evidence
        │
        ▼
cuqou-cases             ← Evidence Layer (Phase II → Phase III)
```

**`cuqou-cases`** — the Evidence Layer of the Living Ontology.  
Not marketing. Not testimonials.

| What it contains | Purpose |
|---|---|
| Case Studies | How specific human problems were resolved |
| Anonymous Patterns | Recurring behaviors observed across users |
| Validation Results | Phase II KPI outcomes |
| Human Transformations | Before/after documented per Experience Pattern |
| Lessons Learned | Where the Foundation was challenged or confirmed |

`cuqou-cases` is deferred until Phase II produces evidence worth recording.  
It will become the primary input for Phase III Knowledge Validation and Phase IV Externalization.

---

## RFC Process

Any proposed change to the foundation must go through the RFC process.  
See: `rfc/RFC-INDEX.md`

New Experience Patterns do not require an RFC — they require the canonical template, Relationship Truth Review, and Maintainer approval.

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/roadmap*  
*License: CC BY 4.0 — Attribution required*

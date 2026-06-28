---
version: "1.0"
status: canonical
uri: https://ontology.cuqou.com/roadmap
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---

# Cuqou Relationship Ontology — Roadmap

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

If validation of the foundation reveals a structural gap, that gap is addressed through the RFC process — not by adding layers informally.

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
Every concept in this ontology can answer: *"How does this serve Relationship Truth?"*  
Every Experience Pattern can answer: *"What human problem does this resolve — and what must it never become?"*

---

## Phase II — Validation (current)

**Goal:** Prove that the foundation is sufficient for real implementations without adding new structural layers.

**Method:** Build additional Experience Patterns and observe whether each one fits the existing foundation or exposes a gap.

**Planned Experience Patterns:**

| Pattern | Status | Human Problem it addresses |
|---|---|---|
| `waiting-for-me` | ✅ canonical | No signal when a relationship needs attention |
| `attention-layer` | proposed | WFM must reach the person in their existing context |
| `daily-reflection` | proposed | No structured moment to survey the state of meaningful relationships |
| `relationship-inbox` | proposed | Multiple relationship signals with no prioritization |
| `silent-reminder` | proposed | Relationships where presence matters more than words |

**Validation criterion:**  
If all planned patterns can be fully written using existing Layers 0–3 without adding new concepts, the foundation passes Phase II.

If a gap is found, it is addressed by RFC — not by informal structural expansion.

**Reference Implementations (outside this repository):**
- **Cuqou LINE Mini App** — proves the Ontology can produce real user experience
- **cuqou-web** — proves the Ontology can explain itself to humans and AI (Knowledge Center, JSON-LD, llms.txt)

---

## Phase III — Externalization (future)

**Goal:** Make the Cuqou Relationship Ontology usable by external systems, AI agents, and developers.

**Planned:**

| Artifact | Purpose |
|---|---|
| `CONFORMANCE.md` | Defines what it means for a system to be "Cuqou compatible" |
| MCP Server | Exposes ontology concepts as tools for AI agents |
| JSON-LD exports (expanded) | Machine-readable knowledge for search and AI |
| `llms.txt` | AI-optimized entry point for LLM reasoning |
| Semantic API | Query-able access to concepts, patterns, and decision rules |
| LLM Training Package | Curated concept definitions for fine-tuning or RAG |

Phase III begins after Phase II validation is complete — when the foundation has been proven by implementation, not just by theory.

---

## What "Cuqou Compatible" Will Mean (CONFORMANCE preview)

A system that claims to implement Cuqou concepts must:

1. **Relationship Truth Review** — every experience passes the canonical check
2. **Human Agency** — no action reaches another person without explicit human approval
3. **Human Contribution** — the person's voice is preserved in every expression
4. **Intent Provenance** — the system can distinguish human-initiated from AI-initiated intent
5. **Pattern compliance** — Experience Patterns follow the canonical template and name their Anti-patterns

Using the words "CPP" or "CRP" is not sufficient for Cuqou compatibility.  
Compatibility is structural — it requires implementing the principles, not just the vocabulary.

See: `CONFORMANCE.md` (to be written in Phase III)

---

## RFC Process

Any proposed change to the foundation must go through the RFC process.  
See: `rfc/RFC-INDEX.md`

New Experience Patterns do not require an RFC — they require the canonical template and Maintainer approval.

---

*Cuqou Relationship Ontology — https://ontology.cuqou.com/roadmap*  
*License: CC BY 4.0 — Attribution required*

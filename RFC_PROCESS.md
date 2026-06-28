# Cuqou Ontology — RFC Process

**Version:** 1.0  
**Status:** Canonical  
**Modeled after:** IETF RFC process, adapted for relationship knowledge governance

---

## Purpose

The RFC (Request for Concept) process governs how new concepts enter the Cuqou Relationship Ontology.

This process exists because:
- Concepts proposed in isolation may conflict with existing canonical definitions
- AI agents, contributors, and founders may identify new concepts independently
- Without a formal process, the ontology will fragment

The RFC process ensures every new concept is reviewed against the Constitution before any file is created.

---

## Who May Propose

Anyone may submit an RFC:
- Founders
- Contributors
- Researchers
- AI agents (Claude Code, Cursor, Codex, etc.)

However, **only the Cuqou Ontology Maintainer may approve an RFC** and advance it to the Draft stage.

---

## RFC Lifecycle

```
Idea
 │
 ▼
RFC Submitted       ← rfc/RFC-XXXX-{concept-name}.md created
 │
 ▼
RFC Review          ← Maintainer checks against Constitution + existing concepts
 │
 ├── Rejected       ← documented with reason; RFC stays in rfc/ as historical record
 │
 ▼
RFC Accepted        ← status: accepted; concept added to CANONICAL_MAP as `draft`
 │
 ▼
Draft               ← concept files created using templates
 │
 ▼
Proposed            ← all 6 files complete; passes Canonicalization Gate
 │
 ▼
Canonical           ← Maintainer approves; CHANGELOG.md updated; version tagged
```

---

## RFC File Format

Create at: `rfc/RFC-{XXXX}-{concept-name}.md`  
Number: sequential, zero-padded to 4 digits (RFC-0001, RFC-0002, ...)

```markdown
---
rfc: {XXXX}
title: {Concept Name}
status: draft | accepted | rejected
proposed_by: {Founder | Contributor | AI Agent name}
date: {YYYY-MM-DD}
affects:
  - {existing-concept-id}
  - {existing-concept-id}
---

# RFC-{XXXX} — {Concept Name}

## Proposed Canonical Question

> {The one human problem this concept answers}

## One-Sentence Proposal

{What this concept is, in 30–50 words, with no product references}

## Why This Concept Needs a New Name

{Why existing terminology is insufficient. Reference CONSTITUTION Principle 4.}

## Canonical Independence Check

> If every Cuqou application disappeared tomorrow, would this concept still be
> meaningful to someone studying or maintaining human relationships?

Answer: {Yes / No}  
Explanation: {Why}

## Affected Existing Concepts

| Concept | How it is affected |
|---|---|
| {concept-id} | {relationship or potential conflict} |

## Negative Definition (preliminary)

This concept is NOT:
- {term} — {reason}
- {term} — {reason}

## Proposed Category

{concept | protocol | state | artifact | system}

## Reviewer Notes

{Left blank by proposer — filled in during review}

## Decision

Status: {draft | accepted | rejected}  
Reason: {documented by Maintainer}  
Date: {YYYY-MM-DD}
```

---

## Review Criteria

The Maintainer evaluates each RFC against:

1. **Principle 1 (Scope)** — Is this within relationship maintenance?
2. **Principle 4 (Naming Authority)** — Can it be expressed with existing terminology?
3. **Principle 9 (Canonical Independence)** — Is it product-independent?
4. **Canonical Concept Test** — One enduring human problem + consistent interpretability?
5. **Conflict check** — Does it conflict with or duplicate any existing canonical concept?

An RFC may be:
- **Accepted** — proceed to Draft
- **Rejected** — documented with reason; may be resubmitted with revisions
- **Merged** — the proposed concept is better expressed as an extension of an existing concept

---

## RFC Index

RFCs are tracked in `rfc/RFC-INDEX.md`.

| RFC | Title | Status | Proposed By | Date |
|---|---|---|---|---|
| RFC-0001 | *(first RFC to be submitted)* | — | — | — |

---

## Notes for AI Agents

If you are an AI agent proposing a new concept:
1. Check `CANONICAL_MAP.md` first — the concept may already exist
2. Check existing concept files for overlap
3. Submit an RFC file; do NOT create concept files directly
4. Do not advance your own RFC — only the Maintainer may approve

The RFC process protects the ontology from concept proliferation and ensures human oversight of every addition.

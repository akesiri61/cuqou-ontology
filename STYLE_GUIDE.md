# Cuqou Ontology — Style Guide

**Version:** 1.0  
**Status:** Canonical  
**Applies to:** All files in `vocabulary/`, `knowledge/`, `schema/`, `exports/`

This guide defines writing standards for the Cuqou Relationship Ontology. All contributors and AI agents MUST follow these rules when creating or modifying canonical content.

---

## Language and Tone

### Voice
- MUST use active voice: "CPP prepares the person" not "the person is prepared by CPP"
- MUST write for a human reader who has no knowledge of Cuqou as a product
- SHOULD write at a reading level accessible to an educated non-specialist

### Prohibited language
- MUST NOT reference Cuqou the app, LINE, Mini App, or any specific implementation
- MUST NOT use marketing language ("powerful", "revolutionary", "seamless", "cutting-edge")
- MUST NOT use hedging language in definitions ("kind of", "sort of", "basically", "essentially")
- MUST NOT use passive voice in definitions
- SHOULD NOT use jargon without definition

### Terminology consistency
- Canonical concept names MUST be written exactly as defined (e.g., "Conversation Preparation Protocol", not "conversation preparation protocol" or "CPP protocol")
- First mention of a concept name MUST include its abbreviation in parentheses: "Conversation Preparation Protocol (CPP)"
- Subsequent mentions MAY use the abbreviation alone

---

## Definition Standards

### One Sentence
Every concept MUST have a single-sentence canonical definition that:
- States what the concept IS (not what it does, not why it matters)
- Contains no product references
- Can be understood without reading anything else
- Is 30–50 words

### Canonical Question
Every concept MUST have exactly one Canonical Question — the enduring human problem the concept was created to answer.

Format:
- A genuine question a person would ask
- Written in first person: "How should I..." / "ฉันควร..."
- No more than 15 words

### Definition Body
The definition body MUST answer in order:
1. What it is
2. Why it exists (the problem it addresses)
3. When to use it
4. When NOT to use it
5. What it is not (Negative Definition)

---

## Negative Definition (REQUIRED for all concepts)

Every canonical concept MUST include a Negative Definition.

Purpose: prevent misapplication by humans and incorrect mapping by AI systems.

Format:
- List of 5–10 things the concept is NOT
- Each item MUST include a brief reason
- Use table format in `.md` files

Example:
```
| CPP is not... | Because... |
|---|---|
| A script | CPP does not tell you what to say |
```

---

## Canonical Independence (REQUIRED for all concepts)

Every canonical concept MUST include a statement of its independence from Cuqou products.

This section MUST answer:
1. Who can use this concept without knowing Cuqou exists?
2. Would this concept remain meaningful if Cuqou ceased to exist?

If the answer to question 2 is "no", the concept is not eligible for canonicalization.

---

## LLM Hints (REQUIRED in vocabulary YAML)

Every concept MUST include `llm_hints` — a list of natural-language questions a person might ask that this concept is designed to answer.

Rules:
- Include both Thai and English examples
- Write as real questions people ask, not keywords
- Minimum 5 hints, maximum 15
- MUST NOT include the concept name itself as a hint

Purpose: help AI systems map natural-language queries to the correct canonical concept.

---

## File Naming

| File type | Naming convention | Example |
|---|---|---|
| Vocabulary | `{id}.yaml` | `cpp.yaml` |
| Knowledge | `{id}.md` | `cpp.md` |
| Reasoning | `{id}.reasoning.md` | `cpp.reasoning.md` |
| Examples | `{id}.examples.md` | `cpp.examples.md` |
| Schema | `{id}.schema.json` | `cpp.schema.json` |
| JSON-LD export | `{id}.jsonld` | `cpp.jsonld` |

Concept IDs:
- MUST be lowercase
- MUST use hyphens for multi-word IDs: `relationship-decay`, `waiting-for-me`
- MUST be unique across all categories
- MUST NOT change after canonicalization

---

## Frontmatter (REQUIRED in all .md files)

Every `.md` file MUST begin with YAML frontmatter:

```yaml
---
id: {concept-id}
version: "{major}.{minor}"
status: draft | proposed | canonical | deprecated
category: concept | protocol | state | artifact | system
uri: https://ontology.cuqou.com/{id}
license: CC BY 4.0 — Cuqou (https://cuqou.com)
---
```

---

## Examples

Examples MUST be in a separate file (`{id}.examples.md`), never embedded in the canonical definition file.

Rules:
- Examples MUST be realistic, not contrived
- Examples MUST NOT reference Cuqou features
- Examples MUST cover at least 2 different relationship types (personal, professional, etc.)
- Examples MUST include a "without this concept" and "with this concept" contrast

---

## What belongs in which file

| Content | File |
|---|---|
| Structured metadata, aliases, LLM hints | `vocabulary/{id}.yaml` |
| Canonical definition, FAQ, Negative Definition | `knowledge/{category}/{id}.md` |
| Design decisions, alternatives rejected, open questions | `knowledge/{category}/{id}.reasoning.md` |
| Situational examples | `knowledge/{category}/{id}.examples.md` |
| Validation rules | `schema/{id}.schema.json` |
| AI/Search consumption | `exports/{id}.jsonld` |

Content MUST NOT be duplicated across files. If it belongs in reasoning, it does not belong in the definition.

---

## RFC Keywords

This guide uses RFC 2119 keywords with the following meanings:
- **MUST** / **MUST NOT** — absolute requirement; violation invalidates canonicalization
- **SHOULD** / **SHOULD NOT** — recommended; deviation requires documented justification
- **MAY** — optional; no justification required

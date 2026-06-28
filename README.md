# Cuqou Ontology

The Cuqou Relationship Ontology is the canonical knowledge layer for concepts, protocols, and ideas that Cuqou has developed around human relationship maintenance.

This repository is the **single source of truth** for all relationship knowledge published by Cuqou — whether on the website, in AI systems, via MCP Server, or in future applications.

## Repository Structure

```
cuqou-ontology/
│
├── MANIFESTO.md         — Why this ontology exists
├── CONSTITUTION.md      — Rules governing what becomes canonical
├── CANONICAL_MAP.md     — Index of all canonical concepts
│
├── vocabulary/          — Machine-readable concept definitions (YAML)
├── knowledge/           — Human-readable concept explanations (Markdown)
│   ├── concepts/
│   ├── protocols/
│   ├── states/
│   ├── artifacts/
│   └── systems/
├── schema/              — Schema.org, JSON-LD, RDF exports
├── exports/             — Generated files (llms.txt, knowledge graph, embeddings index)
└── mcp/                 — MCP Server resources and manifest
```

## Layers

| Layer | Location | Purpose | Audience |
|---|---|---|---|
| Vocabulary | `vocabulary/` | Identifiers and structured metadata | Machines |
| Knowledge | `knowledge/` | Canonical definitions and explanations | Humans |
| Schema | `schema/` | Interoperability formats | AI systems |
| Exports | `exports/` | Published artifacts | Web, APIs |
| MCP | `mcp/` | AI tool integration | LLM agents |

## Contributing

All changes to canonical concepts require review by the Cuqou Ontology Maintainer.  
See `CONSTITUTION.md` for governance rules.

New concept proposals must pass the **Canonical Independence Test** (Principle 9).

## Publications

- Web: `https://cuqou.com/knowledge/`
- LLMs: `https://cuqou.com/llms.txt`
- MCP: *(planned)*

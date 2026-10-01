# Vortex Personal Intelligence — v0.1

This is the first local, Git-friendly personal intelligence corpus for Vortex.

The corpus follows the current Open Knowledge Format (OKF) v0.2 model: Markdown concept files with YAML frontmatter, a directory hierarchy for navigation, and ordinary Markdown links for relationships.

## What this is

This is **not** a database, RAG index, or chatbot memory dump.

It is the durable knowledge layer from which those systems can later be derived.

The intended architecture is:

```text
External sources
      ↓
Raw imports
      ↓
Extraction / curation
      ↓
OKF knowledge corpus  ← source of truth
      ↓
Indexes / embeddings / graph (derived later)
      ↓
Context orchestrator
      ↓
Agents / LLMs
```

## Current status

`v0.1` is intentionally incomplete. It is a **seed corpus**, created from accumulated conversation context. It should be reviewed by the user before being treated as authoritative.

## First next step

Add raw source material under `sources/` or a future `raw/` directory, run the extraction prompt in `prompts/extraction-prompt.md`, review the proposed concepts, and commit the changes.

## Git

```bash
git add .
git commit -m "Initialize Vortex personal intelligence corpus"
# then add your remote and push
```

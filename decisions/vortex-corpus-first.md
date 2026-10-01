---
type: Decision
title: Corpus-First Vortex Architecture
description: Decision to start Vortex with a human-readable OKF knowledge corpus before specialized databases.
tags: [decision, vortex, okf, architecture, knowledge]
context_priority: P0
evidence_level: explicit
temporal_status: current
status: active
confidence: 0.98
generated: { by: openai, at: 2026-10-01 }
sources:
  - id: conversation-context
    resource: /sources/conversation-context.md
---

# Decision

Start the personal intelligence system with a local, human-readable folder/OKF corpus rather than immediately migrating the information into Postgres, vector databases, or a graph database.

# Rationale

- The ontology is not yet known.
- Folder structure makes information scarcity and density visible.
- Markdown is inspectable by humans and coding agents.
- Git provides history.
- Derived stores can be added later.
- The source representation remains portable.

# Architecture hypothesis

`raw sources → extraction/curation → OKF corpus → derived retrieval/graph/indexes → context orchestrator → agent tools → LLM`

# Status

Current architectural direction.

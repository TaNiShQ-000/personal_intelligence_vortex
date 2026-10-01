---
type: Project
title: Vortex Personal Intelligence
description: Persistent AI context and memory system intended to understand and work continuously with one person.
tags: [project, vortex, ai, memory, agents]
context_priority: P0
evidence_level: demonstrated
temporal_status: current
status: stable
confidence: 0.97
generated: { by: openai/gpt-5.6-luna, at: 2026-10-01T17:30:00Z }
sources:
  - id: conversation-context
    resource: /sources/conversation-context.md
---
# Project thesis

Build a persistent personal intelligence layer where a human-readable knowledge corpus acts as the source of truth and agents retrieve only the context relevant to the current task.

# Current architectural direction

```text
Sources
  ↓
Raw imports
  ↓
Extraction / curation
  ↓
OKF corpus
  ↓
Derived indexes / graph / embeddings
  ↓
Context orchestrator
  ↓
Agent tools
  ↓
LLM
```

# Current hypothesis

A well-structured personal context corpus may provide more useful continuity than repeatedly pasting a giant personal profile into a model context window.

# Research direction

Test this against historical queries using baseline, giant-profile, and tool-retrieval conditions.

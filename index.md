---
type: Knowledge Bundle
title: Vortex Personal Intelligence Corpus
description: Human-readable, machine-readable personal intelligence corpus for Vortex.
okf_version: "0.2"
tags: [vortex, personal-intelligence, knowledge, context]
status: active
---

# Vortex Personal Intelligence Corpus

This repository is the durable, human-readable source of truth for the Vortex Personal Intelligence Layer.

## Start here

- [Ontology](ontology.md) - Current working taxonomy and metadata contract.
- [Current State](state/index.md) - What matters now.
- [Identity](identity/index.md) - Who the user is and career/background.
- [Goals](goals/index.md) - Current and long-term objectives.
- [Decisions](decisions/index.md) - Decisions and reasoning.
- [Capabilities](capabilities/index.md) - Technical and business capability.
- [Projects](projects/index.md) - Active and historical project context.
- [Preferences](preferences/index.md) - How the user prefers to work and communicate.
- [Experiences](experiences/index.md) - Important historical experiences.
- [Observations](observations/index.md) - Cross-conversation patterns and tensions.
- [Content](content/index.md) - Personal-brand/distribution context.
- [Sources](sources/index.md) - Provenance and source-scope descriptors.
- [Prompts](prompts/context-anchor.md) - Instructions for agents consuming this corpus.

## Current architecture hypothesis

`raw sources → extraction → OKF corpus → derived indexes/graph/embeddings → context orchestrator → agent tools → LLM`

The corpus comes first. Derived infrastructure comes later.

## State rule

Historical information is not current information. Decisions and current state should be updated explicitly rather than inferred from old project documents.

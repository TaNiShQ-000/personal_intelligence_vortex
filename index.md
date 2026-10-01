---
okf_version: "0.2"
---
# Vortex Personal Intelligence Corpus

This repository is the first local corpus representing the user's durable context for AI collaboration.

It is intentionally **human-readable first** and **machine-queryable second**. The current ontology is provisional and should evolve from observed data rather than premature database design.

## Core context

* [Identity](identity/) - Core identity, background, and current professional self-concept.
* [State](state/) - Current situation, priorities, constraints, and open loops.
* [Goals](goals/) - North-star and strategic goals.
* [Capabilities](capabilities/) - Demonstrated technical and business capabilities.
* [Preferences](preferences/) - Stable communication, work, and decision preferences.

## Reasoning and history

* [Decisions](decisions/) - Important decisions and their rationale.
* [Beliefs](beliefs/) - Explicit and inferred operating principles.
* [Experiences](experiences/) - Career, projects, experiments, failures, and lessons.
* [Observations](observations/) - Cross-conversation patterns, contradictions, and leverage.

## Work and identity in motion

* [Projects](projects/) - Active and historical projects.
* [Content](content/) - Personal-brand and creator context.
* [Relationships](relationships/) - Personal context that materially affects planning or priorities.

## Provenance

* [Sources](sources/) - Description of the source layers used to create this initial corpus.
* [Ontology](ontology.md) - Provisional Vortex concept taxonomy and metadata extensions.
* [Setup](SETUP.md) - Local Git setup and next ingestion steps.
* [Agent Instructions](AGENTS.md) - How agents should read and update the corpus.
* [Seed Corpus Prompt](prompts/seed-corpus-prompt.md) - Prompt for generating a first corpus from large source exports.
* [Extraction Prompt](prompts/extraction-prompt.md) - Reusable prompt for incremental conversion of new source material into OKF concepts.
* [Context Anchor](prompts/context-anchor.md) - Runtime instruction for agents consuming the corpus.

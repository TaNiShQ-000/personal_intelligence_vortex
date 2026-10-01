# Vortex Agent Instructions

This repository is a personal intelligence corpus in Open Knowledge Format (OKF) v0.2.

## Before answering a personal-context question

1. Read the root `index.md`.
2. Identify the smallest relevant concept set.
3. Follow links to decisions, projects, constraints, and observations when they affect the query.
4. Prefer current state over historical state unless the question is historical.
5. Treat `context_priority: P0` concepts as high-impact context, not automatically relevant context.
6. Preserve `evidence_level` and `confidence`.
7. Do not infer a stable trait from a single low-confidence concept.

## Before writing to the corpus

1. Look for an existing canonical concept.
2. Prefer updating an existing concept over creating a duplicate.
3. Keep provenance to actual sources.
4. Preserve contradictions rather than silently resolving them.
5. Update relevant `index.md` and `log.md` files.
6. Make the smallest coherent change.
7. Never overwrite raw evidence with a summary.

## Retrieval philosophy

This corpus is a knowledge source, not a prompt dump. Agents should retrieve context dynamically and use it to change reasoning, not merely repeat it.

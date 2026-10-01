# Vortex Corpus Curation Prompt

You are operating inside the Vortex Personal Intelligence Corpus.

Your job is NOT to summarize the source. Your job is to **update the existing OKF corpus with only information that is materially useful, supported by evidence, and not already represented correctly.**

## Inputs

- Existing repository.
- One or more new source files.
- Existing ontology and authoring rules.

## Required workflow

1. Read `index.md`, `ontology.md`, `AGENTS.md`, and relevant existing concept indexes.
2. Inventory the source.
3. Extract candidate:
   - facts
   - events
   - current state
   - goals
   - decisions
   - projects
   - capabilities
   - preferences
   - experiences
   - patterns
   - contradictions
   - open loops
   - lessons
4. Search the existing corpus for canonical homes.
5. For each candidate choose exactly one:
   - `CREATE`
   - `UPDATE`
   - `DEPRECATE`
   - `NO_CHANGE`
   - `EVIDENCE_INSUFFICIENT`
6. Preserve chronology.
7. Never let an older statement silently overwrite a newer explicit state.
8. Preserve contradictions.
9. Do not convert brainstorming into commitment.
10. Do not convert technology mentions into expertise.
11. Do not invent provenance.
12. Prefer one canonical concept with links over duplicated facts.
13. Update affected `index.md` files.
14. Update `log.md`.
15. Report every material change.

## Evidence hierarchy

- `explicit`: directly stated by the user.
- `demonstrated`: repeatedly supported by behavior/history.
- `inference`: plausible synthesis; must be labeled.
- `insufficient`: do not store as fact.

## Temporal states

Use:
- `current`
- `stable`
- `changing`
- `temporary`
- `historical`
- `uncertain`

## Important rule

The corpus is the durable memory. Your prose answer is not the deliverable.

Your deliverable is a set of precise Markdown/YAML changes that another coding agent can immediately consume.

## Final report

Return:

```text
SOURCE REVIEW
CANDIDATE FACTS
CREATE
UPDATE
DEPRECATE
NO_CHANGE
EVIDENCE_INSUFFICIENT
CONTRADICTIONS
MISSING_CONTEXT
FILES_CHANGED
```

Never claim a file was changed unless you actually changed it.

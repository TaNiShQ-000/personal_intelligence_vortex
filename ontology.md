# Vortex v0.1 Ontology

The ontology is intentionally small. It is a working taxonomy, not a final schema.

## Design principles

1. **Markdown is the durable source of truth.** Derived indexes, embeddings, graphs, and databases may be rebuilt.
2. **Folder hierarchy is for progressive disclosure, not relational modeling.** OKF supports directory navigation while concepts connect through ordinary links.
3. **A concept should represent one useful unit of knowledge.** Split documents when separate retrieval would be useful.
4. **Current state is separate from history.** Historical facts should not silently overwrite current state.
5. **Decisions are first-class.** Preserve rationale, alternatives, constraints, outcomes, and lessons.
6. **Evidence is first-class metadata.** Never turn an inference into a fact silently.
7. **The ontology must be allowed to change.** New types should appear because the corpus needs them.

## Initial concept families

| Family | Typical `type` values | Purpose |
|---|---|---|
| identity | `Identity`, `Professional Identity`, `Background` | Who the user is and how they self-describe |
| state | `Current State`, `Priority`, `Constraint`, `Open Loop` | What is true now |
| goals | `Goal`, `Strategic Objective` | Desired future state |
| capabilities | `Capability`, `Skill` | Demonstrated or developing ability |
| preferences | `Preference` | Stable ways the user prefers things done |
| decisions | `Decision` | Choices plus reasoning and outcome |
| beliefs | `Principle`, `Belief` | Explicit or inferred operating principles |
| projects | `Project`, `Experiment` | Work streams and experiments |
| experiences | `Experience`, `Failure`, `Success`, `Learning` | Historical evidence |
| content | `Content Strategy`, `Audience`, `Content Experiment` | Creator/distribution context |
| observations | `Pattern`, `Contradiction`, `Leverage Opportunity` | Cross-source synthesis |
| relationships | `Relationship Context` | Personal context when decision-relevant |
| sources | `Source` | Provenance and source mapping |

## Vortex-specific metadata

These are producer-defined extensions on top of OKF's base fields:

- `context_priority`: `P0`–`P3`
- `evidence_level`: `explicit`, `demonstrated`, `inference`, `insufficient`
- `temporal_status`: `current`, `stable`, `changing`, `temporary`, `historical`, `uncertain`
- `status`: `draft`, `stable`, `deprecated`
- `sensitivity`: `normal`, `personal`, `restricted`
- `confidence`: numeric 0–1 when useful
- `last_confirmed`: ISO 8601 timestamp when known

## When to create a new document

Create a new concept when the information is likely to be retrieved independently, has its own lifecycle, or participates in relationships with other concepts.

Prefer links between concepts over repeating large blocks of the same information.


## v0.1 expansion

Additional concept types observed in the seed corpus:
- `Timeline`
- `Pattern`
- `Contradiction`
- `Experience`
- `Content Strategy`
- `Current State`

These were added because they carry retrieval value that would be lost if flattened into ordinary facts.

## Metadata contract

Use when applicable:
- `type`
- `title`
- `description`
- `tags`
- `context_priority`
- `evidence_level`: explicit / demonstrated / inference / insufficient
- `temporal_status`: current / stable / changing / temporary / historical / uncertain
- `status`: active / draft / exploratory / deprecated / archived
- `confidence`
- `generated`
- `sources`

## Canonical-source rule

Markdown concepts are authoritative. Any relational store, graph, vector index, or search index created later is derived and rebuildable.

## Update rule

Prefer updating canonical concepts over duplicating facts. Preserve historical state where useful.

## Evidence rule

LLM-generated text is not evidence. Material assertions must trace to user statements, demonstrated repeated behavior, or clearly labeled inference.

## Privacy rule

Only retain personal context that is relevant to the intended intelligence system. Do not infer sensitive attributes.

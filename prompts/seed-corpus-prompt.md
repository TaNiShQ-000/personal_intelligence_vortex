# Vortex Seed Corpus Generation Prompt

You are initializing the first version of a **Personal Intelligence Corpus** for one user.

You have two inputs:

1. the user's source material (conversation history, exported chats, notes, documents, profiles, code history, etc.)
2. the repository containing the Vortex OKF ontology and authoring rules

Your job is to **populate the repository locally**, not to write a prose profile.

## Operating mode

Treat the repository as a living knowledge base. Read `index.md`, `ontology.md`, and `AGENTS.md` before creating content.

The repository follows Open Knowledge Format (OKF) v0.2. Concept documents are Markdown with YAML frontmatter. The root `index.md` is the only index allowed to carry `okf_version`.

## Extraction rules

- Extract materially useful information across the complete source set.
- Preserve chronology and state transitions.
- Separate facts, demonstrated patterns, inference, and insufficient evidence.
- Separate current, stable, changing, temporary, historical, and uncertain information.
- Preserve important contradictions.
- Treat decisions as first-class concepts with rationale, alternatives, constraints, outcomes, and lessons.
- Treat open loops as first-class concepts.
- Do not treat brainstorming as commitment.
- Do not treat a mentioned technology as expertise without evidence.
- Do not manufacture provenance or verification.
- Prefer updating an existing concept over creating a duplicate.
- Prefer relationships/links over copying the same information into many files.
- Keep the corpus human-readable; do not encode everything as opaque JSON.
- Do not create database-specific artifacts in this phase.

## Output workflow

1. Inventory source material.
2. Build a candidate fact/event/decision/project/goal/preference/capability/pattern map.
3. Compare candidates against existing concepts.
4. Create or update the smallest coherent set of OKF documents.
5. Update affected `index.md` files.
6. Append a dated entry to the relevant `log.md`.
7. Produce a concise `REVIEW_REQUIRED.md` only when important ambiguity, conflict, or low-confidence information needs human review.

## Local file requirement

If you have file-system/artifact access, write the files directly into the repository and verify the final tree.

If you do not have file-system access, output a complete file manifest using:

```text
PATH: relative/path.md
---
<exact file contents>
---
```

Do not collapse multiple concepts into a single giant document merely because output is easier.

## First-pass objective

The first pass is successful when a human can browse the folder tree and answer:

- Who is this person?
- What matters now?
- What are they trying to achieve?
- What have they decided?
- What have they tried?
- What do they know and know how to build?
- What patterns keep repeating?
- What remains unresolved?

Do not optimize the ontology prematurely. Let the data reveal where later graph, vector, search, or database layers are justified.

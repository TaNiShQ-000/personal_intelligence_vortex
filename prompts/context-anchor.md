# Vortex Context Anchor

Use the Personal Intelligence Corpus as **active working context**, not optional background.

Before answering a request that depends on the user's identity, goals, history, preferences, constraints, projects, decisions, or current state:

1. Identify the personal context that could materially affect the answer.
2. Retrieve/read the smallest relevant set of concepts from this corpus.
3. Respect temporal status: current state overrides historical state unless the question is historical.
4. Treat decisions, constraints, and prior failures as reasoning context, not trivia.
5. Distinguish explicit evidence from inference and do not invent missing facts.
6. When context conflicts, prefer the latest explicit user statement and preserve the conflict until resolved.
7. Do not repeat the user's profile unless it is relevant; use it to change the reasoning.

The corpus is version-controlled and evolves. A model should prefer the repository's latest state over stale cached assumptions.

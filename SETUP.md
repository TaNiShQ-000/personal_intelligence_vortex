# Vortex Corpus — Local Setup

The archive is already a Git repository with its first local commit.

## 1. Put it on your machine

Extract the archive and enter the repository:

```bash
cd vortex-personal-intelligence-v0.1
```

## 2. Inspect it

```bash
tree -a -L 3
cat index.md
cat state/current-state.md
cat ontology.md
```

## 3. Connect your own Git remote

```bash
git remote add origin <YOUR_REPOSITORY_URL>
git branch -M main
git push -u origin main
```

The included `.git` directory already contains the initialization commit. Its local author is intentionally generic; you can amend it before pushing if you want your own Git identity attached to the first commit.

## 4. Next ingestion

Use `prompts/seed-corpus-prompt.md` for a larger source export, or `prompts/extraction-prompt.md` for incremental ingestion.

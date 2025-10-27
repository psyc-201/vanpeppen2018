<!-- Purpose: guide AI coding agents (and humans) to be productive in this replication-template repo. Keep short and focused. -->
# Copilot / AI agent instructions for this repo

Purpose: short, actionable guidance so an automated coding assistant can make safe, high-value edits in this replication template repository.

- Project snapshot
  - This repo is a replication project template for PSYCH 201a (see `README.md`).
  - Key directories: `writeup/` (Quarto report template: `writeup/Replication Report Template.qmd`), `data/` (raw or derived datasets), and `original_paper/` (source PDFs / materials).

- What you may safely change without extra approval
  - Edit and improve text, formatting, and code chunks inside `writeup/Replication Report Template.qmd` (this is a Quarto `.qmd` file). Example: update the YAML/meta header or adjust sections (Introduction, Methods, Results) directly in that file.
  - Add editorial clarifications, inline comments, figure/table captions, and small reproducibility notes into `writeup/` documents.

- What to avoid or treat as sensitive
  - Do NOT modify files in `original_paper/` (these are copies of source materials) unless explicitly asked; keep originals unchanged.
  - Do NOT alter raw files in `data/` without the user's explicit instruction. If you must transform data, create a new derived file and include provenance (a short note in the commit and in `writeup/`).

- Project-specific patterns and examples (from the repo)
  - Report template: open `writeup/Replication Report Template.qmd`. It uses a YAML header (title/author/date/format). Keep the YAML structure consistent when editing front matter.
    - Example header snippet (preserve keys and structure):

```
---
title: "Replication of Effects of Self-Explaining on Learning and Transfer ..."
author: "Van Peppen, L. M., ..."
format:
  html:
    toc: true
    toc_depth: 3
---
```

  - Use relative links when referencing repo files (e.g., `writeup/Replication Report Template.qmd`).

- Developer workflows discovered (explicitly found / validated)
  - No CI/workflows detected: there are no `.github/workflows` files in this template.
  - No package manifests detected: no `package.json`, `pyproject.toml`, `requirements.txt`, or `environment.yml` were found.
  - Quarto rendering (report authoring): the report file is a `.qmd`. To render locally (if Quarto is installed):

```bash
# render the report (requires Quarto installed on your machine)
quarto render writeup/Replication\ Report\ Template.qmd
```

- Integration, deps, and cross-component notes
  - There are currently no discovered code scripts or notebooks for data processing. If you add data processing, put provenance notes in `writeup/` and prefer small, descriptive filenames.
  - Keep any added analysis scripts in a clear location and reference them from the report (e.g., a `scripts/` or `analysis/` folder), and document how to run them in `README.md`.

- PR and commit guidance for AI agents
  - For content fixes to `writeup/`: make focused commits that change only the report or its assets. Use branch names like `fix/writeup-typo` or `feat/report-figure`.
  - When touching `data/`, include a short provenance file or commit message explaining the source and transformations (dates, code used).

If anything above is unclear or you want the agent to be more or less permissive (for example, to allow automated data cleaning), tell me which areas to expand or lock down and I will update this file.

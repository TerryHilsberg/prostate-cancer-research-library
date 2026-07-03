# Prostate Cancer Research Library

A patient-perspective research repository and web dashboard for prostate cancer diagnosis, risk stratification, treatment options, side effects, surveillance, and new evidence.

> Educational only — not medical advice. Use this to prepare questions for qualified clinicians.

## Local use

```bash
uv venv
. .venv/bin/activate
uv pip install mkdocs-material
mkdocs serve --dev-addr 0.0.0.0:8000
```

## Update workflow

The weekly Hermes job should:

1. Search configured sources for new studies and guideline updates.
2. Apply `docs/policies/selection-policy.md`.
3. File accepted items into the category pages under `docs/categories/` and/or weekly update pages under `docs/updates/`.
4. Keep patient-facing summaries separate from technical details.
5. Never make personal medical recommendations.

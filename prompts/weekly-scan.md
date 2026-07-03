# Hermes Weekly Prostate Cancer Research Scan Prompt

Update `/home/ceden/prostate-cancer-research-library` for the topic: prostate cancer diagnosis and treatment from the perspective of a potential patient.

Follow these rules:

1. Read `sources/sources.yaml`, `docs/policies/selection-policy.md`, and `docs/policies/medical-safety-policy.md`.
2. Search PubMed, guideline bodies, major oncology/urology journals, and configured web sources for new high-quality items from the last 7–14 days.
3. Focus on research relevant to diagnosis, risk stratification, treatment choice, active surveillance, recurrence, side effects, quality of life, and patient decision-making.
4. Score candidates using the rubric. Include only items scoring >= 7.5 unless there is a clear safety/guideline watchlist reason.
5. For each accepted item, write a concise note under `docs/updates/YYYY-MM-DD.md` with:
   - citation/title/authors/date/source URL/DOI/PMID if available
   - evidence type and population
   - category/categories
   - summary
   - main finding
   - patient relevance
   - limitations
   - safety/clinical cautions
   - whether it changes the decision map or a category page
6. Update `docs/updates/index.md` with a link to the new update.
7. If the evidence materially changes a category, update the relevant page in `docs/categories/`.
8. Never give personal medical advice. Frame findings as education and clinician-discussion prompts.
9. Run `mkdocs build --strict` from the repository root. If the repo is connected to GitHub, commit changes, push `main`, and deploy with `mkdocs gh-deploy --force --clean`; otherwise report that the local site was updated but not deployed.
10. Report a short summary of what changed and list the most clinically relevant new items.

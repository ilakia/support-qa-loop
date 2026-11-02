# Release checklist

Checked before publishing the repository.

## Method
- [x] Test set frozen before the first run (commit "Freeze 40 test questions") and never edited afterwards
- [x] Threshold tuned once on the separate tuning set, never on the test set
- [x] Escalation decided by keyword rules in code, never by the LLM
- [x] Baseline run_v1 made with no edits to articles or rules
- [x] Fixes change articles and rules only; every change listed in `docs/changelog.md`
- [x] Test-informed changes and deliberately unfixed problems stated openly
- [x] Manual spot check of 10 labels for run_v1 (10/10 agree)
- [x] Manual spot check of 10 labels for run_v2 (10/10 agree)

## Reproducibility
- [x] All four workflows exported to `workflows/` and run end to end on kb/v1 and kb/v2
- [x] Temperature 0 and seed 42 for the model
- [x] Results, labels and reports for both runs committed
- [x] Setup steps in the README (Ollama models, Node 24, n8n file access)

## Content and legal
- [x] All companies, people and data fictional; product name web-checked for collisions
- [x] Article owners are team labels, not person names
- [x] No real customer data, credentials or API keys in the repository
- [x] `docs/known_flaws.md` kept private (git-ignored)
- [x] LICENSE (MIT) for code, CC BY 4.0 stated for articles and docs
- [x] AI assistance stated in the README

## Publishing
- [x] Screenshots of the workflows in `screenshots/` (800 px wide)
- [ ] Public GitHub repository created and pushed

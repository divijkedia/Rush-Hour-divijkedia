# Submission checklist

Tick each box, then run `python code/check_submission.py`. The script verifies the parts it can; the rest is on you.

## Code and results (checked by the script)
- [ ] `code/starter_student.py` has no `raise NotImplementedError` left: cost function, blocking policy, and traffic-aware planner are written
- [ ] `python code/export_results.py` runs without errors from a fresh clone
- [ ] `results/metrics/ml_metrics.json` exists (held-out accuracy, macro F1, confusion matrix)
- [ ] Route files exist for **RUSH-1** and **RUSH-2**, distance-only and traffic-aware (`results/routes/`)
- [ ] At least one figure is in `results/figures/`
- [ ] RUSH-3 route files (optional stress test)

## Technical documents
- [ ] `docs/01_technical_report.md` is complete, including an error analysis of missed blocked roads
- [ ] The comparison uses the same blocking policy for both routes and reports length and cost
- [ ] Every improvement claim names its baseline and metric

## Consulting documents
- [ ] `docs/02_executive_summary.md` fits on one page
- [ ] `docs/03_service_model_and_rollout.md`
- [ ] `docs/04_funding_and_cost_model.md` (who pays, operator payment approach, rough pilot cost)
- [ ] `docs/05_stakeholder_map.md`
- [ ] `docs/06_risk_register.md` (includes the missed-blocked-road risk from your error analysis)
- [ ] `docs/07_assumptions_log.md` lists every assumption behind a number or a saving
- [ ] A short deck (about 5 slides) is in `presentation/`, ready for a 5-minute pitch

## Repository hygiene (not checked by the script)
- [ ] This is **our own** repository (created by our team, not the organizers' starter), and the organizers have access to it (Read access if it is private)
- [ ] `README.md` is filled in, with the team members and roles
- [ ] The repository has a clear commit history from the whole team
- [ ] No passwords, tokens, or personal data are committed
- [ ] You pushed the final commit before the deadline, and you know the commit you are submitting: [[FILL IN: commit hash or tag]]

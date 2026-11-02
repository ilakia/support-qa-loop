# Changelog

## v2 (run_v2), 2026-11-02

Fixes are based on the root causes found in `reports/report_run_v1.md`.
The 40 test questions were not changed. The similarity threshold (0.68)
was not changed.

### Knowledge base (kb/v1 → kb/v2)

| Article | Problem in v1 | Fix in v2 | Test question |
|---|---|---|---|
| DRV-002 | Outdated: routes available offline for 12 hours (`last_reviewed` 2024) | 48 hours, `last_reviewed` 2026-11-02 | Q22 |
| FD-002 | Contradicted FD-001: "at most 2 times in total" vs "up to 3" | "up to 3 times in total: the first attempt and two retries" | Q14 |
| ADR-006 (new) | No article on importing stops, although ADR-004 mentions file imports | New article "Importing stops from a file" | Q07 |

### Escalation rules (workflow 2)

- "billing" and "complaint" matched any question that contained them, so two
  how-to questions were escalated (Q18 "customer complaint", Q30 "billing team").
- They now only match intent phrases: billing problem / issue / question / error,
  make / file / have a complaint, formal complaint, I want to complain.
  The other seven keywords are unchanged.
- Trade-off: this rule change was found with test questions Q18 and Q30.
  A real complaint written without these phrases (for example "Your driver was
  rude") is no longer escalated.

### Result

| Run | Pass rate | wrong_answer | missing_content | retrieval_miss | dead_end | bad_escalation | made_up |
|---|---|---|---|---|---|---|---|
| run_v1 | 26/40 (65.0%) | 8 | 1 | 1 | 2 | 2 | 0 |
| run_v2 | 30/40 (75.0%) | 6 | 0 | 1 | 3 | 0 | 0 |

Changed labels: Q14, Q22 wrong_answer → correct; Q18, Q30 bad_escalation →
correct; Q07 missing_content → dead_end. No question got worse.

### Known limitations (deliberately not fixed)

- **Q07:** ADR-006 is now retrieved, but llama3.2:3b still answers
  "I don't know". The content gap is closed; the small model did not use it.
- **Q23, Q31 (dead_end):** blocked by the 0.68 threshold although the right
  article was found. Changing the threshold because of test questions would
  tune on the test set, so it stays.
- **Q03, Q05, Q10, Q12, Q15, Q25 (wrong_answer):** the right article was
  retrieved and contains the answer; the model answered wrongly. Rewriting
  these articles to make these exact questions pass would be teaching to the test.
- **Q20 (retrieval_miss):** FD-005 is not in the top 3 for this question.
- Keyword labels are deterministic and can miss correct answers worded
  differently; a 10-row manual spot check guards against this.

### Workflow changes

- Settings switched from v1 / run_v1 to v2 / run_v2 (workflows 1-4).
- Workflow 4: the spot-check count treats an empty CSV cell correctly.

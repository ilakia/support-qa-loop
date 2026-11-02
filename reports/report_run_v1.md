# QA report: run_v1

Generated: 2026-11-02 08:43 UTC

## Summary

**Pass rate: 26 / 40 (65.0%)** of the frozen test questions are labelled `correct`.

## Labels

| Label | Count | Questions |
|---|---|---|
| correct | 26 | (not listed) |
| wrong_answer | 8 | Q03, Q05, Q10, Q12, Q14, Q15, Q22, Q25 |
| missing_content | 1 | Q07 |
| retrieval_miss | 1 | Q20 |
| dead_end | 2 | Q23, Q31 |
| bad_escalation | 2 | Q18, Q30 |
| made_up | 0 |  |

## Per category

| Category | Questions | Correct | Pass rate |
|---|---|---|---|
| addresses | 8 | 5 | 62.5% |
| time_windows | 5 | 3 | 60.0% |
| failed_deliveries | 7 | 3 | 42.9% |
| driver_app | 5 | 2 | 40.0% |
| account | 6 | 4 | 66.7% |
| escalation | 6 | 6 | 100.0% |
| out_of_scope | 3 | 3 | 100.0% |

## Articles to fix

| Article | Problems |
|---|---|
| ADR-002 | Q03 wrong_answer: ADR-002 retrieved, but answer lacks: Remember this location |
| ADR-004 | Q05 wrong_answer: ADR-004 retrieved, but answer lacks: Admin |
| ADR-006 | Q07 missing_content: article ADR-006 does not exist in kb v1 |
| DRV-002 | Q22 wrong_answer: DRV-002 retrieved, but answer lacks: 48 hours |
| DRV-005 | Q25 wrong_answer: DRV-005 retrieved, but answer lacks: Android 11\|version 11 |
| FD-001 | Q15 wrong_answer: FD-001 retrieved, but answer lacks: Delivery options |
| FD-002 | Q14 wrong_answer: FD-002 retrieved, but answer lacks: 3 attempts\|3 delivery attempts\|three attempts\|three delivery attempts\|3 times\|three times |
| FD-005 | Q20 retrieval_miss: FD-005 not in top 3 (DRV-003, DRV-004, DRV-001) |
| TW-002 | Q10 wrong_answer: TW-002 retrieved, but answer lacks: Move stop |
| TW-004 | Q12 wrong_answer: TW-004 retrieved, but answer lacks: 2 hours |

## Rules and settings to check

- Q18 `bad_escalation`: escalated on keyword "complaint" but should be answered
- Q23 `dead_end`: said I don't know although DRV-002 was in the top 3 (route dont_know)
- Q30 `bad_escalation`: escalated on keyword "billing" but should be answered
- Q31 `dead_end`: said I don't know although ACC-005 was in the top 3 (route dont_know)

## Manual spot check

10 of 10 automatic labels confirmed by manual review.

## Before / after

| Run | Pass rate | correct | wrong_answer | missing_content | retrieval_miss | dead_end | bad_escalation | made_up |
|---|---|---|---|---|---|---|---|---|
| run_v1 | 26/40 (65.0%) | 26 | 8 | 1 | 1 | 2 | 2 | 0 |

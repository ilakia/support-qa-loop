# Similarity threshold: tuning decision

Decided once, on the 10 tuning questions in `data/tuning_questions.csv`
(5 answerable, 5 not answerable), never on the 40 test questions.
Run: `data/results_tuning.csv`, kb v1, nomic-embed-text, cosine similarity of
the question to its best-matching article (top-1 score).

| Group | Top-1 scores |
|---|---|
| Answerable (T01-T05) | 0.6855, 0.6898, 0.7423, 0.7429, 0.8196 |
| Not answerable (T06-T10) | 0.6619, 0.6633, 0.6856, 0.7039, 0.7141 |

- The planned value 0.45 never triggers: every question scores above 0.66.
- The two groups overlap, so no threshold separates them perfectly.
- Retrieval itself worked: the correct article was top-1 for all 5 answerable questions.

**Decision: threshold = 0.68**, just below the lowest answerable score.
It loses no answerable tuning question and blocks 2 of the 5 unanswerable ones.
The remaining unanswerable questions rely on llama3.2 replying "I don't know",
which it did for all 5 in the tuning run.

Alternatives considered: 0.715 blocks all 5 unanswerable questions but also
turns 2 answerable ones into dead ends; 0.45 has no effect.

Limitation: 10 questions is a small sample, and the margin (0.6855 vs 0.68)
is narrow, so the test set may behave differently. The threshold is not
changed after seeing test results.

# Evaluation protocol — not yet executed

## Research question
Does ICA improve detection of real reasoning errors in long-running AI projects compared with ordinary self-review and fresh-chat review?

## Conditions
A. Same-conversation self-review.
B. Fresh-conversation review with the original decision record.
C. ICA blind reconstruction followed by decision-record audit.

Use identical cases, comparable evidence, equivalent evaluation budgets where feasible, and multiple runs/models. Randomize condition order and prevent benchmark answer leakage.

## Dataset
Start with at least 30 cases, including:
- Known contradictions and incorrect factual claims.
- User-induced anchoring and overlooked viable alternatives.
- Unsupported certainty and objective drift.
- Correct plans with no planted defects (negative controls).
- Ambiguous cases where the right answer is uncertainty.

Separate dataset creation from adjudication. Preserve independent ground-truth notes and original evidence. Do not treat AI-generated labels alone as verified truth.

## Metrics
- True positives, false positives, false negatives.
- Precision, recall, and false-positive rate.
- Severity-weighted detection where justified.
- Time, tokens, and dollar cost.
- Agreement between independent human or evidence-based adjudicators.
- Variability across models and repeated trials.

Publish raw cases where privacy and rights allow, prompts, scoring rules, limitations, and unfavorable results. Do not invent test outcomes.

## Decision gate
Only claim superiority if independently adjudicated results support it. If ICA underperforms, document that and improve or simplify the protocol.

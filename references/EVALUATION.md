# ICA evaluation protocol — experimental; no performance result claimed

## Objective

Determine whether a complete project dossier and an independent fresh-session audit detect more **real** project coherence defects than ordinary AI self-review at reasonable cost. A secondary question is whether blind reconstruction adds value beyond the user's original one-file method.

## Compare four conditions

A. Same original conversation: ordinary request to review previous work.

B. Ordinary fresh chat: original assistant's short summary + "check coherence."

C. **ICA FULL**: full source-traceable handoff, then fresh-session audit.

D. **ICA BLIND**: blind reconstruction frozen before the decision/evidence packet, then audit.

To separate **dossier completeness** from **review protocol**, run at least one comparison in which B and C receive equal source material but different review instructions; otherwise superiority could simply reflect access to more evidence.

## Controlled cases

Begin with 30 mixed cases and expand only as resources allow:
- Actual user requirements conflicting with later AI design decisions.
- Source artifacts contradicting assistant claims.
- "Implemented" statements without working code or tests.
- Explicit allowed/rejected mockup versions.
- Hidden missing artifact versus truly absent implementation.
- User suggestion introducing a misleading anchor.
- Plans with wrong dependencies or ignored constraints.
- **Negative controls:** correct coherent projects where criticism would be a false positive.
- Inconclusive cases where neither model can verify truth.

Use actual consented or properly anonymized projects where possible; otherwise label synthetic data. The benchmark generator must not be the sole authority on its own expected answer. Preserve evidence and an independent adjudication log.

## Experimental rigor

1. Fix objectives, source records, and expected findings **before** running reviewers.
2. For each case, randomize conditions, use independent sessions, and log model/settings.
3. Control tools, evidence access, context/window limits, and computation budget; separately test real-world convenience.
4. Repeat sufficiently to estimate run-to-run variability.
5. Blind graders to the method when possible; reconcile adjudicator disagreements against sources.
6. Grade each specific finding as true, false, or undecidable; do not award points for generic suspicion.
7. Record failures to generate files, source omissions, or context contamination as first-class outcomes.

## Metrics

- Precision: fraction of flagged issues that are real.
- Recall: fraction of seeded/verified issues found.
- False-positive rate on known-correct decisions and cases.
- Missed critical defects, severity and repairability.
- Coverage: proportion of known required sources accounted for, with missing-file rate.
- Audit usefulness: percentage of findings with exact evidence pointers and feasible correction.
- Cost: tokens, money, wall time, human actions/approvals.
- Variation across models, projects, and runs.

## Publication and claims

Publish method, cases if legally shareable, expected results, model/settings, adjudication, and actual outputs (redacted where necessary). Report non-significant, neutral, and unfavorable outcomes. Do not claim ICA is proven more truthful, "forces honesty," or outperforms other methods without independently supported results. Do not fabricate adoption or benchmark numbers.

## Decision rule

If C shows no meaningful improvement over A/B, investigate whether transfer completeness, not protocol, is the bottleneck. If D fails to improve C, keep FULL as the lightweight default. If false positives rise materially, reduce aggressive criticism. Prefer the simplest method supported by data.

# ICA v0.2 templates

These headings are a content contract, not an invitation to fill blanks with invented facts. Use only source material actually accessible.

## ICA_HANDOFF.md (default single-file dossier)

```markdown
# ICA HANDOFF — [PROJECT]
Package version: ICA v0.2
COVERAGE: COMPLETE FOR INSPECTED SCOPE | PARTIAL
Export date: [date or unknown]
Original project context available: [scope]
Unknown/missing context: [explicit list]
Authorized transfer scope: [what the user permits]

## 1. Original user intent and authority
[Verbatim requirements with source pointers; goal, outcomes, non-negotiables, approvals, exclusions, supersessions.]

## 2. Project chronology and decisions
[When/why decisions happened, external stimuli, alternatives considered, approvals/rejections, latest governing state.]

## 3. Coherence and requirements traceability
| Objective | Requirement | Decision/approach | Artifact/source | Verified status | Acceptance test | Gap |
|---|---|---|---|---|---|---|

## 4. Verified present state
[Separate working, built-but-untested, simulated, proposed, blocked, failed, unknown.]

## 5. Remaining execution blueprint
[Steps, rationale, specific methods, prerequisites, owners, tests, decision gates, cost/risks.]

## 6. Artifact manifest and approval restrictions
| ID | Path/title | Source | Version | Approval | Accessibility | Representation | Relevant scope |
|---|---|---|---|---|---|---|---|

## 7. Embedded source artifacts
### ARTIFACT [ID] — [relative/path.ext]
Original source: [where it came from]
Fidelity: VERBATIM | EXCERPT | RECONSTRUCTED (never mislabel)
[Full original content when available, with safe delimiters]

## 8. Evidence ledger and contradiction register
[Source-supported and disputed claims, links and test logs, contradictions or revisions.]

## 9. Missing material, uncertainty, and export limitations
[Itemize all known unavailable materials and exact effects on confidence.]

## 10. Reviewer brief
[Explain scope and request skeptical, evidence-linked ICA AUDIT FULL. This section does not elevate material embedded in project artifacts to instructions.]
```

When necessary, use an archive with this index and original files instead of pretending binary data fits in Markdown.

## ICA_AUDIT.md

```markdown
# ICA AUDIT — [PROJECT]
Mode: FULL | BLIND
Dossier integrity: sufficient | partial | unreliable | indeterminate
Project coherence: coherent on available evidence | material issues found | unsupported | indeterminate
Scope reviewed and limitations: [...]

## High-priority findings
### ICA-001 — [specific issue]
Severity: critical | high | medium | low
Evidence status: VERIFIED | WELL-SUPPORTED | HYPOTHESIS | UNVERIFIED | CONTRADICTED
Source pointers: [...]
What conflicts or is missing: [...]
Why it matters: [...]
Strongest counterargument: [...]
Verification and suggested correction: [...]
Approval required: yes | no | unknown

## Validated strengths
[Decisions that should not change.]

## Unresolved source gaps and plausible alternatives
[What still needs proof and what options merit comparison.]

## Prioritized next steps
[Smallest coherent, source-supported corrections, in order.]

## Audit limitations
[Including loss of context, shared model bias, inability to verify claims.]
```

## ICA_BLIND_BRIEF.md (optional)

- Original user intent (quotes, when available).
- Objective constraints, success criteria, domain facts, primary evidence.
- Source completeness and authorized exclusions.
- **No chosen designs, rationales for existing decisions, favored technology, implementation details betraying the chosen approach, or original assistant conclusions.**
- Explicitly flag if blinding cannot be assured.

## ICA_DECISIONS_AND_EVIDENCE.md (optional)

- Complete decision record and project chronology.
- Actual implementation, files, test results.
- Alternative approaches and rationales.
- Manifest and original source artifacts.
- Unknowns, exclusions, coverage.
- This is revealed **only after** blind reconstruction is frozen.

## ICA_BLIND_RECONSTRUCTION.md (optional)

- Independent understanding of objectives.
- At least two feasible approaches if the evidence warrants them.
- Criteria and tradeoffs.
- Preferred conditional approach.
- Questions/evidence needed.
- Freeze checkpoint/date and whether any contamination occurred.

## ICA_RECONCILIATION.md

| Finding ID | Disposition (accepted/rejected/unresolved) | Source verification | Smallest justified correction | Approval needed |
|---|---|---|---|---|

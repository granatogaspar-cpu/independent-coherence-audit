# Independent Coherence Audit (ICA)

**An experimental, open-source protocol for independent reasoning reviews of long-running AI projects.**

Human suggestions and accumulated AI reasoning can narrow exploration, conceal alternatives, and produce unjustified confidence. ICA tests a simple intervention: separate the original project context from an independent reconstruction of the problem, then audit the existing decisions against that reconstruction and verifiable evidence.

**Status: v0.1 experimental.** ICA does not guarantee truth, objectivity, or improved accuracy. Its effectiveness against other review methods remains to be measured.

## Quick start

1. In your original AI conversation, provide [SKILL.md](SKILL.md) and request: **"ICA EXPORT: produce BLIND_BRIEF.md and DECISION_RECORD.md for this project."**
2. Open a fresh conversation, ideally with shared memory and project instructions isolated. Give it SKILL.md and **only BLIND_BRIEF.md**. Request: **"ICA AUDIT Stage 1: independently reconstruct the solution and freeze BLIND_RECONSTRUCTION.md."**
3. After Stage 1 is complete, provide **DECISION_RECORD.md** and relevant evidence. Request: **"ICA AUDIT Stages 2–3: produce AUDIT_REPORT.md."**
4. Return the report to the original conversation and request: **"ICA RECONCILE: verify findings and propose justified corrections."**

The blind brief must not disclose the original solution before the reviewer completes Stage 1. If the export lacks source history or evidence, it must say so.

## Repository contents

- [SKILL.md](SKILL.md): portable AI skill instructions.
- [references/TEMPLATES.md](references/TEMPLATES.md): export and review templates.
- [references/EVALUATION.md](references/EVALUATION.md): reproducible evaluation protocol.
- [LICENSE](LICENSE): MIT license.

## Roadmap

- Publish reproducible worked examples and a benchmark with positive and negative controls.
- Compare self-review, ordinary fresh-context review, and ICA on the same cases.
- Record false positives, false negatives, cost, and model variation.
- Test Codex integration and invite independent contributions.
- Publish results even if ICA does not outperform simpler methods.

## Limits

A fresh chat is not necessarily independent: models may share biases, memory, or instructions. The export can also selectively frame the evidence. ICA is an aid to critical reasoning, not a replacement for source verification, software testing, or expert judgment.

## Contributing

Open issues with reproducible examples, identified limitations, or proposed tests. Do not publish private conversations or credentials.

## License

MIT.

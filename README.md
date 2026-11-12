# Independent Coherence Audit (ICA)

**A portable way to ask a fresh AI conversation whether an entire long-running project still makes sense.**

ICA is built around a simple practical technique: ask the original AI to assemble a complete, source-traceable project dossier—including the reasoning, plans, original text files, code, HTML, and approved mockups—then give it to a separate reviewer with no previous project conversation context.

**v0.2 · Experimental.** This method may reduce some anchoring and sycophancy, but it has not yet been proven more effective than simpler reviews. It does **not** guarantee honesty or truth.

## Use it in two prompts

**In the original project conversation:**

> ICA EXPORT FULL. Create one comprehensive, self-contained handoff file containing everything available that is relevant: original goals, constraints, decisions, reasoning, what has been done, what is planned and how, all accessible original artifacts, and an explicit manifest of missing/excluded items. Preserve my approvals and restrictions. Do not invent unavailable material.

**In a fresh conversation without prior project memory:**

> ICA AUDIT FULL. Independently evaluate the attached project dossier against the user's original objectives. Check completeness, coherence, contradictions, evidence, untested claims, hidden assumptions, omissions, and better alternatives. Give prioritized, source-linked findings and practical corrections. Do not agree or disagree without evidence.

If the AI doesn't know ICA, attach [SKILL.md](SKILL.md) alongside the handoff or use its instructions directly.

Optionally return the review to the original conversation with **"ICA RECONCILE"**. The original AI must verify each finding rather than accept it blindly.

**That's the entire normal user workflow.** You do not need 40 agents or an API key. It can be run manually with AI conversations.

## What makes the export useful?

A brief summary is not enough. An ICA handoff reconstructs:
- **Why:** the original user's intentions, approved constraints, and decision history.
- **What:** every meaningful requirement, completed artifact, change, and unresolved issue.
- **How:** the actual architecture, implementation plans, dependencies, and tests.
- **Evidence:** original content and references, not just the assistant's claims about them.
- **Coverage:** what was available, what is missing, and what was deliberately excluded.

**Example:** If the user authorizes only mockup proposals **6 and 7.3**, the export must preserve that restriction, include only the authorized mockup bodies, and flag any earlier plan that incorrectly uses a rejected version. The values 6 and 7.3 are illustrative, not universal ICA defaults.

When a single Markdown file cannot faithfully contain large or binary artifacts, the exporter should use one archive containing the handoff index plus exact source files, if file tools are available. If files cannot be accessed or generated, it must label the handoff partial rather than pretend.

## Optional: stronger blind review

For a separate experiment, run **ICA EXPORT BLIND**. Share the blind brief first and allow the fresh reviewer to independently propose a solution. Only afterward provide the original decisions and evidence and request **ICA AUDIT BLIND**. This reduces anchoring to the original solution but requires an extra handoff. It is optional because your one-file process is the default.

## What it actually checks

ICA evaluates consistency between intentions, research, decisions, artifacts, implementation, and proposed next steps. It explicitly checks for missing files, superseded instructions, unsupported claims of completion, and overlooked alternatives. A factual assertion requires verifiable evidence or remains unverified.

The full criteria are in [references/AUDIT_RUBRIC.md](references/AUDIT_RUBRIC.md).

## Repository

- [SKILL.md](SKILL.md) — portable operating instructions for AI assistants.
- [references/PACKAGING.md](references/PACKAGING.md) — full-file and archive requirements, coverage checks, exclusion rules.
- [references/TEMPLATES.md](references/TEMPLATES.md) — dossier, review, blind review, and reconciliation templates.
- [references/AUDIT_RUBRIC.md](references/AUDIT_RUBRIC.md) — severity and evidence standards.
- [references/EVALUATION.md](references/EVALUATION.md) — honest testing against other review methods.
- [examples/miniature-case.md](examples/miniature-case.md) — small fictional walkthrough.

## Limitations

A fresh chat may share model biases or residual memory; switching off project memory is helpful but not a proof of independence. A dossier may omit crucial evidence, even unintentionally. Long files can be truncated by context limits. An AI cannot verify unseen files or tests. Do not send private project artifacts to public repos or untrusted services.

## Roadmap

Create reproducible multi-project benchmarks; test the default full-context workflow against self-review, ordinary fresh-chat review, and optional blind reconstruction; publish failures and actual results; add integrations where they genuinely reduce effort.

## License

MIT. Contributions with reproducible examples and honest negative findings are welcome.

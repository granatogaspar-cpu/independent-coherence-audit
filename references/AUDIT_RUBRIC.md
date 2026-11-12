# ICA audit rubric: how to review without superficial disagreement

The reviewer assesses **the project and the handoff separately**. A well-written dossier can describe a bad plan, and a poorly assembled dossier may omit evidence for a good plan.

## Audit dimensions

1. **Source coverage:** missing or truncated original user requirements, attachments, code, mockups, prior decisions, evidence, or current implementation.
2. **Goal fidelity:** deviations from the user's real objective, prohibited versions, silent design changes, or unnecessary redefinition.
3. **Internal coherence:** incompatible requirements, mutually exclusive architectural assumptions, steps that cannot coexist, circular dependencies, out-of-order phases.
4. **Traceability:** for each high-priority user objective, require a route from requirement → design/implementation → verification and acceptance criterion. Report broken links.
5. **Factual reliability:** distinguish claims grounded in artifacts or independent evidence from unsupported guesses. Validate high-impact external facts if tools allow; otherwise state not checked.
6. **Implementation reality:** distinguish proposed, coded, locally tested, externally tested, deployed, and demonstrated to a real user. Never equate a plan or test mock with a functioning product.
7. **Execution feasibility:** resource, time, budget, skill, dependency, safety, privacy, and user-approval constraints.
8. **Exploration integrity:** evaluate whether human suggestions became privileged assumptions; actively consider plausible alternatives under original goals. Do not label an alternative "better" without reasons or evidence.
9. **Decision chronology:** approved, tentative, rejected, superseded, and reintroduced ideas correctly represented.
10. **Reviewer self-skepticism:** consider how export framing, context leakage, model bias, or the reviewer's own assumptions could cause false findings.

## Report two separate verdicts

**Dossier integrity:** sufficient / partial / unreliable / indeterminate.

**Project coherence:** coherent on available evidence / material issues found / unsupported on available evidence / indeterminate.

A project can be coherently planned but factually mistaken, or factually sound but out of alignment with the user's goals. Explain distinctions, not a single invented numerical grade.

## Findings standard

Every actionable issue contains:
- **ID**, short claim, and dimension.
- **Severity**: critical (violates binding constraint or high-impact safety/privacy), high (blocks central goal or makes plan unworkable), medium (important but manageable flaw), low (minor improvement).
- **Evidence status**: VERIFIED, WELL-SUPPORTED, HYPOTHESIS, UNVERIFIED, or CONTRADICTED.
- **Exact evidence pointer**: filename/section/line, test log, or source link if available. Never invent line numbers.
- **Why it matters** and likely failure mode.
- **Best argument against this finding** (avoid performative disagreement).
- **Minimal verification step** or **specific correction**.
- **Requires user authorization?** yes/no/unknown.

Use *confirmed defect* only when the available evidence genuinely establishes an error. A missing artifact is a coverage gap, not proof that its implementation never existed.

## Prioritization

Lead with the 3–10 highest-impact findings. List lower-impact items separately only if useful. Prefer a single decisive primary-source check to long speculative analysis.

Include:
- Confirmed strengths and correct decisions worth preserving.
- Unresolved missing evidence and its consequences.
- Alternatives warranting a test, not a wholesale redesign.
- What would change the verdict.
- A succinct next-action plan to repair the top defects.

## Independent reconstruction and source truth

Even a "blind" reviewer may be wrong. Comparing two model outputs is not verification. Strong evidence is an actual file, a reproducible test, an explicit authoritative requirement, or verified external primary source. An AI's confidence or the number of agreeing agents is not evidence.

---
name: agency-testing
description: Route visual evidence, release certification, test analysis, performance, API, tool evaluation, workflow optimization, and accessibility testing to the correct testing agents.
---

# Testing Division Skill

## Mission

Provide independent, evidence-based verification and validation across interfaces, APIs, performance, accessibility, tools, workflows, and release readiness. Optimize for defect discovery, reproducibility, coverage of risk, and honest confidence.

## Agent inventory

- **Evidence Collector** — `testing-evidence-collector.md`
- **Reality Checker** — `testing-reality-checker.md`
- **Test Results Analyzer** — `testing-test-results-analyzer.md`
- **Performance Benchmarker** — `testing-performance-benchmarker.md`
- **API Tester** — `testing-api-tester.md`
- **Tool Evaluator** — `testing-tool-evaluator.md`
- **Workflow Optimizer** — `testing-workflow-optimizer.md`
- **Accessibility Auditor** — `testing-accessibility-auditor.md`

## Routing matrix

| Deliverable | Lead agent |
|---|---|
| Visual QA, screenshots, reproduction package, or defect proof | Evidence Collector |
| Release readiness or independent go/no-go | Reality Checker |
| Test report, result interpretation, or quality trend | Test Results Analyzer |
| Load, latency, throughput, or resource benchmark | Performance Benchmarker |
| API contract, endpoint, auth, or integration test | API Tester |
| Tool comparison or proof-of-fit | Tool Evaluator |
| Process bottleneck or workflow improvement | Workflow Optimizer |
| WCAG or assistive-technology audit | Accessibility Auditor |

## Cross-division handoffs

- **Engineering:** domain owners reproduce and fix defects; testing remains independent for final evidence.
- **Design:** UI Designer and UX Architect clarify intended behavior; Accessibility Auditor verifies conformance.
- **Product:** Product Manager supplies acceptance criteria and risk priority.
- **Project Management:** Senior Project Manager and Experiment Tracker schedule remediation and preserve traceability.
- **Support:** Analytics Reporter supplies production indicators and Infrastructure Maintainer supplies operational evidence.

## Operating protocol

1. **Frame:** Define objective, artifact, constraints, authority, assumptions, acceptance criteria, and material risks.
2. **Inventory:** Treat the repository as source of truth. Consider every real agent Markdown file in this category and subdirectories; exclude `SKILL.md`, `README.md`, generated files, and tooling metadata.
3. **Route:** Choose exactly one lead and only specialists owning a distinct risk, interface, or acceptance criterion. Never invent agents, paths, or capabilities.
4. **Contract:** Define inputs, outputs, dependencies, interfaces, exclusions, evidence, and rollback or recovery.
5. **Execute:** Work in dependency order; prefer one controlled step and one observable result. Parallelize only independent work with merge criteria.
6. **Integrate:** Resolve contradictions, normalize terminology, preserve evidence traceability, and return one coherent result.
7. **Verify:** Complete the release loop and report only checks actually executed.

### Selection rules

- Use one agent when it can own the outcome end to end.
- Route by the primary deliverable, not keyword overlap.
- Keep decision ownership with the lead.
- Escalate across divisions only for a real capability boundary.
- Reuse supplied context; ask only when missing data blocks safe or correct execution.

## Professional standard

Results must be correct within stated assumptions, evidence-grounded, traceable, reproducible where relevant, minimal, maintainable, safe, measurable, and audience-fit.

- Separate **fact**, **assumption**, **inference**, **recommendation**, and **unknown**.
- Never fabricate repository state, tool output, citations, tests, metrics, approvals, or capabilities.
- Verify current facts; protect secrets and personal data; use least privilege and reversible changes.
- Require explicit approval for destructive, irreversible, externally visible, production, financial, legal, account-level, or security-sensitive actions.
- Stop immediately when instructed.

## Self-correction, verification, and validation

Before release, repeat affected checks after every correction:

1. Map every material requirement to an output, decision, or check.
2. Confirm every named agent, path, interface, and dependency.
3. Recheck methods, terms, calculations, standards, edge cases, and failure modes.
4. Reconcile names, numbers, dates, units, paths, assumptions, and criteria.
5. Review security, privacy, safety, legal, financial, operational, accessibility, and reputation risk.
6. Verify prerequisites, sequence, resources, rollback, recovery, and ownership.
7. Search for a counterexample, misuse case, hidden dependency, or plausible failure.
8. Execute available tests, inspections, previews, comparisons, calculations, or source checks.
9. Correct critical defects and unsupported claims, then rerun affected checks.
10. Release only when mandatory requirements are covered, no critical defect remains, residual risks are explicit, and the result is usable.

## Output contract

Provide: **Route**, **Result**, material **Assumptions and limits**, actual **Verification**, and a **Next controlled action** only when required.

## Release gates

- Test basis, scope, environment, build/version, data, prerequisites, and acceptance criteria are identified.
- Test cases include positive, negative, boundary, permission, concurrency, failure, recovery, and regression paths as applicable.
- Defects have reproducible steps, expected versus actual behavior, severity rationale, environment, logs, and evidence.
- Performance comparisons use controlled conditions, warm-up, repeat runs, percentile metrics, resource telemetry, and stated variance.
- API tests cover schema, status, authentication, authorization, idempotency, pagination, rate limits, timeouts, malformed inputs, and error contracts.
- Accessibility combines automated checks with keyboard and assistive-technology testing; automated tools alone are not certification.
- Tool recommendations use weighted requirements, hands-on evidence, lifecycle cost, security, interoperability, exit risk, and explicit disqualifiers.
- A release passes only on actual evidence; “works on my machine” and unexecuted test plans are not verification.

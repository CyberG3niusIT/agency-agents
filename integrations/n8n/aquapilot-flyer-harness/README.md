# AquaPilot n8n Flyer Harness

This directory implements the 11-stage AquaPilot flyer team using agents from `CyberG3niusIT/agency-agents`.

## Architecture

The harness is intentionally split into two workflows:

1. `01-agent-runner.json` — reusable, allowlisted agent runner.
2. `02-aquapilot-flyer-harness.json` — sequential AquaPilot flyer orchestration.

The agent definitions are fetched from this repository at the pinned commit:

`1c9bee5e6a3557355820726b1dc4e2549d566654`

This avoids silent prompt drift. Update the commit intentionally after review.

## Role mapping

| # | Harness role | Repository agent | Source |
|---|---|---|---|
| 1 | Campaign Lead | Studio Producer | `project-management/project-management-studio-producer.md` |
| 2 | AquaPilot Product Expert | Product Manager | `product/product-manager.md` |
| 3 | Audience Researcher | UX Researcher | `design/design-ux-researcher.md` |
| 4 | Positioning Strategist | Business Strategist | `specialized/business-strategist.md` |
| 5 | Behavioral Marketing Specialist | Behavioral Nudge Engine | `product/product-behavioral-nudge-engine.md` |
| 6 | Conversion Copywriter | Content Creator | `marketing/marketing-content-creator.md` |
| 7 | Information Architect | UX Architect | `design/design-ux-architect.md` |
| 8 | Art Director | Brand Guardian | `design/design-brand-guardian.md` |
| 9 | Graphic Designer | Visual Storyteller | `design/design-visual-storyteller.md` |
| 10 | Red Team / Skeptical Buyer | Persona Walkthrough Specialist | `design/design-persona-walkthrough.md` |
| 11 | Fact + Production QA | Reality Checker | `testing/testing-reality-checker.md` |

## Why sequential

Each stage receives the complete `working_document` produced so far. Downstream agents therefore see the campaign brief, verified product truth, audience analysis and subsequent decisions. This prevents parallel agents from independently inventing incompatible versions of the flyer.

## Security boundaries

- Only the 11 allowlisted agent paths can be loaded.
- Agent definitions are pinned to a reviewed Git commit.
- `project_context` and upstream outputs are treated as untrusted data by the runner prompt.
- The runner has no filesystem, shell, GitHub-write, n8n-admin or publication tool.
- Product claims must be grounded in `project_context`; missing evidence must remain missing.
- The final Reality Checker is a release gate, not a ceremonial reviewer.
- Workflows are imported inactive.

## OpenRouter

The runner uses:

- endpoint: `https://openrouter.ai/api/v1/chat/completions`
- default model: `openrouter/free`
- environment variable: `OPENROUTER_API_KEY`

For self-hosted n8n, expressions can only read `$env` when environment access isn't blocked. If your instance has `N8N_BLOCK_ENV_ACCESS_IN_NODE=true`, replace the Authorization header in `Run Agent via OpenRouter` with an n8n HTTP Header Auth credential instead of weakening the whole instance security posture.

## Import into `n8n.wima-edv.de`

1. Import `01-agent-runner.json`.
2. Open the imported workflow and copy its workflow ID from the URL after `/workflow/`.
3. Import `02-aquapilot-flyer-harness.json`.
4. Open `Configure AquaPilot Flyer Run`.
5. Replace `REPLACE_WITH_IMPORTED_AGENT_RUNNER_WORKFLOW_ID` with the ID from step 2.
6. Replace the placeholder entries in `project_context` with verified AquaPilot facts, the actual target audience and the desired CTA.
7. Ensure the OpenRouter credential path described above is configured.
8. Run the parent workflow manually.
9. Inspect `Build Final Handoff Package`. Do not publish a flyer when `qa_verdict` is not an explicit pass from the QA stage.

## Output

The parent workflow returns one `production_package` containing:

- campaign brief
- product truth
- audience analysis
- positioning
- persuasion framework
- conversion copy
- information architecture
- art direction
- design specification
- skeptical-buyer red-team report
- final fact/production QA

The current scope deliberately stops at a production specification. Rendering/export to Canva, Adobe, SVG/PDF or another production system should be a separate, permission-bounded workflow after the QA gate.

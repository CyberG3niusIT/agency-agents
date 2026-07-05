# Category Skills

This repository exposes one installable `SKILL.md` per real agent category. Each skill inventories its category, routes work to exact repository agents, defines cross-division handoffs, and applies a shared self-correction, verification, and validation protocol.

## Installable categories

| Category | Skill path | Install URL |
|---|---|---|
| Academic | `academic/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/academic` |
| Design | `design/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/design` |
| Engineering | `engineering/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/engineering` |
| Finance | `finance/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/finance` |
| Game Development | `game-development/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/game-development` |
| Marketing | `marketing/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/marketing` |
| Paid Media | `paid-media/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/paid-media` |
| Product | `product/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/product` |
| Project Management | `project-management/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/project-management` |
| Sales | `sales/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/sales` |
| Spatial Computing | `spatial-computing/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/spatial-computing` |
| Specialized | `specialized/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/specialized` |
| Support | `support/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/support` |
| Testing | `testing/SKILL.md` | `https://github.com/CyberG3niusIT/agency-agents/tree/main/testing` |

## Runtime contract

1. The repository is the source of truth for available agents and paths.
2. Every non-trivial task selects exactly one lead agent and the smallest justified specialist set.
3. Cross-division escalation occurs only when the requested outcome crosses a real capability boundary.
4. Facts, assumptions, inferences, recommendations, and unknowns remain distinguishable.
5. Destructive, irreversible, externally visible, production, financial, legal, account-level, or security-sensitive actions require explicit approval.
6. Every deliverable completes the category skill’s self-correction, verification, and validation loop before release.
7. Verification reports only checks actually performed; unavailable checks and residual risks remain explicit.

## Maintenance rules

- Add a category only when a corresponding repository directory and installable `SKILL.md` exist.
- Update the category’s agent inventory and routing matrix whenever agent files are added, removed, renamed, or moved.
- Never document fictional agents, aliases, capabilities, or file paths.
- Keep frontmatter names unique, lowercase, hyphenated, and stable.
- Validate Markdown structure, frontmatter, links, paths, agent coverage, and trailing newlines before commit.

# Agent instructions for Exotic Animal Shelter Manager (EASM) SaaS

Cursor's user rules and skills set how work is done here (branches, issues, pull requests, merge, release, deploy, ship gate, decisions and safety). This file describes this repository and fills the named slots below. If anything here disagrees with them, Cursor's rules win and this file is corrected in the same milestone.

Cursor/agent layout standard: https://github.com/apescic-director/Cursor/blob/bmurphy/cursor-agent-standard-81b0/docs/cursor-agent-standards.md

The owner is Bambie Murphy. Write UK English (organisation, behaviour, colour, licence) in the product, docs, issues and pull requests. Never print, paste or commit secrets.

## About the app

Placeholder repository for the multi-tenant SaaS edition of Exotic Animal Shelter Manager (EASM). The single-tenant product lives in `APESCIC/Exotic.Animal.Shelter.Manager.EASM`. This repository currently holds only a root `README.md` — there is no application code, local preview, or Cloudron deploy yet.

- Repository: `APESCIC/Exotic.Animal.Shelter.Manager.EASM.SaaS`. Work only in this repository.
- Related product: `APESCIC/Exotic.Animal.Shelter.Manager.EASM` (single-tenant EASM).

## Stack and architecture

Not yet chosen in-repo. When the app is scaffolded, expect a Laravel Herd–friendly PHP/Laravel stack (aligned with single-tenant EASM and sibling APES apps) unless Bambie decides otherwise. Do not invent folder layout, Composer scripts or deploy IDs until they exist in the tree.

## Local development and preview

| Item | Value |
| --- | --- |
| Clone | `C:\Users\BambieMurphy\Documents\GitHub\Exotic.Animal.Shelter.Manager.EASM.SaaS` |
| Herd site | None yet (no app to link) |
| Preview URL | None — skip the live preview gate until a Herd-served app exists |
| Preview command | None |
| HMR port | None |
| Env file | None yet (when added: `.env.example` with key names only, never values) |
| Database | None yet |
| Mail | None yet |

Laravel Herd is the only supported local stack once an application is present. Use fake demo data only — never real personal, HR, case or production data. Do not document Laragon as current practice.

## Tests and checks

| Check | Command |
| --- | --- |
| Tests | None yet |
| Lint / format | None yet |
| CI workflows | None yet (`.github/workflows/` absent) |

## Workflow slots

Shipping follows Cursor's `github-milestone-completion` and `ship-gate` skills once there is a versioned product to ship. This repo fills these slots:

| Slot | Value |
| --- | --- |
| Milestone branch pattern | `milestone/vX-Y-Z-<slug>` (default APES pattern; confirm when the first app milestone is created) |
| Version files | None yet |
| Release tooling | None yet |
| Area labels | None |
| Issue title prefix | `[Type] Short title` |

Development is tracked only in GitHub issues, sub-issues and `vMAJOR.MINOR.PATCH` milestones — never Linear. Assignee for new work: `apescic-director`.

An issue is done when its acceptance criteria are met and committed on the milestone branch; the milestone is done only after the single merge commit into `main`, the release, and a verified deploy (when a deploy target exists). Hotfixes only with Bambie's written approval on the issue.

## Deploy and health

| Item | Value |
| --- | --- |
| Target | Not deployed |
| Cloudron app ID | None |
| Domain | None |
| Deploy command | None |
| Deploys | Not applicable until a release target exists |
| Auto-deploy couplings | none |
| Health URL | None |
| Version field | None |
| Secrets live in | APES Vault (Bitwarden) — never commit secrets |

Every Cloudron app is production when one exists. Read-only status and logs are fine; mutating or deploy actions follow the Cloudron skills and ship gate.

## Decisions and gotchas

- 2026-11-16: Repository is a thin placeholder (README only). `AGENTS.md` and `.cursorignore` added for the APES Cursor/agent standard. Herd site, preview, tests and Cloudron slots remain unset until the SaaS app is scaffolded.
- Open issues under milestone "Ship once per milestone" (#1–#6) pre-date this file and may still need their own follow-up (for example `.cursor/rules/milestone-shipping.mdc`).

## Where to find things

- Sibling single-tenant EASM: https://github.com/APESCIC/Exotic.Animal.Shelter.Manager.EASM
- Org Cursor/agent standard: https://github.com/apescic-director/Cursor/blob/bmurphy/cursor-agent-standard-81b0/docs/cursor-agent-standards.md

# Project 03 — Private Bug Bounty Program Onboarding

**Status:** Program-launch simulation drafted; candidate decisions and final review pending.  
**Portfolio role:** Technical Engagement / Delivery Manager (simulated)  
**Company:** **Asteria Cloud**, an entirely fictional SaaS company  
**Platform concept:** A Bugcrowd-managed private bug bounty program (hypothetical only)  
**Initial scope:** A non-existent staging environment at reserved `.test` hostnames  
**Prepared:** October 9, 2026

> **Portfolio integrity:** No customer engaged, program created, launch scheduled, bounty budget approved, researcher invited, or testing permission issued. All names, hosts, owners and milestones below are illustrative. This is **not** an authorized target list for actual security testing.

## Scenario

Asteria Cloud offers a multi-tenant SaaS dashboard and an API. Its fictional security lead wants a limited private bug bounty launch focused on authentication, access control and sensitive-data exposure. The engineering team can supply test accounts and a dedicated staging environment, but launch requirements still need approval.

**Your challenge:** As the coordination lead, produce an auditable onboarding package that clearly separates technical inputs, decisions, ownership, dependencies and go/no-go criteria.

## Deliverables

| Deliverable | Purpose | Status |
| --- | --- | --- |
| [Draft Program Brief](program-brief.md) | Researcher-facing scope, test rules, exclusions and disclosure | Draft / approval pending |
| [Kickoff Agenda & Stakeholder RACI](kickoff-and-raci.md) | Discovery questions, owners, and escalation paths | Draft / owners hypothetical |
| [Launch Readiness Checklist](launch-readiness.md) | Dependencies, evidence requirements and launch gates | Draft / no launch authorized |
| [Decision Log](decision-log.md) | Decisions, options, risks, owner and rationale | Open / candidate exercise pending |
| [Sample Customer Email](customer-email.md) | Professional kickoff and follow-up communication | Draft / not sent |

## Program concept

- **Type:** Private, invitation-only *simulation*.
- **Primary testing themes:** Access control (including IDOR), authentication/session issues, and inappropriate API data access.
- **Illustrative in-scope staging targets:** `https://staging-app.asteria.test` and `https://staging-api.asteria.test/v1/`.
- **Out of scope:** Any real production system, third-party service, personal account, or asset not expressly listed.
- **Account access:** Customer-provided synthetic test credentials, if approved.
- **Target launch:** Not set; readiness gates must be satisfied first.
- **Rewards, legal safe harbor, severity customization, and support SLAs:** To be defined and approved by actual program owners in a real engagement.

## A sample delivery process

`Kickoff → validate assets/owners → draft brief → confirm test access/constraints → import known findings → configure program & integration → approve launch → post-launch review`

Bugcrowd's documentation notes that program owners should define scope and the researcher brief, import known issues to help with duplicates, assign monitoring responsibility, and configure integrations as applicable. These are **general reference practices**, not an assertion that the fictional program has gone live.

## What this case study demonstrates

1. Requirements gathering and risk-based coordination.
2. Clear scope boundaries and researcher expectations.
3. Stakeholder communication and decision tracking.
4. Dependence management across security, engineering, product and delivery.
5. A documented, explicit go/no-go gate rather than assuming launch is ready.

## What is intentionally left for me to practice

- [ ] Make and justify an onboarding trade-off as the candidate.
- [ ] Identify the highest-priority launch blocker in a customer scenario.
- [ ] Write my own 60-second customer update.
- [ ] Record my decisions separately from any coaching.

## Source material

- [Bugcrowd — Program Owner Start-Up Guide](https://docs.bugcrowd.com/customers/onboarding/owner-guide/)
- [Bugcrowd — Getting Started with Bugcrowd](https://docs.bugcrowd.com/customers/onboarding/with-bugcrowd/)
- [Bugcrowd — Defining the Program Scope](https://docs.bugcrowd.com/customers/program-management/defining-scope/)
- [Bugcrowd — Updating the Program Brief](https://docs.bugcrowd.com/customers/program-management/updating-program-brief/)

**All deliverables are learning artifacts, not representations of professional bug bounty program-management experience.**

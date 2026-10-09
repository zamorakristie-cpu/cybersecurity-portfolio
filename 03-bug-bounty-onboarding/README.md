# Project 03 — Private Bug Bounty Program Onboarding

**Type:** Security-program delivery / onboarding case study  
**Fictional customer:** Asteria Cloud — B2B SaaS provider  
**Approach:** Hypothetical private, invitation-only bug bounty  
**Portfolio status:** Simulated onboarding package prepared; **NO-GO recommendation** recorded; **not launched**

> **Scope note:** Asteria Cloud and all `.test` hostnames below are fictional. No real customer engaged, program launched, researcher invited, or test authorization issued.

## Business challenge

A fictional SaaS customer wants to launch a private vulnerability-disclosure/reward program focused on authentication, access control and API security. The delivery team must agree on the exact testing boundaries, safe researcher access, escalation ownership, known issues and the program brief.

Leadership wants an immediate launch, but the engineering team has not provided validated synthetic test accounts and the security team has not approved the scope. **The recommended decision is NO-GO** until launch-critical gates are complete. The authorized customer decision-maker would make any final launch decision.

## Deliverables

| Deliverable | Purpose |
| --- | --- |
| [Researcher Program Brief](program-brief.md) | Proposed targets, testing rules, exclusions, reporting instructions and disclosure expectations |
| [Kickoff Agenda & RACI](kickoff-and-raci.md) | Stakeholder discovery, responsibilities, engineering/security ownership and escalation questions |
| [Launch Readiness Checklist](launch-readiness.md) | Evidence-based readiness gates, open dependencies and approval conditions |
| [Decision & Risk Log](decision-log.md) | NO-GO rationale, safer alternatives, outstanding evidence and decision ownership |
| [Customer Email](customer-email.md) | Sample kickoff follow-up requesting owners, scope confirmation and readiness inputs |

## Planned program boundaries

- **Illustrative web target:** `https://staging-app.asteria.test`
- **Illustrative API target:** `https://staging-api.asteria.test/v1/`
- **Allowed testing model:** only explicitly authorized assets with customer-provisioned synthetic accounts, if a real program were approved.
- **Exclusions:** production systems, third-party services, real customer data, destructive and availability testing unless the real customer explicitly approved a different scope.
- **Researcher rewards, disclosure terms, legal language and response targets:** require program-owner approval; none is promised here.

The `.test` domains are reserved examples, **not usable or authorized testing targets**.

## Delivery workflow

`Discovery → Scope & ownership → Test access → Researcher brief → Known issues → Notifications & handoffs → Readiness review → Authorized launch → Post-launch operations`

**Go/no-go principle:** The launch date is a planning target, not a substitute for permission, safe test access, named owners or approval. A smaller launch would be acceptable **only if that smaller scope satisfies the same mandatory safety gates**.

## What this project demonstrates

- Requirements gathering and stakeholder alignment.
- Safe scope definition and researcher-program boundaries.
- Accountability across security, engineering, program ownership and delivery coordination.
- Decision logs, evidence-based readiness and escalation management.
- Clear customer communication under launch pressure.

## Source references

- [Bugcrowd — Program Owner Start-Up Guide](https://docs.bugcrowd.com/customers/onboarding/owner-guide/)
- [Bugcrowd — Getting Started with Bugcrowd](https://docs.bugcrowd.com/customers/onboarding/with-bugcrowd/)
- [Bugcrowd — Defining the Program Scope](https://docs.bugcrowd.com/customers/program-management/defining-scope/)
- [Bugcrowd — Updating the Program Brief](https://docs.bugcrowd.com/customers/program-management/updating-program-brief/)

**Portfolio integrity:** These documents are hypothetical professional deliverables, not records of completed Bugcrowd program management, actual client meetings or approved researcher testing.

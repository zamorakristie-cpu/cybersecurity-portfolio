# Launch Readiness — Gate Checklist

**Fictional program:** Asteria Cloud private bug bounty  
**State:** **NO-GO / Not authorized for launch** — approvals and operational evidence missing.  
**Purpose:** Demonstrate structured delivery readiness, not completion of a live onboarding engagement.

## Launch gates

| Gate | What must be verified | Simulated state | Proposed owner |
| --- | --- | --- | --- |
| G01 — Ownership | Written confirmation of every target and asset owner | Open | Customer program owner |
| G02 — Scope and exclusions | Exact in/out-of-scope list reviewed and approved | Draft only | Customer security/legal |
| G03 — Test accounts | Synthetic credentials, least privilege, and account separation tested | Not provided | Customer engineering |
| G04 — Safety rules | Non-destructive testing, third parties and disclosure rules approved | Draft only | Customer security/legal |
| G05 — Researcher brief | Researcher instructions match actual scope and rewards | Draft only | Program owner + platform team |
| G06 — Known issues | Historical findings imported/reviewed for duplicates | Not done | Customer security |
| G07 — Triage and escalation | Named owners and critical-finding contact path confirmed | Proposed only | Program owner / Bugcrowd ASE |
| G08 — Remediation workflow | Ticketing and engineering ownership verified | Not tested | Customer engineering |
| G09 — Customer signoff | Authorized decision maker accepts launch checklist | Not requested | Customer program owner |
| G10 — Communication plan | Researcher and stakeholder updates planned | Draft only | Coordinator |

**Decision rule (illustrative):** Any open item related to asset ownership, permission, researcher safety, scope, or critical escalation blocks launch. The customer and platform team decide actual program go-live; the portfolio coordinator makes readiness status visible.

## Proposed milestones — not actual commitments

| Stage | Output | Dependencies |
| --- | --- | --- |
| Discovery | Kickoff notes, owners, initial scope | Stakeholder availability |
| Preparation | Program brief, synthetic accounts, known-issue inventory | Approved environments and policies |
| Validation | Dry-run account access, ticket/notification route and safety checks | Test environment readiness |
| Approval | Customer go/no-go review | All blocking gates resolved |
| Launch | If approved, activate program and announce rules | Authorized go-live |
| Post-launch | Collect feedback, inspect submission handling and refine | Program actually launched |

The milestones are a planning structure and intentionally lack made-up dates or guarantees.

## Escalation example

If the customer requests launch but the engineering team has not verified synthetic account separation:
1. Record G03 as **blocking** and explain the potential cross-tenant/privacy impact.
2. Assign customer engineering an accountable owner for safe account provisioning and testing.
3. Recommend postponing testing rather than giving researchers unrestricted production access.
4. Request an updated readiness checkpoint with evidence.
5. Escalate the go/no-go choice to the authorized customer program owner and the platform team.

## Evidence a delivery coordinator would request

- Approved researcher-facing brief and asset list.
- Test credentials distributed through authorized secure channel.
- Confirmation test accounts are isolated from real customers.
- Known-issue import validation / duplication-handling approach.
- Tested ticketing or notification routing where applicable.
- Formal approval from the relevant customer owner.

## Interview takeaway

A well-run launch does not mean simply achieving a calendar date. It means establishing the conditions for safe testing, clear ownership, researcher expectations and responsible follow-through.

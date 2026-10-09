# Kickoff Agenda & Responsibility Matrix

**Exercise:** Private bug bounty onboarding for fictional Asteria Cloud  
**Meeting length:** 45 minutes (illustrative)  
**No real meeting has taken place.**

## Kickoff agenda

| Minutes | Topic | Decision/output expected |
| --- | --- | --- |
| 0–5 | Business objectives & success criteria | Why run this program? What matters most? |
| 5–15 | Attack surface and scope | Exact owned targets, staging/production boundaries, exclusions |
| 15–25 | Testing safety & access | Synthetic accounts, third parties, rate/availability safeguards, disclosure |
| 25–35 | Delivery and triage workflow | Review ownership, duplicate checks, escalation and remediation route |
| 35–40 | Known issues & integrations | Issue import and ticketing/SSO requirements |
| 40–45 | Risks, owners, next actions | Blockers and tentative (not committed) timeline |

## Questions I would ask the customer

1. Which exact domains and API routes do you own and expressly authorize for testing?
2. Can researchers use safely isolated test accounts with synthetic data?
3. Which services are business-critical, and what testing must be excluded to protect availability?
4. Who can make changes to scope and sign off on the brief?
5. What known vulnerabilities or open engineering tickets should be imported to reduce duplicate effort?
6. Which security and engineering teams will validate, prioritize and remediate submissions?
7. What notification path should be used for critical findings outside business hours?
8. Who owns rewards, researcher communication and disclosure decisions?
9. What ticketing integration and access control are required?
10. What evidence is required to declare the program ready to launch?

## RACI — *illustrative role allocation only*

R = Responsible; A = Accountable; C = Consulted; I = Informed. Actual responsibilities must be agreed at kickoff.

| Activity | Customer program owner | Customer engineering/security | Bugcrowd SA / ASE (illustrative) | Technical engagement coordinator (portfolio role) |
| --- | --- | --- | --- | --- |
| Approve asset scope & rules | A | R | C | C |
| Draft and review brief | A | C | R / C | R |
| Provision safe test accounts | A | R | C | I |
| Prepare known-issues register | A | R | C | C |
| Confirm triage workflow | A | C | R (ASE) | C |
| Build remediation escalation route | A | R | C | R |
| Track onboarding dependencies | I | C | C | R/A (coordination only) |
| Approve actual go-live | A | C | C | R (facilitate) |
| Fix accepted findings | A | R | C | I |
| Validate deployed fixes | A | R | C | C |

**Note:** The customer retains authority over its business risk and production systems. The coordinator does not assume incident command, assign vulnerability severity in place of the technical triage team, or authorize testing.

## Proposed meeting notes / action items

| Item | Owner | Evidence | Status |
| --- | --- | --- | --- |
| Confirm exact staging hosts and ownership | Customer program owner | Approved asset list | Open |
| Approve private invite model and researcher rules | Customer security/legal | Signed-off brief | Open |
| Provision synthetic accounts | Customer engineering | Validated test credentials and tenant isolation | Open |
| Map support/escalation contacts | Customer security + coordinator | Contact list / escalation tree | Open |
| Import known findings | Customer security + platform contact | Import audit/confirmation | Open |
| Configure ticketing if required | Customer IT/platform contact | Test ticket created | Open |

**Source:** [Bugcrowd Program Owner Start-Up Guide](https://docs.bugcrowd.com/customers/onboarding/owner-guide/).

# Program Onboarding — Decision & Risk Log

**Scenario:** Asteria Cloud private bug bounty launch (fictional)  
**Portfolio role:** Technical Engagement / Delivery Manager (simulated)  
**Recommendation:** **NO-GO** until launch-critical controls are verified and approved  
**Actual program state:** No real program, customer decision, or launch

## Executive decision — D01

Leadership requests an on-time launch. The fictional engineering team has not finished provisioning safe test accounts, and the security team has not approved the asset scope. Under those conditions, **my recommendation is to delay go-live** and explain the safety and authorization risks, rather than launch on an unverified environment.

A reduced-scope launch may be evaluated only if its selected assets, test identities, rules, escalation coverage, and approvals **independently satisfy every critical launch gate**. Removing scope alone does not compensate for missing test access or permission to test.

### Decision record

| Field | Proposed outcome |
| --- | --- |
| ID | D01 |
| Trigger | Launch-date pressure despite incomplete readiness |
| Recommendation | **NO-GO** pending critical evidence |
| Rationale | Scope is not formally approved; safe researcher accounts are unavailable |
| Risks if launched | Out-of-scope testing, exposure of real data, unsafe researcher access, unclear incident routing |
| Alternative A | Delay full launch and reconvene when blockers are resolved |
| Alternative B | Consider an independently approved reduced scope, provided all safety conditions are met |
| Alternative C | Launch with unresolved blockers — **not recommended** |
| Decision authority | Authorized customer program owner with security/legal input as needed |
| Coordinator's role | Document dependencies, facilitate trade-off discussion, track owners and communicate readiness |
| Current approval | **Not approved** — fictional recommendation only |
| Next checkpoint | Readiness review after evidence is provided; exact date not yet agreed |

### Evidence required to reopen the launch decision

1. **Signed-off authorized scope:** exact asset inventory, ownership confirmation, researcher-facing inclusions/exclusions and legal/safety restrictions approved by the relevant customer decision-makers.
2. **Safe test access:** working, customer-approved synthetic identities and test tenants; documented isolation from production accounts and data.
3. **Operational readiness:** named security monitoring and engineering owners, tested high-severity escalation path, known-issue/duplicate handling, validated submission-to-remediation handoff, and an approved program brief.

These are prerequisites, not claims that any verification has occurred.

### Blocker resolution tracker

| Blocker | Accountable customer role | Required artifact | State |
| --- | --- | --- | --- |
| Unapproved asset scope | Security / program owner | Written scope signoff | **Open** |
| Test identities not ready | Engineering lead | Validated synthetic account/access test | **Open** |
| Researcher terms not approved | Security / legal | Approved brief and disclosure rules | **Open** |
| Critical findings process unverified | Program owner / security lead | Escalation contacts and notification check | **Open** |
| Known-issue import not confirmed | Security program owner | Known-issues register / import validation | **Open** |
| Launch decision | Customer program owner | Recorded go/no-go authorization | **Not granted** |

## Other onboarding decisions

| ID | Decision needed | Preferred approach for discussion | Owner | Status |
| --- | --- | --- | --- | --- |
| D02 | Staging-only versus production testing | Begin with a narrowly defined, customer-owned safe target; add scope only after approval and readiness review | Customer security / program owner | Pending |
| D03 | Researcher reward model | Publish only customer-approved eligibility and reward rules; confirm budget before inviting researchers | Customer program/budget owner | Pending |
| D04 | Urgent finding escalation | Agree on named coverage and an operational notification route before launch | Customer security owner | Pending |
| D05 | Historical findings and duplicates | Prepare a sanitized known-issues register and confirm its handling before launch | Customer program owner | Pending |

## Communication approach

The status message to leadership should distinguish three things:
- **What is confirmed:** the proposed launch has unresolved authorization and access prerequisites.
- **What is being done:** engineering/security are assigned the relevant evidence and approval tasks.
- **What would change the decision:** explicit, documented completion of all launch-critical gates and formal customer approval.

See the [sample customer kickoff email](customer-email.md) and [launch readiness checklist](launch-readiness.md).

---

**Portfolio disclosure:** This is a proposed decision framework in a fictional delivery case study. No actual customer has accepted risk, approved a launch, or authorized researcher testing.

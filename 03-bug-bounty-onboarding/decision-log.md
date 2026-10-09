# Onboarding Decision Log — Asteria Cloud

**Case study type:** Fictional, educational simulation. No actual customer decisions or approvals.

| ID | Question / trade-off | Options | Current status | Decision owner | What evidence is needed? |
| --- | --- | --- | --- | --- | --- |
| D01 | Launch next week if safe test accounts are not ready? | Delay / limit scope to an approved safe target / launch anyway | **Candidate recommends NO-GO — customer approval not simulated** | Customer program owner | Test-account readiness, signed-off scope, safety review |
| D02 | Stage-only program or add production? | Stage-only / production with safeguards | Open | Customer security/program owner | Asset inventory, permissions and risk review |
| D03 | Researcher incentives | Approve reward schedule / keep pending | Open | Customer budget/program owner | Approved funding, VRT mapping and brief |
| D04 | Escalation route for urgent findings | Existing incident process / new named route | Open | Customer security owner | Contacts, response coverage, tested routing |
| D05 | Import known issues before launch | Import sanitized list / defer with documented risks | Open | Customer program owner | Known-issue inventory and platform import validation |

## Candidate interview exercise — D01

**Fictional event:** On the planned launch date, the customer says its dedicated staging accounts are not ready. Leadership is pressuring the delivery team to launch on time.

**Question:** As the Technical Engagement Manager, would you launch, delay, or reduce scope? What would you communicate in the next customer meeting?

**Candidate's original answer — verbatim (October 9, 2026):**

> I wouldn't recomend going live until engineering team is ready and would point out the risks

*Original wording, capitalization and spelling retained exactly. This is the candidate's own answer.*

**Decision the candidate actually proposed:** Recommend **NO-GO** until engineering is ready; explain launch risks. This is a recommendation in a fictional interview, not an approval or action taken in a real program.

### Interview assessment — coach's feedback (not written by the candidate)

**Practice score: 7/10.** This is a subjective coaching assessment, not an official Bugcrowd recruiting score.

**Strengths:**
- Prioritizes safe readiness instead of yielding to launch-date pressure.
- Shows an awareness of delivery risk.
- Recognizes the need to communicate risks to stakeholders.

**Areas to strengthen:**
- The **program scope is also unapproved**, not only the test accounts. Researcher testing should not begin without explicit in-scope authorization.
- Identify accountable owners for test-account readiness (customer engineering) and scope signoff (customer security/program owner).
- Recommend an agreed next checkpoint and a documented launch-blocker list.
- If leadership wants to protect the date, explore a **limited, fully approved** launch only if all permissions, testing accounts, safety rules, response ownership and other critical gates are met.
- Maintain clear boundaries: the Technical Engagement Manager coordinates readiness and makes the recommendation; the authorized customer/program owner approves the final go/no-go.

### Suggested stronger response — **coach-generated example, not the candidate's words**

> I would recommend postponing the launch until the critical readiness requirements are met, particularly the availability of test accounts and formal approval of the program scope.
>
> I would clearly communicate the risks to the customer and leadership, assign owners to the outstanding dependencies, and establish a revised readiness checkpoint.
>
> If the customer wanted to maintain the original timeline, I would explore whether a limited launch with a fully approved scope and validated testing environment was feasible.
>
> My priority would be to protect the customer while maintaining transparency, accountability, and progress toward a successful launch.

### D01 — Sample decision record (coach-generated; not an approved customer decision)

| Field | Simulated working entry |
| --- | --- |
| Recommendation | **NO-GO** until mandatory readiness controls pass |
| Evidence | Engineering test accounts unavailable; customer security has not approved scope |
| Primary risk | Researcher access could be unsafe or outside authorized testing boundaries |
| Option 1 | Postpone full launch; complete readiness and repeat gate review |
| Option 2 | Consider a reduced-scope launch **only** with separate approval, validated safe accounts, exact targets, and complete launch requirements |
| Required owners | Customer engineering: safe test accounts. Customer security/program owner: scope approval. Coordinator: blockers, dependencies and communications |
| Decision authority | Authorized customer program owner, with security/legal input as required |
| Next checkpoint | Agree on a specific review meeting after prerequisite evidence is provided; no date invented |
| Customer communication | Coach's suggested response above; **not sent** |
| Final launch approval | **Not granted or simulated** |

### Candidate reflection — next exercise

**Question:** Leadership still wants the scheduled launch. What three specific pieces of evidence would you require before reconsidering the NO-GO recommendation?

**Candidate's new answer:** _Pending._
## Decision-record format to use

- Decision:
- Alternative options evaluated:
- Risk / potential consequence:
- Evidence currently available:
- Owner with authority to approve:
- Temporary control or dependency:
- Next checkpoint:
- Communication sent:
- Final approval state:

A candidate-generated answer will be added without rewriting it as if it were the coach's text. Suggested improvements, when provided, will be labeled separately.

**Reminder:** A mock decision log is a portfolio artifact; it does not indicate that any real customer has accepted risk or authorized testing.

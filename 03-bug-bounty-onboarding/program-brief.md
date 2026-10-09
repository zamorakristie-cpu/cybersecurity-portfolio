# Asteria Cloud — Draft Private Program Brief

> **FICTIONAL / TRAINING-ONLY DRAFT — NOT AUTHORIZATION TO TEST.**  
> The business and `.test` domains are invented. This document is an example of what a researcher-facing brief might include. The authorized program owner must approve every term before any real launch.

## Program overview

Asteria Cloud is a hypothetical B2B SaaS provider with tenant-based accounts and an API. The *proposed* private bug bounty would focus on identifying vulnerabilities involving authentication, tenant separation, horizontal/vertical authorization, and potential disclosure of sensitive data.

**Program type:** Private, invite-only (proposed)  
**Program status:** Not launched  
**Primary focus:** Broken access control, IDOR, authentication and API security

## Proposed targets — fictional staging environment only

| Target | Included functionality | Boundary |
| --- | --- | --- |
| `https://staging-app.asteria.test` | Web dashboard, account settings and test-user workflows | Exact hostname only |
| `https://staging-api.asteria.test/v1/` | Documented API routes in version 1 | Exact hostname and `/v1/` path only |

The reserved `.test` domain is used solely to illustrate scope in this case study. It does **not** resolve to an authorized research target. A real program requires actual, expressly approved assets and verifiable ownership.

## Out of scope (proposed)

- All production environments and domains other than the two explicitly listed staging targets.
- Third-party identity, cloud, payment or analytics infrastructure.
- Real customers, real customer data and employee accounts.
- Availability testing, denial-of-service, stress testing, destructive payloads and unrestricted scanning.
- Social engineering, phishing, physical testing and attacks on other researchers.

Any exception would require **explicit written authorization and a revised brief before testing**.

## Account access and test data

- Test identities must be provisioned by the customer for participating researchers.
- Use synthetic tenants and records; avoid real personal or confidential customer data.
- Researcher credentials must be distributed securely and never posted publicly.
- Report leaked credentials securely through the program's designated channel.

**Blocker:** Account provisioning plan and confirmed environment isolation are **not yet approved**.

## Reporting guidance

A useful report should include:
1. Concise title and affected target.
2. Prerequisites and test account roles.
3. Exact reproduction steps (sanitize tokens and secrets).
4. Actual versus expected behavior.
5. Security/business impact supported by evidence.
6. Screenshots or sanitized HTTP requests/responses.
7. Remediation suggestions where appropriate.

Submit through the real program's designated channel, if a real program is ever authorized. **No intake address or URL is designated in this mock brief.**

## Safety, privacy and disclosure

- Stay strictly within authorized scope; stop if data from a real person or third party appears.
- Minimize proof-of-concept impact and collection of data; do not retain unnecessary sensitive information.
- Do not use, share or publish captured credentials, secrets or non-public findings.
- Follow the approved program disclosure terms and coordination process.
- Researcher safe harbor and legal terms require approval by the customer's authorized legal/security team; none is granted by this sample.

## Rewards, priority and known issues

- **Reward eligibility and amounts:** Pending program-owner approval; no reward promise exists.
- **Severity framework:** Bugcrowd VRT can be a reference but final program-specific mappings require agreement.
- **Known-issue import:** Pending. Prepare a redacted list of previously reported issues before launch to support duplicate triage.
- **Potential focus example:** An IDOR exposing another test account's API key, modeled on my [completed PortSwigger lab](../01-idor-access-control/vulnerability-report.md). This is **illustrative**, not evidence of a vulnerability in Asteria Cloud.

## Signoff gate

Not approved for launch until scope, ownership, test access, confidentiality terms, rewards, contact channels, researcher safety rules, and response process are explicitly confirmed.

## Reference

[Bugcrowd: Program Brief and onboarding guidance](https://docs.bugcrowd.com/customers/onboarding/with-bugcrowd/)

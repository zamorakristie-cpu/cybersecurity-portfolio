# Lab 01 — User ID Controlled by Request Parameter

**Source:** [PortSwigger Web Security Academy — User ID controlled by request parameter](https://portswigger.net/web-security/access-control/lab-user-id-controlled-by-request-parameter)  
**Environment:** Authorized PortSwigger training lab  
**Status:** Solved manually; screenshots and formal evidence report pending  
**Observed testing method:** Changed the user identifier in the account page URL using a browser (Burp Suite was not required)

## Objective and vulnerability
The official lab describes a **horizontal privilege escalation** flaw in the account page. Its challenge is to obtain the API key associated with the training user `carlos` using access from the training user `wiener`. The URL's `id` parameter selects the user account.

This is a lab example of broken object-level authorization / IDOR.

## Conceptual request difference
These are patterns from the lab instructions, **not captured HTTP evidence**:

```text
/my-account?id=wiener
/my-account?id=carlos
```

Changing a URL parameter should never grant access to someone else's private account resources.

## Evidence checklist
- [ ] **E01:** Original account page with `id=wiener`
- [ ] **E02:** Modified account page with `id=carlos`, showing the result **with the API key fully redacted**
- [ ] **E03:** PortSwigger "Lab Solved" confirmation
- [ ] **E04 (optional):** Sanitized Burp Repeater request and response comparison
- [ ] Complete [vulnerability-report.md](vulnerability-report.md) with actual steps and findings

## Publishing safety
Use only your authorized training lab. Redact any API keys (including the lab key), session cookies, credentials, tokens and personal information before publishing screenshots. Do not publish the unredacted HTTP response if it contains a key.

## Portfolio integrity
Training lab only—not a production discovery, commercial penetration test or real bug bounty submission. The learner completed this lab manually by changing the URL.

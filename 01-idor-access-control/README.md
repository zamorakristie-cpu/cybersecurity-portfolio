# Lab 01 — IDOR / Broken Access Control

**Environment:** PortSwigger Web Security Academy (authorized training lab)  
**Status:** Lab solved manually; Burp reproduction, screenshots, and complete report pending  
**Method used so far:** Changed a user identifier in the browser URL

## Objective
Investigate whether changing an object/user identifier in a URL can expose a resource without the appropriate authorization check.

## What I did (confirmed)
I completed the PortSwigger access-control training challenge by changing the URL. I did **not** need Burp Suite to solve the challenge.

## Evidence to collect next
- [ ] Record the exact lab title and link
- [ ] Record the original request URL with sensitive values removed
- [ ] Record the modified identifier and resulting page/response
- [ ] Capture the lab-solved confirmation
- [ ] Optionally reproduce with Burp Proxy / Repeater and save sanitized HTTP exchanges
- [ ] Write a clear finding and risk assessment in [vulnerability-report.md](vulnerability-report.md)

**Evidence policy:** Only collect evidence in your own authorized lab instance. Redact session cookies, credentials, tokens, API keys, and any other sensitive material before uploading.

## Portfolio integrity
This is a **training exercise**, not a reported production vulnerability or a paid bug bounty. Any impact and severity assessment should be based on the behavior actually reproduced.

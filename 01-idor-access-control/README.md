# Lab 01 — User ID Controlled by Request Parameter

**Lab:** [PortSwigger Web Security Academy — User ID controlled by request parameter](https://portswigger.net/web-security/access-control/lab-user-id-controlled-by-request-parameter)  
**Test date:** October 9, 2026  
**Environment:** PortSwigger's authorized, intentionally vulnerable lab  
**Status:** **Solved and reproduced in screenshots**; sanitized screenshot uploads to this repository are pending.  
**Method:** Chrome browser, manually modifying the `id` URL parameter; no Burp Suite used.

## Objective

Evaluate whether the signed-in user `wiener` can view account information for `carlos` by changing a URL parameter. The exercise demonstrates **horizontal privilege escalation / insecure direct object reference (IDOR)**.

## Actual observations

1. Signed in to the lab as `wiener`.
2. Navigated to `/my-account?id=wiener`; the page displayed username `wiener` and a training API key.
3. Edited the address bar to request `/my-account?id=carlos` in the same browsing session.
4. The application displayed username `carlos` and Carlos's training API key, even though the user had not logged in as Carlos.
5. The PortSwigger interface subsequently displayed **Solved** and **Congratulations, you solved the lab!**.

These observations are supported by screenshots provided by the learner. They are from the training application only, not a production engagement.

## Evidence captured

| File to upload | What it shows | Status |
| --- | --- | --- |
| `E01_authorized_wiener.png` | Original `id=wiener` account page | Captured; API key redacted; upload pending |
| `E02_unauthorized_carlos.png` | Modified `id=carlos` account page | Captured; API key redacted; upload pending |
| `E03_lab_solved.png` | PortSwigger successful lab completion | Captured; API key redacted; upload pending |

**Publish only the sanitized images**. The unedited screenshots contain visible training API keys. The screenshot files are prepared locally for upload but have **not been uploaded** to GitHub.

## Technical report

See [vulnerability-report.md](vulnerability-report.md) for steps, root cause, impact, remediation and validation plan.

## Next lab extension (optional)

Repeat the same authorized training scenario in **Burp Suite Repeater** to record sanitized raw HTTP requests and responses. This is not required to substantiate the existing browser-based observation, and it has not been performed yet.

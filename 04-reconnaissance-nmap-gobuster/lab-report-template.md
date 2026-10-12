# Nmap & Gobuster — Authorized Local Reconnaissance Report

**Status:** TEMPLATE — **NOT YET EXECUTED**  
**Exercise:** Synthetic localhost web application (no production or third-party systems)

> Replace the bracketed placeholders only after performing the lab. Do not invent findings, tool versions or screenshots.

## 1. Engagement summary

| Field | Record after running |
| --- | --- |
| Scan date | [YYYY-MM-DD] |
| Operator | [Name or handle] |
| Test platform | [macOS / Kali / Ubuntu, version if known] |
| Authorization | Localhost-only service created and controlled by operator |
| Target | `127.0.0.1`, port `8000` |
| Nmap version | [Observed version] |
| Gobuster version | [Observed version] |
| Service used | Python 3 `http.server`, loopback only |

## 2. Nmap observations

**Commands used:**

```bash
nmap -sT -p 8000 --reason 127.0.0.1
nmap -sT -sV -p 8000 127.0.0.1
```

**Sanitized actual output:** [Add output only after running commands]

| Port | State reported by Nmap | Service / detected version | Confidence / limitations |
| --- | --- | --- | --- |
| TCP 8000 | [Actual state] | [Actual service probe result] | [Notes] |

**Interpretation:** [What does the observed state mean? How did service detection behave?]

## 3. Gobuster observations

**Command used:**

```bash
gobuster dir -u http://127.0.0.1:8000/ -w /tmp/recon-demo/wordlist.txt -t 2
```

**Sanitized actual output:** [Add output only after running]

| Path | HTTP status | Why observed / follow-up |
| --- | --- | --- |
| [Actual result] | [Actual code] | [Reason / redirect notes] |

**Interpretation:** [Explain why finding a path alone is not a confirmed vulnerability.]

## 4. Security assessment

- **Observed exposure:** [State only what test output supports.]
- **Authentication/authorization:** [Not assessed unless additional authorized tests were performed.]
- **Confirmed vulnerability:** [None claimed by this lab unless supported by separate evidence.]
- **Risk considerations:** [Example: listener scope, intended use, data sensitivity.]
- **Recommendation:** [Evidence-backed action or “not applicable” for intentionally exposed demo paths.]

## 5. Evidence inventory

| ID | File or link | Description | Publication status |
| --- | --- | --- | --- |
| E01 | [Pending] | Nmap port-state output | Not collected |
| E02 | [Pending] | Nmap service detection | Not collected |
| E03 | [Pending] | Gobuster path enumeration | Not collected |

## 6. Retesting / closure

[Document changes, rescans, unexpected outcomes, or troubleshooting after performing the lab.]

**Integrity statement:** The report is a placeholder until the learner captures and reviews the local test results. No customer scan or penetration test is implied.

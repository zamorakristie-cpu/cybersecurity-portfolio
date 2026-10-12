# Project 04 — Nmap & Gobuster: Local Reconnaissance Lab

**Focus:** Network enumeration, TCP service discovery, web content discovery and reporting  
**Environment:** macOS terminal or personal Linux VM  
**Target:** `127.0.0.1` / `http://127.0.0.1:8000/` (the machine running this lab)  
**Status:** **Prepared — hands-on testing and evidence pending**

> **Authorization and accuracy:** This project provides instructions for testing a web server intentionally created on my own machine. I have **not yet performed or documented the scans**. This lab does not authorize scanning another system, a public website, an employer network, or a real bug bounty target.

## Objective

Demonstrate a basic authorized reconnaissance workflow:

1. **Nmap** identifies whether a specific TCP port on my localhost is open and attempts to identify its listening service.
2. **Gobuster** requests candidate directories from a deliberately configured local test web server using a tiny custom wordlist.
3. Findings are interpreted in terms of exposure, confidence and potential next steps, without assuming that an open port or a discovered path is automatically a vulnerability.

## Tools

- **Nmap:** Network Mapper — [official reference](https://nmap.org/book/man.html)
- **Gobuster:** web directory and DNS enumeration tool; this lab uses its `dir` mode — [official repository](https://github.com/OJ/gobuster)
- **Python 3:** temporary localhost-only web server

Check installation:

```bash
nmap --version
gobuster version
python3 --version
```

If the Gobuster version command differs on your installation, check `gobuster --help`. On macOS with Homebrew available, use `brew install nmap gobuster`; otherwise see the official project installation guides.

## Lab setup: create a safe local target

Run the following in **Terminal 1** on your own machine. A temporary website will be created inside `/tmp`. It has a homepage and two intentionally created directories:

```bash
mkdir -p /tmp/recon-demo/site/admin /tmp/recon-demo/site/docs
printf 'Local reconnaissance practice site\n' > /tmp/recon-demo/site/index.html
printf 'Test admin directory, no real access controls\n' > /tmp/recon-demo/site/admin/index.html
printf 'Test documentation directory\n' > /tmp/recon-demo/site/docs/index.html
printf 'admin\ndocs\nmissing\n' > /tmp/recon-demo/wordlist.txt

cd /tmp/recon-demo/site
python3 -m http.server 8000 --bind 127.0.0.1
```

Leave Terminal 1 running during the scans. The server listens **only on loopback** (`127.0.0.1`). The wordlist is **outside** the served website root.

> Using `python3 -m http.server` serves files under the current directory. Do not run it from a personal documents folder or a location containing secrets. This example intentionally uses a small synthetic website.

## Part A — Nmap: identify the local listening port

Open **Terminal 2** and run:

```bash
nmap -sT -p 8000 --reason 127.0.0.1
```

Interpret the resulting state (`open`, `closed`, or `filtered`) and the reason supplied by Nmap. The lab is designed to make TCP 8000 **open while the test server is running**, but record what your own machine actually reports.

Next, attempt service detection:

```bash
nmap -sT -sV -p 8000 127.0.0.1
```

| Item | Meaning |
| --- | --- |
| `-sT` | TCP connect scan (does not require raw-packet privileges) |
| `-p 8000` | Scan only TCP port 8000 |
| `--reason` | Show why Nmap assigned the reported port state |
| `-sV` | Probe for a service and, where possible, version information |
| `127.0.0.1` | The local loopback host, not an external target |

**Technical interpretation:** An `open` port means something accepted connections; it does not prove a security flaw. Service detection is best-effort and must be validated before reporting a product/version.

## Part B — Gobuster: find deliberately created directories

With Terminal 1 still running, execute from Terminal 2:

```bash
gobuster dir -u http://127.0.0.1:8000/ -w /tmp/recon-demo/wordlist.txt -t 2
```

| Item | Meaning |
| --- | --- |
| `dir` | Gobuster's directory/content enumeration mode |
| `-u` | URL for the **authorized local** website |
| `-w` | Path to the custom wordlist (`admin`, `docs`, `missing`) |
| `-t 2` | Limit concurrent workers to two in this beginner demonstration |

The test site contains `/admin/` and `/docs/` by design, and does not intentionally include `/missing/`. Gobuster may report directory redirects (for example, HTTP 301) before reaching the trailing-slash URL. Record the response status codes you **actually observe**.

**Technical interpretation:** Directory enumeration helps identify reachable routes or resources. A discovered `/admin/` path alone is **not** proof of broken authentication, unauthorized access, or any other vulnerability. Further testing must stay within explicitly permitted scope.

## Part C — Clean up

Stop the Python server in Terminal 1 with **Ctrl+C**. If desired, run the targeted Nmap command again to see whether port 8000 changes state. Another process could still be listening; avoid assuming the result.

The temporary files can be removed manually when no longer needed: `/tmp/recon-demo/`.

## Evidence and report

After performing the lab, complete the [reconnaissance report template](lab-report-template.md) using your own observed results and version numbers. See [evidence-handling guidance](evidence/README.md) before uploading screenshots, terminal output or text files.

**Evidence to capture when available:**
- Version check of Nmap and Gobuster.
- Nmap result for localhost TCP 8000.
- Nmap service-detection result.
- Gobuster results with paths/status codes.
- Short analysis: what was observed, what was **not** established, and why.

## Relevance to security and delivery

This lab is intended to build my ability to interpret network evidence, explain the difference between **reconnaissance** and **vulnerability confirmation**, and communicate findings in a concise, reproducible report.

## References

- [Nmap Reference Guide](https://nmap.org/book/man.html)
- [Gobuster project documentation](https://github.com/OJ/gobuster)

**Project integrity:** Until real local outputs are added, this is a **lab guide**, not proof of completed scanning.

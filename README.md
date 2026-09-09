## Kamil Mete Yalçınkaya

Cybersecurity student in Warsaw. I build detection and analysis tooling, and I break my own
applications before someone else does.

Most of what I write ends up being about the gap between a control existing and a control working.
A rule that has never been tested against telemetry is a guess. A checksum with a constant salt is
tamper-evidence, not authentication. An encryption key that regenerates on restart silently makes
its own data unreadable. Those distinctions are what the repositories below are actually about.

### Detection and response

**[detection-engineering-lab](https://github.com/Metercedes/detection-engineering-lab)** —
15 Sigma detections for Windows, Linux and authentication telemetry, with an offline evaluator so
every rule can be validated against deterministic telemetry without a SIEM. Each rule ships the
events it must match and a benign baseline it must not. 18 ATT&CK techniques, 138 tests.

**[sentinel-kql-detections](https://github.com/Metercedes/sentinel-kql-detections)** —
10 Microsoft Sentinel analytics rules and 3 hunting queries across Entra ID, Defender and the
Windows Security log, plus a static analyser that resolves every column reference against
checked-in table schemas. A mistyped column makes a Sentinel rule return nothing forever without
any error. 14 ATT&CK techniques, 68 tests.

**[soc-triage-toolkit](https://github.com/Metercedes/soc-triage-toolkit)** —
Turns a reported phishing message into an analyst report: which headers disagree, where it really
came from, what the attachments hash to, every indicator extracted and defanged. Evidence rather
than a score.

**[network-incident-triage](https://github.com/Metercedes/network-incident-triage)** —
PCAP triage in pure Python: flows, DNS, TLS server names, HTTP metadata, and detection of scans
and beaconing. The parser is written from the format specifications and checked against tshark on
every fixture.

### Application and supply-chain security

**[secure-notes-api](https://github.com/Metercedes/secure-notes-api)** —
Spring Boot REST API with rotating refresh tokens, replay detection that revokes the whole token
family, and per-owner access control proved by negative tests. The build fails on a dependency
with a known critical vulnerability, which it currently catches.

**[secure-recruitment-platform](https://github.com/Metercedes/secure-recruitment-platform)** —
A university project of mine, reviewed as if it were someone else's code. Twelve findings, worst
of them an authentication bypass through a client-supplied header, each fixed with a regression
test. The vulnerable code stays in the history so the review can be checked against it.

**[vulnerability-prioritization-workbench](https://github.com/Metercedes/vulnerability-prioritization-workbench)** —
Reconciles Trivy and Grype output into one set of findings, enriches with CISA KEV and EPSS, and
orders remediation with a stated reason for every decision. On the sample scan, 262 raw findings
are the same 131 vulnerabilities.

### Reverse engineering

**[save-format-research](https://github.com/Metercedes/save-format-research)** —
Working out what an unknown binary container is: entropy and signature triage, telling obfuscation
apart from encryption, recovering a repeating-key XOR from ciphertext alone, and identifying which
digest construction produced a checksum from one known-good file.

### Working with

Python, Java, Bash, KQL. Sigma, MITRE ATT&CK, Elastic Security, Microsoft Sentinel, Defender XDR,
Wireshark and tshark. Spring Security, OWASP Top 10, CVSS, EPSS, CISA KEV, Trivy, Grype, CodeQL,
SBOM and CI security gates.

### Education

Cybersecurity, Uniwersytet VIZJA, Warsaw. VKV Koç School. IELTS Academic 6.5.

### Contact

[ymete089@gmail.com](mailto:ymete089@gmail.com)

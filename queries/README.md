# 🔍 Queries

Detection logic, search queries, and analytics rules from this lab.

**Primary language:** Detection queries

---

## How to organize this folder

```
queries/
├── 01-brute-force.txt
├── 02-anomalous-signin.txt
└── 03-data-exfiltration.txt
```

For each query file, include a header comment with:
- What the query detects
- Which MITRE ATT&CK technique it maps to
- The data source it depends on
- Known false positives

Example header:

```
// Detection: Brute-force login attempts
// MITRE: T1110 — Brute Force
// Source: SecurityEvent (Windows logon events)
// FP: scheduled tasks running with wrong cached creds; service account testing
```

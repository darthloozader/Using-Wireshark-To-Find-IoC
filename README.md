# 🛡️ Network Security: Implementing Basic Network Security

> Hands-on cybersecurity lab from Pluralsight with implementation notes and outcomes.

![Platform](https://img.shields.io/badge/platform-Pluralsight-39ff7a?style=flat-square)
![Status](https://img.shields.io/badge/status-complete-39ff7a?style=flat-square)
![Date](https://img.shields.io/badge/date-2026--05--20-blue?style=flat-square)

---

## 📌 Overview

This repository documents my hands-on completion of **Pluralsight Hands-On Lab — Network Security: Implementing Basic Network Security** on **Pluralsight**.
It includes the methodology I followed, tools I used, evidence I captured, and the skills I demonstrated.

**Lab URL:** https://app.pluralsight.com/hands-on/labs/09462adf-0dc2-4eac-94ba-11949025122c?originUrl=https%3A%2F%2Fapp.pluralsight.com%2Fhands-on

---

## 🎯 Objectives

- Complete the guided hands-on lab from start to finish
- Demonstrate endpoint threat detection and triage
- Use network traffic PCAP to identify IoC
- Document the process for future reference and portfolio

---

## 🧰 Tools & Technologies

`Pluralsight Hands-On Sandbox` · `Wireshark` · `VirusTotal`  

---

## 🧠 Security Concepts Demonstrated

- Analyze network traffic to identify malicious activity amongst normal legitimate traffic and find the victim host
- Find the victim host to quarantine

---

## 🪜 Walkthrough
<!--
> Replace this section with your actual step-by-step walkthrough.
> Use the placeholders below as a starting structure.
-->
### Step 1 — Setup & Recon
Loaded network traffic capture into Wireshark.

### Step 2 — Investigation & Detection

The endpoint became infected when the user clicked a Microsoft Word macro.

> Filtered PCAP for TLS handshakes to find an anomalous client/server connection.
```
tls.handshake.type eq 1
```
### Step 3 — Analyze
> Found suspicious .dll file being downloaded.
> > Extracted malicious file from Wireshark.
> > Analyzed file in sandboxed environment & VirusTotal.
> > Malware attempted to call out to control server.

### Step 4 — Cleanup & Reflection
Identified compromised endpoint to quarantine

### 📝 My Lab Notes

> The following are my raw notes captured during the lab.

```
Used Wireshark to find IoC. Filtered for TLS handshakes. Extracted the malicious file for analysis in the sandbox. Discovered malware attempting to call out to the C2 server. Identified the compromised endpoint to quarantine.
```

---

## 📸 Screenshots


### Lab Environment

> Following HTTP Stream & Find Executable

![Lab Environment](screenshots/lab-environment.png)

### Anomalous Traffic

> Key configuration step

![Configuration](screenshots/configuration.png)

### Infected Host

> Mapping victim IP address to hostname to quarantine

![Validation](screenshots/validation.png)

### Completion

> Lab completion screen

![Completion](screenshots/completion.png)

---

## 🎯 MITRE ATT&CK Mapping

| ID | Tactic / Technique | How it appears in this lab |
|----|--------------------|----------------------------|
| `T1574` | Hijack Execution Flow: DLL | Dridex can abuse legitimate Windows executables to side-load malicious DLL files |
| `T1071` | Application Layer Protocol: Web Protocols | Dridex used POST requests and HTTPS for C2 communications. |

---

## 🧠 What I Learned

- Bridging theory to practice in a sandboxed environment
- How production-style configurations differ from documentation examples
- Why structured note-taking accelerates the learning curve

---

## 🛠️ Skills Gained

- Pluralsight Hands-On Sandbox
- Cloud console (Azure / AWS / GCP)
- Wireshark 
- VirusTotal

---

## 💼 Resume Bullets


- Completed Pluralsight hands-on cybersecurity lab: Network Security: Implementing Basic Network Security
- Applied lab concepts in a real cloud environment with documented outcomes
- Built portfolio writeup with screenshots, configuration notes, and lessons learned

---

## 🔗 References

- [Pluralsight](https://app.pluralsight.com/hands-on/labs/09462adf-0dc2-4eac-94ba-11949025122c?originUrl=https%3A%2F%2Fapp.pluralsight.com%2Fhands-on)
- [MITRE ATT&CK Framework](https://attack.mitre.org/)
- [GitHub Markdown Guide](https://docs.github.com/en/get-started/writing-on-github)

---

## 👤 About Me

I'm **Jonathan Luzader**, a cybersecurity student building public proof-of-skill through hands-on labs and detailed writeups.

- 🌐 GitHub: [@darthloozader](https://github.com/darthloozader)
- 📂 More projects: see my [pinned repositories](https://github.com/darthloozader)

---

## 📝 License

MIT — see [LICENSE](LICENSE).

---

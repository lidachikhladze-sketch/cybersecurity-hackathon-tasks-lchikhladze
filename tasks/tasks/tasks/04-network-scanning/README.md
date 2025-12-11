# Task 4 – Network Scanning & Enumeration

## Challenge  
Perform network scanning and information gathering on a target host.  
Identify:

- Open ports  
- Running services  
- Service versions  
- Potential CVE vulnerabilities  
- OSINT data (e.g., Shodan results)  
- Indicators of weak or outdated services  

Target IP (training / practice context):  
116.203.39.76

> ⚠️ **Important:**  
> All scanning must be done only on hosts you own or have explicit permission to test.  
> This task was performed in an educational context.

---

## Methodology

### 1️⃣ **Initial Scan with Nmap**

I started with a SYN scan plus version detection:

```bash
nmap -sS -sV -sC -Pn 116.203.39.76
This helps discover:

Open TCP ports

Service banners

Basic script-based enumeration (via -sC)

If specific ports were discovered, a deeper scan can be: nmap -p 22,80,443 -sV -sC 116.203.39.76
Service Fingerprinting

Using Nmap results, I noted:

service names

detected version numbers

SSL/TLS info (if port 443 is open)

These version numbers were used to check for potential CVEs.

OSINT Check with Shodan

Using Shodan:

Verified which ports Shodan sees as open

Compared banners with Nmap

Looked for tagged vulnerabilities

Checked host metadata (uptime, open ports, service fingerprints)

Shodan URL structure (example): https://www.shodan.io/host/<IP>

High-Level Vulnerability Review

For each discovered service version, I researched:

CVE entries (NVD database)

vendor advisories

public exploit reports (if outdated versions appeared)

No exploitation was performed.
The goal was learning enumeration, not attack execution.

Tools Used:
Kali Linux
Nmap
Shodan.io
Basic OSINT techniques

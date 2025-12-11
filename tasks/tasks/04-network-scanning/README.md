# Task 4 – Network Scanning & Enumeration

## Challenge

Perform network scanning and information gathering on a target host.  
The goal is to identify:

- Open ports  
- Running services  
- Service versions  
- Potential CVE vulnerabilities  
- OSINT data (e.g., Shodan results)  
- Indicators of weak or outdated services  

---

## Target IP (training/practice environment)

116.203.39.76


> ⚠️ **Important:**  
> • All scanning must be done only on hosts you own or have explicit permission to test.  
> • This task was performed in an educational context only.

---

## Methodology

### 🔍 1. Initial Scan with Nmap

I started with a SYN scan plus version detection:

nmap -sS -sV 116.203.39.76


This identifies:

- Open ports  
- Running services  
- Version numbers  

---

### 🔍 2. Full Port Scan (All 65535 Ports)

nmap -p- 116.203.39.76


This helps uncover non-standard ports that may run hidden services.

---

### 🔍 3. Service Enumeration

Once open ports were found, I used:


This performs:

- Default script scanning  
- Service fingerprinting  
- Detection of outdated or vulnerable versions  

---

### 🔍 4. OSINT Review with Shodan

I searched the IP on Shodan:

https://www.shodan.io/host/116.203.39.76

On Shodan, I reviewed:

- Open ports  
- Banner information  
- Metadata (uptime, ISP, region)  
- Possible vulnerabilities  

I compared Shodan’s results with Nmap findings to see which ports matched.

---

### 🔍 5. High-Level Vulnerability Review

For each discovered service version, I researched:

- CVE entries (NVD database)  
- Vendor advisories  
- Public exploit reports (if outdated versions appeared)  

> ⚠️ No exploitation was performed.  
> This task focuses only on scanning and enumeration — not attacking.

---

## Tools Used

- Kali Linux  
- Nmap  
- Shodan.io  
- Basic OSINT techniques  

---

## Key Learning

- How to map a target host safely using Nmap  
- Why OSINT platforms like Shodan are important  
- The role of version detection in vulnerability analysis  
- Importance of ethical boundaries during reconnaissance  


# 🛡️ Week 02 – Cybersecurity Reconnaissance & Network Scanning

## 📌 Project Information

- **Author:** Uttam Parmar
- **Role:** Cybersecurity Professional
- **Program:** Cybersecurity & Ethical Hacking Internship
- **Organization:** Networkwalks
- **Batch:** B084
- **Assessment Date:** 14 November 2026
- **Deliverable:** Week 02 Practical Penetration Testing Report

---

## 📍 Project Overview

This repository showcases my Week 02 practical work completed during the Cybersecurity & Ethical Hacking Internship at Networkwalks.

The project focuses on two important stages of penetration testing: **Footprinting & Reconnaissance** and **Network Scanning & Discovery**.

During these practical exercises, I used Kali Linux command-line utilities and Zenmap to gather domain intelligence, identify web technologies, enumerate DNS records, inspect HTTP headers, detect Web Application Firewall (WAF) technology, and discover active devices on my local network.

### Key Objectives

- Collect publicly available domain registration information.
- Identify website technologies and server details.
- Perform DNS resolution and DNS record enumeration.
- Inspect HTTP response headers.
- Identify Web Application Firewall technology.
- Discover live hosts and open ports on a local network.
- Understand network topology through Zenmap.

---

## ⚙️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Reconnaissance environment |
| WHOIS | Domain registration information |
| WhatWeb | Website technology fingerprinting |
| Nslookup | DNS resolution |
| cURL | HTTP response header inspection |
| Wafw00f | WAF detection |
| DNSRecon | DNS record enumeration |
| Zenmap | Network discovery and topology mapping |
| Nmap | Network scanning engine |
| Windows | Zenmap scanning environment |

---

## 🔍 Phase 1: Footprinting & Reconnaissance

**Target:** `networkwalks.com`

Performed domain reconnaissance using six Kali Linux tools.

### Commands Executed

```bash
whois networkwalks.com

whatweb networkwalks.com

nslookup networkwalks.com

curl -I https://networkwalks.com

wafw00f networkwalks.com

dnsrecon -d networkwalks.com
```

### Key Findings

| Reconnaissance Area | Observation |
|---|---|
| Domain IP | 192.232.216.135 |
| Registrar | GoDaddy.com, LLC |
| Web Server | Apache |
| CMS | WordPress 7.1.4 |
| DNS | SOA, NS, MX, A, AAAA and SRV records |
| WAF | ModSecurity (SpiderLabs) |
| DNSSEC | Unsigned |
| Public Email | info@networkwalks.com |

---

## 🌐 Phase 2: Network Scanning & Discovery

**Environment:** Personal Local Network

**Target Subnet:** `10.120.1.0/24`

Used Zenmap (Nmap GUI) to identify active devices, inspect network services and visualize the local network topology.

### Scanning Commands

**1. Host Discovery & Quick Scan**

```bash
nmap -T4 -F 10.120.1.0/24
```

**2. Detailed Network Scan**

```bash
nmap -T4 -A -v 10.120.1.188
```

### Network Discovery Results

| IP Address | MAC Address | Vendor | Key Findings |
|---|---|---|---|
| 10.120.1.76 | 7A:36:0A:93:5D:A2 | Unknown | Filtered port 7 |
| 10.120.1.174 | 3E:34:69:51:E9:78 | Unknown | Port 53 DNS |
| 10.120.1.188 | Not shown | Not shown | Ports 135, 139, 445, 3306, 5432 |

### Scanning Summary

- Scanned 256 IP addresses.
- Discovered 3 live hosts.
- Identified MAC address information where available.
- Examined open and filtered ports.
- Visualized discovered devices using Zenmap Topology.

---

## ⚠️ Risk Analysis & Security Observations

The practical assessment identified several potential security concerns:

| Finding | Risk Level |
|---|---|
| Exposed web technology information | Medium |
| Server IP identification | Low |
| Missing commonly recommended HTTP headers | Low |
| DNS infrastructure information exposure | Medium |
| DNS recursion reported enabled | Medium |
| DNSSEC unsigned | Low |
| Public email exposure | Low |
| Multiple live network hosts | Medium |
| SMB/NetBIOS services visible | Medium |
| Database ports exposed internally | Medium |

**Note:** These are observations from reconnaissance and scanning, not confirmed vulnerabilities. No exploitation or vulnerability validation was performed.

---

## 🛡️ Defensive Recommendations

1. Regularly review publicly exposed website technologies.
2. Keep CMS platforms and plugins updated.
3. Improve HTTP security header configuration.
4. Review DNS records and disable unnecessary open recursion.
5. Consider enabling DNSSEC.
6. Properly configure and monitor WAF protection.
7. Reduce unnecessary public email exposure.
8. Restrict database access through firewall rules.
9. Investigate unknown devices on local networks.
10. Perform regular authorized network security assessments.

---

## 📂 Repository Structure

```text
Uttam-Parmar-Cybersecurity-Week02/
│
├── README.md
│
├── report/
│   └── W2-PM-FINAL_Report_UTTAM_PARMAR_B084.pdf
│
└── screenshots/
    ├── whois.png
    ├── whatweb.png
    ├── nslookup.png
    ├── curl.png
    ├── wafw00f.png
    ├── dnsrecon.png
    ├── zenmap-scan.png
    └── zenmap-topology.png
```

---

## 📚 Learning Outcomes

Through this practical project, I gained hands-on experience in:

- Domain footprinting and information gathering.
- DNS resolution and enumeration.
- Web technology identification.
- HTTP header analysis.
- WAF detection techniques.
- Network host discovery and port scanning.
- Understanding network topology.
- Identifying potential security risks.
- Documenting technical findings professionally.

---

## ⚖️ Legal & Ethical Disclaimer

All activities documented in this repository were conducted for educational and research purposes within authorized boundaries.

- `networkwalks.com` – Assessed with written permission.
- `10.120.1.0/24` – My own local network.

No unauthorized exploitation or denial-of-service testing was performed. Never scan or test systems without explicit permission from their owner.

---

## 👨‍💻 Author

**Uttam Parmar**

Cybersecurity Professional | Batch B084

Cybersecurity & Ethical Hacking Internship – Networkwalks

**Project:** Week 02 – Footprinting & Network Scanning

**Date:** 14 November 2026

---

⭐ *Learning • Practicing • Securing • Growing in Cybersecurity*

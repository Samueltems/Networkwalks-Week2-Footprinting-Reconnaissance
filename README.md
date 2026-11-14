# Networkwalks Cybersecurity Internship - Week 2

## Footprinting & Network Scanning

**Pentester:** Olawoyin Samuel  
**Batch:** B084  
**Date:** 14 November 2026

---

## Modules Completed

| Module | Description | Status |
|--------|-------------|--------|
| W2-PM1 | Footprinting with Kali Tools (WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, DNSRecon) | ✅ Complete |
| W2-PM2 | GHDB (Google Hacking Database) | ✅ Complete |
| W2-PM4 | theHarvester | ✅ Complete |
| W2-PM5 | Zenmap Network Scanning | ✅ Complete |
| W2-PM3 | Maltego | ❌ Skipped (account setup constraints) |

---

## Key Findings

### Footprinting (W2-PM1)
- **WHOIS:** Domain registered with GoDaddy, hosted on HostGator.
- **WhatWeb:** WordPress 7.1.4, WP Download Manager 3.3.76, Apache server.
- **Nslookup:** Resolved to `192.232.216.135`.
- **Curl:** Exposed WordPress REST API endpoint (`/wp-json/`).
- **Wafw00f:** Site protected by ModSecurity (SpiderLabs).
- **DNSRecon:** Enumerated MX, NS, TXT, and SRV records.

### theHarvester (W2-PM4)
- Ran against `microsoft.com` with Baidu and "all" sources.
- Found **1320 hosts** (all sources) and **11 hosts** (Baidu).
- Many API-key-dependent sources returned errors.

### GHDB (W2-PM2)
- **Task 1:** Found **10 live camera feeds** using Google dorks.
- **Task 2:** Original math PDF dork returned "No matching records found." Alternative dorks also returned no results. Documented as OSINT friction.

### Zenmap (W2-PM5)
- Scanned local subnet with Ping Scan.
- Identified live hosts and saved topology as PDF.

---

## Troubleshooting & Lessons Learned

**1. theHarvester API Key Errors**  
Many sources (Bitbucket, BufferOverun, Censys, Shodan) required API keys. I documented the errors and focused on the sources that worked (Baidu, DuckDuckGo). This taught me that OSINT tools often return partial results in real-world scenarios.

**2. GHDB Dork Obsolescence**  
The math PDF dork from the GHDB returned no results. I attempted alternative dorks but found none. This demonstrated that OSINT dorks age and become obsolete as search engines re-index. A competent footprinting workflow must test variant queries.

**3. VM Networking (Week 1 Carryover)**  
In Week 1, I encountered a `dev eth0` typo in Kali. I diagnosed the syntax error and successfully applied the IP. This troubleshooting mindset carried over to Week 2.

---

## Files in This Repository

- `W2-PM-FINAL_Report.docx` — Full penetration testing report
- `Zenmap_Topology.pdf` — Network topology map
- `GHDB_Tables.docx` — Completed GHDB tables (cameras & math PDFs)
- `screenshots/` — All terminal and tool outputs

---

## Authorization

All activities were performed within the scope of the signed Letter of Authorization (LOA) provided by Networkwalks and against my own local network.

---

**End of README**

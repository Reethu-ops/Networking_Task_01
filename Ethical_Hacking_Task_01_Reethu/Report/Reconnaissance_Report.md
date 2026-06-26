# Ethical Hacking Task 01 – Information Gathering & Reconnaissance

**Student Name:** Reethu

**Course:** BCA Cybersecurity

**Task:** Ethical Hacking Task 01 – Information Gathering & Reconnaissance

**Date:** 26 June 2026

---

# Part A – Target Selection

### Website Name

OpenAI

### Website URL

https://openai.com

### Reason for Choosing the Target

OpenAI was selected because it is a publicly accessible organization whose website provides sufficient publicly available information for passive reconnaissance. The information gathered is collected ethically without interacting with or exploiting the target system.

---

# Part B – WHOIS Lookup

WHOIS information was collected using a public WHOIS lookup service.

| Field             | Details                                                                                                                                            |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| Domain Name       | openai.com                                                                                                                                         |
| Registrar         | MarkMonitor, Inc.                                                                                                                                  |
| Registration Date | 19 January 2007                                                                                                                                    |
| Expiry Date       | 19 January 2029                                                                                                                                    |
| Name Servers      | ns1-02.azure-dns.com, ns2-02.azure-dns.net, ns3-02.azure-dns.org, ns4-02.azure-dns.info                                                            |
| Domain Status     | clientDeleteProhibited, clientTransferProhibited, clientUpdateProhibited, serverDeleteProhibited, serverTransferProhibited, serverUpdateProhibited |

### Observation

The WHOIS lookup identified the domain registration details, registrar information, registration and expiration dates, name servers, and domain status. The domain uses multiple security status codes to prevent unauthorized updates, transfers, and deletion.

**Screenshot:** `WHOIS.png`

---

# Part C – DNS Enumeration

DNS records were identified using a public DNS lookup tool.

| Record     | Status     |
| ---------- | ---------- |
| A Record   | Identified |
| MX Record  | Identified |
| NS Record  | Identified |
| TXT Record | Identified |

### Observation

The DNS lookup provided information about the website's IP addresses, mail exchange servers, authoritative name servers, and TXT records used for verification and security purposes.

**Screenshots:**

* DNS_A.png
* DNS_MX.png
* DNS_NS.png
* DNS_TXT.png

---

# Part D – Website Technology Identification

The technologies used by the target website were identified using an online technology detection tool.

### Technologies Identified

* Web Server: Cloudflare
* CMS: Not Detected
* Programming Language: JavaScript
* JavaScript Framework: Next.js / React
* CDN: Cloudflare

### Summary

The target website uses modern web technologies and Cloudflare services for content delivery, performance optimization, and security. The use of a modern JavaScript framework improves the user experience and application performance.

**Screenshot:** `Website_Technology.png`

---

# Part E – HTTP Security Headers

HTTP security headers were analyzed using an online security header checker.

| Header                           | Present | Purpose                                                                 |
| -------------------------------- | ------- | ----------------------------------------------------------------------- |
| Content-Security-Policy (CSP)    | Yes     | Prevents cross-site scripting attacks.                                  |
| X-Frame-Options                  | Yes     | Protects against clickjacking attacks.                                  |
| X-Content-Type-Options           | Yes     | Prevents MIME type sniffing.                                            |
| Strict-Transport-Security (HSTS) | Yes     | Forces secure HTTPS connections.                                        |
| Referrer-Policy                  | Yes     | Controls the amount of referrer information shared with other websites. |

### Observation

Most important HTTP security headers are implemented, demonstrating that the website follows good security practices to protect users and web resources.

**Screenshot:** `HTTP_Security_Headers.png`

---

# Part F – Robots.txt & Sitemap Analysis

### Robots.txt

The website contains a robots.txt file that provides instructions to search engine crawlers regarding which resources can or cannot be indexed.

### Sitemap.xml

A sitemap is available to assist search engines in discovering and indexing important pages of the website.

### Observation

Both robots.txt and sitemap.xml help improve website indexing while controlling crawler access to specific resources.

**Screenshots:**

* Robots.txt.png
* Sitemap.xml.png

---

# Overall Observations

Passive reconnaissance provides valuable information about a target without directly interacting with its systems. Information such as domain registration details, DNS records, website technologies, HTTP security headers, robots.txt, and sitemap files helps security professionals understand the target's infrastructure before performing any further security assessment. Throughout this task, only publicly available information was collected, ensuring that the reconnaissance process remained ethical and non-intrusive.

---

# Conclusion

This task provided practical experience in the reconnaissance phase of ethical hacking using passive information gathering techniques. Publicly available information such as WHOIS records, DNS records, website technologies, HTTP security headers, robots.txt, and sitemap data was collected and analyzed without interacting directly with the target system. The activity demonstrated how valuable information about a website can be obtained while maintaining ethical and legal boundaries. Reconnaissance is one of the most important stages of penetration testing because it helps security professionals understand the target environment, identify potential technologies in use, and prepare for future security assessments. This exercise improved my understanding of information gathering techniques and highlighted the importance of responsible and ethical cybersecurity practices.

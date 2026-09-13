B082-Week4-Capstone-Project-Mediroza
# 🛡️ Mediroza Hospital — Penetration Testing & Security Assessment

![Skill](https://img.shields.io/badge/Skill-Cybersecurity-red)
![Skill](https://img.shields.io/badge/Skill-Ethical%20Hacking-red)
![Tool](https://img.shields.io/badge/Tool-Networkwalks%20Hash%20Calculator-informational)
![Tool](https://img.shields.io/badge/Tool-Networkwalks%20Password%20Cracker-informational)
![Platform](https://img.shields.io/badge/Platform-Web%20Browser-blue)

## 📌 Project Overview

This project documents a controlled penetration-testing and cybersecurity assessment of the **Mediroza General Hospital** web application.

The assessment focuses on identifying publicly exposed information, discovering application entry points, analysing authentication mechanisms, and evaluating potential security weaknesses in a controlled and authorized testing environment.

> **Authorization Notice:** This project was conducted as part of an authorized cybersecurity and penetration-testing exercise. Testing activities must remain within the approved scope.

---

## 🎯 Project Objectives

The main objectives of this project are to:

- Conduct reconnaissance against the target application.
- Identify publicly exposed information and resources.
- Identify exposed application entry points.
- Analyse authentication mechanisms.
- Examine how the application handles user input.
- Identify potential security vulnerabilities.
- Collect and document evidence of findings.
- Assess the potential impact of identified weaknesses.
- Provide recommendations for improving the application's security.

---

## 🌐 Target

**Target:** Mediroza General Hospital

**Website:** `https://medirozahospital.com`

### Application Areas Identified

- Home page
- About page
- Doctors page
- Contact page
- Patient Portal
- Patient Login
- Staff Login
- Publicly accessible resources
- Other discovered application endpoints

---

# 🔎 Milestone 3 — Reconnaissance

The reconnaissance phase involved gathering information about the target application and identifying publicly exposed resources before conducting further authorized security testing.

### Reconnaissance Activities

The following activities were performed or considered during the assessment:

1. Website enumeration
2. Search-engine reconnaissance
3. Google Dorking
4. Robots.txt analysis
5. Directory and file discovery
6. Login-page identification
7. Application entry-point identification
8. HTTP response analysis
9. Technology identification
10. Documentation of discovered resources

---

# 🕵️ Passive Reconnaissance

Passive reconnaissance involves gathering information from publicly available sources without unnecessarily interacting with the target system.

Activities included:

- Search-engine queries
- Publicly indexed pages
- Public website information
- Robots.txt analysis
- Publicly accessible URLs
- Identification of login portals
- Identification of potentially exposed resources

### Search Engine Reconnaissance

Search engines were used to identify resources associated with the target domain.

Examples of reconnaissance queries include:

```text
site:medirozahospital.com
site:medirozahospital.com login
site:medirozahospital.com inurl:login
site:medirozahospital.com filetype:pdf
site:medirozahospital.com inurl:admin
```

The results were reviewed to determine whether the website exposed information that should not normally be publicly indexed.

---

# 🤖 Robots.txt Analysis

The `robots.txt` file was examined during reconnaissance.

The purpose of this activity was to determine whether the file revealed potentially interesting directories or resources that search engines were instructed not to index.

It is important to note that `robots.txt` is **not a security mechanism**. Disallowing a directory in `robots.txt` does not prevent users from directly accessing the resource.

### Evidence

Relevant screenshots and observations from the robots.txt analysis should be stored in the project's `Screenshots/` directory.

---

# 🔐 Authentication Entry Points

Authentication-related pages were identified during reconnaissance.

The assessment included the identification of:

- Patient login functionality
- Staff login functionality
- Authentication-related URLs
- Login form fields
- Redirect behavior
- Error-message behavior
- Session-related behavior

The purpose was to understand the application's authentication architecture and identify areas that required further authorized security testing.

> Authentication testing should only be performed using accounts and techniques explicitly authorized by the system owner.

---

# 🔍 Web Application Enumeration

Web application enumeration was performed to understand the publicly accessible structure of the target.

Examples of identified resources included:

```text
/
index.html
about.html
doctors.html
contact.html
robots.txt
patient/
patient/login.php
staff/
staff/login.php
```

The discovered endpoints were documented as part of the reconnaissance process.

---

# 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| **Kali Linux** | Cybersecurity testing environment |
| **Nmap** | Network and service discovery |
| **Zenmap** | Graphical interface for Nmap |
| **Google Search** | Passive reconnaissance |
| **Google Dorking** | Discovery of publicly indexed resources |
| **Gobuster** | Directory and resource enumeration |
| **WhatWeb** | Web technology identification |
| **Burp Suite** | Web application analysis |
| **curl** | HTTP request and response testing |
| **Browser Developer Tools** | Web request and response inspection |
| **Linux Terminal** | Command-line security testing |

---

# 🌐 Network and Service Reconnaissance

Network and service reconnaissance can be used during an authorized assessment to determine what services are exposed.

Example Nmap command:

```bash
nmap -sV <authorized-target>
```

For authorized service and script enumeration:

```bash
nmap -sC -sV <authorized-target>
```

### Information of Interest

The assessment may identify:

- Open ports
- Running services
- Service versions
- Web servers
- HTTP/HTTPS services
- TLS/SSL configuration
- Potentially outdated services
- Other externally accessible services

All discovered services should be recorded and compared against the approved testing scope.

---

# 🧪 Web Application Security Assessment

The web application was reviewed for common security weaknesses.

## Authentication

Areas examined included:

- Login functionality
- Authentication controls
- Login response behavior
- Session management
- Error handling
- Account-enumeration indicators

## Input Validation

Application input areas were reviewed for:

- Form inputs
- URL parameters
- HTTP parameters
- Server-side validation
- Client-side validation
- Improper input handling

## Access Control

The assessment considered whether access controls were correctly implemented for:

- Restricted pages
- Staff functionality
- Patient functionality
- Administrative functionality
- Protected resources

## Information Disclosure

The assessment looked for potentially exposed:

- Configuration information
- Debug information
- Server information
- Directory listings
- Backup files
- Sensitive documents
- Internal application information

---

# 📸 Evidence Collection

Screenshots and other evidence should be collected throughout the assessment.

### Recommended Screenshot Naming

```text
01-target-homepage.png
02-robots-txt.png
03-patient-login.png
04-staff-login.png
05-google-dorking-results.png
06-reconnaissance-results.png
07-nmap-results.png
08-directory-enumeration.png
09-technology-identification.png
10-security-finding.png
```

Evidence should clearly demonstrate the observation or finding without unnecessarily exposing confidential information.

---

# 📊 Findings Documentation

Each security finding should be documented using a consistent structure.

### Finding Template

**Finding:**  
Brief description of the identified issue.

**Severity:**  
Low / Medium / High / Critical

**Affected Resource:**  
URL, endpoint, page, service, or application component.

**Description:**  
Detailed explanation of the issue.

**Evidence:**  
Screenshot, command output, HTTP response, or other supporting evidence.

**Security Impact:**  
Explanation of the potential security consequences.

**Recommendation:**  
Recommended remediation steps.

---

# ⚠️ Risk Classification

Security findings can be categorized according to their potential impact.

| Severity | Description |
|---|---|
| **Critical** | Vulnerability could result in severe compromise of the system or sensitive information. |
| **High** | Vulnerability could significantly affect confidentiality, integrity, or availability. |
| **Medium** | Vulnerability presents a meaningful security risk but may require additional conditions to exploit. |
| **Low** | Vulnerability has limited security impact or requires significant conditions to become exploitable. |
| **Informational** | Observation that does not represent a direct vulnerability but may improve security posture. |

---

# 📁 Repository Structure

```text
Mediroza-Penetration-Testing/
│
├── README.md
│
├── Reconnaissance/
│   ├── robots.txt
│   ├── discovered-endpoints.txt
│   └── search-results/
│
├── Scanning/
│   ├── nmap-results/
│   └── zenmap-results/
│
├── Screenshots/
│   ├── 01-target-homepage.png
│   ├── 02-robots-txt.png
│   ├── 03-patient-login.png
│   ├── 04-staff-login.png
│   ├── 05-google-dorking-results.png
│   └── 06-nmap-results.png
│
├── Evidence/
│   └── findings.md
│
└── Reports/
    └── Penetration-Testing-Report.pdf
```

---

# 🔄 Assessment Methodology

The assessment followed a structured penetration-testing workflow:

```text
                    ┌─────────────────────┐
                    │   Reconnaissance    │
                    └──────────┬──────────┘
                               ↓
                    ┌─────────────────────┐
                    │ Information         │
                    │ Gathering           │
                    └──────────┬──────────┘
                               ↓
                    ┌─────────────────────┐
                    │ Entry-Point         │
                    │ Identification      │
                    └──────────┬──────────┘
                               ↓
                    ┌─────────────────────┐
                    │ Network / Service   │
                    │ Enumeration         │
                    └──────────┬──────────┘
                               ↓
                    ┌─────────────────────┐
                    │ Web Application     │
                    │ Analysis            │
                    └──────────┬──────────┘
                               ↓
                    ┌─────────────────────┐
                    │ Vulnerability       │
                    │ Identification      │
                    └──────────┬──────────┘
                               ↓
                    ┌─────────────────────┐
                    │ Evidence Collection │
                    └──────────┬──────────┘
                               ↓
                    ┌─────────────────────┐
                    │ Risk Assessment     │
                    └──────────┬──────────┘
                               ↓
                    ┌─────────────────────┐
                    │ Recommendations     │
                    └──────────┬──────────┘
                               ↓
                    ┌─────────────────────┐
                    │ Final Report        │
                    └─────────────────────┘
```

---

# 📚 Skills Demonstrated

This project demonstrates practical skills in:

- Cybersecurity reconnaissance
- Ethical hacking methodology
- Web application security
- Network scanning
- Service enumeration
- Search-engine reconnaissance
- Google Dorking
- Authentication analysis
- Web application enumeration
- Vulnerability identification
- Evidence collection
- Risk assessment
- Security documentation
- Security recommendations
- Penetration-testing reporting

---

# 📝 Project Deliverables

The project deliverables include:

- Reconnaissance documentation
- Identified application entry points
- Network/service scan results
- Web application observations
- Screenshots and supporting evidence
- Security findings
- Risk assessment
- Recommended security improvements
- Final penetration-testing report

---

# ⚖️ Responsible Testing

This project is intended strictly for **authorized cybersecurity testing and educational purposes**.

The following principles must be followed:

- Do not test systems without explicit authorization.
- Do not access confidential information unnecessarily.
- Do not modify or delete production data.
- Do not disrupt services.
- Do not attempt to compromise accounts outside the approved scope.
- Do not download or distribute confidential information.
- Protect collected evidence.
- Report vulnerabilities responsibly.
- Remain within the defined rules of engagement.

---

# 👤 Author

**Name:** Kemar Goulbourne  
**Program:** Cybersecurity  
**Batch:** B082  
**Week:** 4 — Capstone Project  
**Institution:** University of the Commonwealth Caribbean (UCC)

---

# 📜 Disclaimer

This repository is intended for **authorized cybersecurity testing, academic research, and educational purposes only**.

The techniques, tools, commands, and information documented in this repository must only be used against systems for which the tester has explicit permission to conduct security testing.

The author is not responsible for unauthorized use of the information contained within this repository.

---

## ⭐ Project Status

**Status:** Completed / In Progress  
**Project Type:** Penetration Testing & Security Assessment  
**Assessment Phase:** Reconnaissance, Enumeration & Web Application Security Testing

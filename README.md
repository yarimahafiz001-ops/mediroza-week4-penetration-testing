# mediroza-week4-penetration-testing
A Week 4 cybersecurity project documenting DNS reconnaissance, web enumeration, information disclosure analysis, and PDF encryption assessment using Kali Linux.
Mediroza General Hospital — Week 4 Penetration Testing Project
Author: HAMZA AHMAD
Project: Mediroza Week 4 — Penetration Testing
Environment: Kali Linux on Oracle VirtualBox
Focus Areas: Reconnaissance, DNS Analysis, Web Enumeration, and PDF Encryption Analysis
Status: In Progress
📌 Project Overview
This project documents a controlled cybersecurity assessment of the Mediroza General Hospital website as part of a Week 4 penetration-testing exercise.
The project focuses on collecting publicly accessible technical information, identifying potential information-disclosure risks, documenting findings, and preparing evidence for security analysis.
All testing should be conducted only within the scope authorized by the instructor or system owner.
🎯 Project Objectives
Perform DNS reconnaissance on the target domain.
Identify basic website technologies and server responses.
Retrieve and analyze the website's robots.txt file.
Document publicly disclosed application paths.
Prepare tools for PDF encryption analysis.
Maintain organized evidence and technical notes.
Develop recommendations to improve website security.
🛠️ Tools and Technologies
Tool
Purpose
Kali Linux
Cybersecurity testing environment
Oracle VirtualBox
Virtual machine platform
nslookup
DNS resolution and domain information
WhatWeb
Website technology identification
curl
Retrieving HTTP responses and website resources
qpdf
PDF structure and encryption inspection
pdfinfo
PDF metadata and encryption-status inspection
ExifTool
File metadata analysis
Linux Terminal
Executing commands and documenting results
📂 Project Structure
The following directory structure organizes the project evidence and documentation.
Mediroza-WK4/
│
├── M1/
│   ├── dns-results.txt
│   ├── robots.txt
│   └── notes.txt
│
├── M2/
│   ├── evidence/
│   └── notes.txt
🔍 Milestone 1: DNS Reconnaissance and Web Enumeration
1. DNS Lookup
Command executed:
nslookup medirozahospital.com
Observed result:
DNS server: 192.168.43.1
Resolved IPv4 address: 199.188.201.16
Security relevance:
DNS reconnaissance identifies the IP address associated with a domain. This information provides a starting point for authorized security assessments.
2. Website Technology Identification
Command executed:
whatweb https://medirozahospital.com
Observed result:
The captured output included an HTTP 403 Forbidden response in one attempt and an HTTP 200 OK response in another, along with technology-identification information.
Security relevance:
HTTP responses can help identify how a web server handles requests. A 403 response does not, by itself, prove that a vulnerability exists.
3. Robots.txt Analysis
Command executed:
curl -sS https://medirozahospital.com/robots.txt
The retrieved file contained:
User-agent: *
Disallow: /patient/
Disallow: /staff/
Disallow: /old/

Sitemap: https://medirozahospital.com/sitemap.xml
Finding:
The robots.txt file identifies application paths that website crawlers are instructed not to access.
Security significance:
The file may disclose application path names. However, the presence of a path in robots.txt does not establish that the path is accessible or vulnerable.
Recommendation:
Sensitive application resources should be protected through appropriate authentication and server-side access controls rather than relying on robots.txt.
🔐 Milestone 2: PDF Encryption Analysis
Objective
Examine the encryption status and relevant metadata of three instructor-provided exercise PDF files.
Required Files
patient_report_1.pdf
patient_report_2.pdf
patient_report_3.pdf
Tools Prepared
QPDF
pdfinfo
ExifTool
Current Status
The project workspace and notes have been created, and the required tools have been prepared.
However, the three exercise PDF files have not yet been located. Consequently, their encryption status has not been verified.
Planned Analysis
Once the authorized exercise files are available:
Identify the three PDF files.
Inspect each file's metadata.
Determine whether PDF encryption is enabled.
Record the observed results.
Save relevant evidence in the M2/evidence/ directory.
Document findings and recommendations.
Important: No encryption results are claimed until the actual exercise files have been examined.
📊 Preliminary Findings
ID
Observation
Status
F-01
Domain resolved to an IPv4 address during DNS reconnaissance.
Observed
F-02
Website technology identification returned different HTTP responses across attempts.
Observed
F-03
The robots.txt file disclosed several application path names.
Observed
F-04
PDF encryption status requires examination of the instructor-provided files.
Pending
These observations are preliminary and do not independently establish exploitable vulnerabilities.
🛡️ Security Recommendations
Enforce access controls: Protect sensitive application routes with server-side authentication and authorization.
Review information disclosure: Avoid unnecessarily exposing sensitive internal paths through public resources.
Monitor HTTP responses: Investigate unexpected server responses and ensure error handling does not reveal sensitive information.
Protect PDF documents: Apply appropriate document permissions and encryption where required by the sensitivity of the information.
Maintain evidence: Store assessment notes, command outputs, and screenshots in an organized evidence directory.
Document limitations: Clearly distinguish verified findings from planned or incomplete tests.
📚 Skills Demonstrated
This project demonstrates practical experience with:
Linux command-line operations.
DNS reconnaissance.
Website technology identification.
HTTP response interpretation.
Web information-disclosure analysis.
Security evidence collection.
PDF metadata and encryption analysis preparation.
Technical documentation and reporting.
⚖️ Ethical and Legal Disclaimer
This project is intended for authorized educational cybersecurity testing.
All activities must remain within the scope approved by the instructor or system owner. Publicly accessible information should not be treated as permission to access restricted resources, test authentication controls, or conduct intrusive security testing.
No unauthorized access to hospital systems or patient information is intended.
👨‍💻 Author
HAMZA AHMAD
Computer Science / Cybersecurity Graduate
Aspiring Cybersecurity Professional

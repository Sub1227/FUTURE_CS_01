# FUTURE_CS_01

## Future Interns Cyber Security Internship – Task 1
### Vulnerability Assessment Report for a Live Website

## Project Overview

This repository contains my work for Task 1 of the Future Interns Cyber Security Internship.

The objective was to perform a read-only vulnerability assessment of public-facing test websites and document security configuration weaknesses in a professional vulnerability assessment report.

## Websites Tested

### Nmap Assessment
- Target: `testphp.vulnweb.com`
- Purpose: Basic service and port exposure assessment

### OWASP ZAP & Browser DevTools Assessment
- Target: `testasp.vulnweb.com`
- Purpose: Passive analysis of HTTP security headers, cookies, and technology disclosure

## Scope and Ethics

The assessment was conducted only on intentionally vulnerable public test websites.

The testing was limited to:
- Passive security analysis
- Basic Nmap service/port discovery
- HTTP response header inspection
- Cookie security attribute review
- Browser Developer Tools inspection

The following activities were not performed:
- Exploitation
- Login bypass
- Brute force
- Denial-of-Service testing
- Active vulnerability scanning
- Destructive or harmful activities

## Tools Used

- Nmap
- OWASP ZAP 2.17.0
- Microsoft Edge Developer Tools
- Canva
- GitHub

## Key Findings

The passive assessment identified several low-risk security configuration and information-disclosure issues, including:

- Cookie missing the HttpOnly attribute
- Cookie missing the SameSite attribute
- `X-Powered-By: ASP.NET` technology disclosure
- `Server: Microsoft-IIS/8.5` information disclosure
- Missing security headers such as X-Content-Type-Options and Strict-Transport-Security

No exploitation was performed.

## Risk Classification

| Finding | Risk |
|---|---|
| Cookie Missing HttpOnly Flag | Low |
| Cookie Missing SameSite Attribute | Low |
| X-Powered-By Header Disclosure | Low |
| Server Version Disclosure | Low |
| Missing Security Headers | Low |

## Repository Contents

- `Vulnerability_Assessment_Report.pdf` – Final vulnerability assessment report
- `evidence/` – Nmap output and assessment evidence
- `screenshots/` – Supporting ZAP and Browser DevTools screenshots
- `README.md` – Project documentation

## Remediation

Recommended actions include:

1. Enable the HttpOnly attribute for session cookies.
2. Configure an appropriate SameSite cookie policy.
3. Remove or suppress unnecessary technology disclosure headers.
4. Minimize server version information in HTTP responses.
5. Configure appropriate security headers, including HSTS and X-Content-Type-Options.

## Conclusion

The assessment identified primarily low-risk configuration and information-disclosure issues. The findings and recommended remediation steps are documented in the accompanying Vulnerability Assessment Report.

This assessment was conducted for educational and internship purposes using permitted public test environments.

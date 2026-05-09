# Security Audit – yrpreyPHP | OWASP Top 10 (2021)

>  This is an educational pentesting lab. All testing was performed
> on an intentionally vulnerable application in an isolated VM environment.
## Environment
- Attacker: Kali Linux (VMware)
- Target: Windows 10 + XAMPP running yrpreyPHP
- Tools: sqlmap, Burp Suite, Hydra, OWASP ZAP

## Vulnerabilities Found

| Vulnerability | OWASP 2021 | Severity | Status |
|---|---|---|---|
| SQL Injection | A03 | 🔴 Critical | Exploited |
| XSS (Reflected + Stored) | A03 | 🟠 High | Exploited |
| CSRF | A01 | 🟡 Medium | Confirmed |
| Broken Authentication | A07 | 🔴 Critical | Exploited |

## Phases
1. **SQL Injection** – sqlmap enumerated 6 DBs, dumped users table
2. **XSS** – Reflected via search.php, Stored via Guestbook
3. **CSRF** – No token in POST requests (confirmed via Burp Suite)
4. **Broken Auth** – Hydra brute-forced login with rockyou.txt

## Files
- `Rapport_Audit_Securite_yrpreyPHP_OWASP2021.pdf` – Full audit report (FR)
- `2026-04-21-ZAP-Report-.html` – OWASP ZAP automated scan results

## Author
Rawen ZGARNI

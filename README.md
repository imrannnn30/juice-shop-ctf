# Juice Shop CTF — 17 Web Security Challenges

> Penetration testing write-ups on OWASP Juice Shop — exploiting and documenting 17 vulnerabilities across 8 OWASP Top 10 categories.

[![OWASP](https://img.shields.io/badge/OWASP-Juice%20Shop-000000?style=flat)](https://owasp.org/www-project-juice-shop/)
[![Burp Suite](https://img.shields.io/badge/Tool-Burp%20Suite-FF6633?style=flat)](https://portswigger.net/burp)

## What it is

A self-directed cybersecurity project where I attacked **OWASP Juice Shop** — a deliberately vulnerable web application — and produced a write-up for each challenge: methodology, techniques used, tools, payloads. The set covers 8 categories of the OWASP Top 10 across 17 challenges of difficulty 3 and 4.

## Challenges solved (17)

### Broken Access Control (5)
- Forged Feedback · Forged Review · Manipulate Basket · Product Tampering · Easter Egg

### Broken Anti-Automation (1)
- CAPTCHA Bypass

### Broken Authentication (1)
- Bjoern's Favorite Pet

### Cryptographic Issues (1)
- Nested Easter Egg

### Improper Input Validation (3)
- Admin Registration · Expired Coupon · Poison Null Byte

### Injection (2)
- Login Bender · Login Jim (SQL injection via login)

### Security Through Obscurity (1)
- Privacy Policy Inspection

### Sensitive Data Exposure (3)
- Forgotten Developer Backup · Forgotten Sales Backup · Misplaced Signature File

## Sample methodology — *Forged Feedback*

> Each challenge follows the same write-up template :  
> **Step-by-step execution**, **techniques used**, **tools needed**.

1. Open Burp Suite, navigate to the proxy tab, and load the target page
2. Go to the `/contact` page of the Juice Shop instance
3. Activate the interceptor
4. Capture the GET request, tamper it into a POST request, and modify the `email` field to forge feedback under another user's identity

**Techniques used** : HTTP request tampering · parameter manipulation · unauthorized action execution · access control bypass

**Tool** : Burp Suite

## Tools & techniques covered

| Tool          | Purpose                              |
| ------------- | ------------------------------------ |
| **Burp Suite**| Proxy interception, request tampering|
| **DevTools**  | Source inspection, hidden fields      |
| Browser cookies | Session manipulation               |
| Manual SQL    | Login-based injection payloads        |

## What I learned

- **OWASP Top 10 in practice** — not just the names, but how to exploit each category by hand
- **Web request tampering** with Burp Suite — proxy setup, intercept, modify, replay
- **SQL injection on auth forms** — bypassing login with `' OR 1=1--` and variants
- **Looking where you're not supposed to** — hidden files, leaked backups, signature files left in `.git/`
- **Writing security write-ups** — clear methodology, reproducible steps, the kind of document a security team actually reads

## Project context

- **Year** : 2025–2026
- **School** : Epitech Bachelor, Mulhouse
- **Team** : solo (self-directed CTF)
- **Course** : Cybersecurity (B-SEC-100)

## Note

This is a portfolio summary. The full write-ups (17 markdown files with payloads, screenshots, and detailed steps) are private per Epitech academic policy. Available on request for recruiters or security teams.

---

[Imran Nogueira](https://github.com/imrannnn30)

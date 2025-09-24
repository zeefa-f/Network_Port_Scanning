# Phishing Indicators Report

**Sample Email Subject:** Urgent: Verify your Amazon account now!

---

## Indicators Identified

1. **Spoofed Sender Address**  
   The email is sent from `support@amazon-security-update.com` instead of the legitimate `@amazon.com`.

2. **Header Authentication Failures**  
   SPF and DMARC checks failed; the IP used is not authorized to send mail for Amazon.

3. **Suspicious Link**  
   Display text shows `https://www.amazon.com/verify` but the actual URL redirects to `http://secure-login.amazon-update-security.com/login`.

4. **Suspicious Attachment**  
   File attached (`invoice.docm`) is risky because `.docm` files can contain malicious macros.

5. **Urgency/Threats**  
   The email threatens suspension of the account within 12 hours to pressure quick action.

6. **Mismatched URL**  
   Visible link and actual link do not match, indicating possible redirection to a phishing site.

7. **Language Issues**  
   The wording is slightly unnatural compared to genuine Amazon communication.

---

## Conclusion
The email displays multiple clear phishing indicators (spoofed domain, header failures, suspicious links/attachments, urgency, and unusual language). It should be treated as malicious and unsafe.

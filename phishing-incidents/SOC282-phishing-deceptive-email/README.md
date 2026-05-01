# 🚨 Incident Report: Phishing Email Detected (SOC282)

## 📌 Summary
A medium severity alert was triggered indicating a phishing email containing a malicious attachment.

## 📌 Resumo (Português)
Um alerta de severidade média foi gerado indicando um e-mail de phishing contendo um anexo malicioso.

---

## 🧾 Alert Details
- **Incident ID:** SOC282  
- **Category:** Phishing  
- **Severity:** Medium  
- **Recipient:** Felix  
- **Sender:** free@coffeeshoop.com  
- **SMTP IP:** 103.80.134.63  
- **Subject:** Free Coffee Voucher  

---

## 🔍 Investigation

The investigation started by analyzing the email metadata and content.

Key observations:
- Suspicious sender domain (possible spoofing)  
- Email subject designed to attract attention (social engineering)  
- Presence of a compressed attachment: `free-coffee.zip`  

The email was successfully delivered to the user, indicating that it bypassed email security controls.

The attachment was analyzed and identified as malicious. It contained an executable file that could compromise the system.

Further log analysis confirmed that the file was executed on the user's machine.

Additionally, network activity revealed communication with an external command-and-control (C2) server:

- **C2 IP:** 37.120.233.226  

This behavior strongly indicates post-exploitation activity and system compromise.

---

## 🚨 Findings

- Phishing email successfully delivered  
- Malicious attachment executed  
- Connection established with external C2 server  
- High likelihood of system compromise  

---

## 🔗 Indicators of Compromise (IOCs)

- SMTP IP: 103.80.134.63  
- Suspicious domain: coffeeshoop.com  
- Malicious file: free-coffee.zip  
- C2 IP: 37.120.233.226  

---

## 🧠 MITRE ATT&CK Mapping

- **T1566** – Phishing  
- **T1204** – User Execution  

---

## 🛠️ Tools Used

- SIEM (Let's Defend platform)  
- Email analysis  
- Log analysis  

---

## ✅ Conclusion

The alert represents a confirmed phishing attack (True Positive).

The execution of the malicious attachment and communication with a C2 server indicate a successful compromise of the host.

Immediate containment actions should be taken to isolate the affected system and prevent further damage.

---

## 📚 Lessons Learned

- Avoid opening attachments from unknown senders  
- Verify sender legitimacy before interacting with emails  
- Monitor outbound connections for suspicious activity 

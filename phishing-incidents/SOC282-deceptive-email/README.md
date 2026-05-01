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
- Presence of an attachment: `free-coffee.zip`

The SMTP IP address was analyzed and showed signs of malicious activity.

The attachment was further inspected and identified as malicious. It contained an executable file that could compromise the system.

Log analysis confirmed that the file was executed on the user's machine.

Additionally, network logs revealed communication with an external IP address:

- **C2 IP:** 37.120.233.226  

This indicates that the system was likely compromised.

---

## 🚨 Findings

- Phishing email successfully delivered  
- Malicious attachment executed  
- Connection established with external C2 server  
- Potential system compromise  

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

The malicious attachment was executed, and communication with a C2 server was observed, indicating a successful compromise.

Immediate containment actions are required.

---

## 📚 Lessons Learned

- Avoid opening unknown attachments  
- Verify sender legitimacy  
- Monitor outbound connections for suspicious activity  

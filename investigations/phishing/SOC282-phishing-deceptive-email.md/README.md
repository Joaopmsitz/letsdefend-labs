# 🚨 SOC282 - Phishing Email Detected

## 📌 Summary

A medium-severity alert was triggered indicating a phishing email containing a malicious attachment designed for payload delivery.

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

The investigation focused on email metadata, attachment analysis, and endpoint activity.

### Key Findings:

- Suspicious sender domain indicating possible spoofing  
- Social engineering technique using “free voucher” lure  
- Malicious attachment: `free-coffee.zip`  
- Attachment contained executable payload  
- Execution confirmed on the target machine  
- Outbound communication detected after execution  

---

## 🌐 Network Activity

- C2 IP: 37.120.233.226  

This indicates post-exploitation communication with an external command-and-control server.

---

## 🚨 Impact

- Successful phishing delivery  
- Malicious payload executed  
- Host compromise likely  
- External C2 communication established  

---

## 🔗 Indicators of Compromise (IOCs)

- SMTP IP: 103.80.134.63  
- Domain: coffeeshoop.com  
- File: free-coffee.zip  
- C2 IP: 37.120.233.226  

---

## 🧠 MITRE ATT&CK Mapping

- T1566 – Phishing  
- T1204 – User Execution  
- T1105 – Ingress Tool Transfer  
- T1071 – Application Layer Protocol  

---

## 🛠️ Response Actions

- Incident classified as True Positive  
- Affected host should be isolated (if not already contained)  
- Network indicators should be blocked  
- Further forensic analysis recommended  

---

## 📚 Conclusion

This incident represents a successful phishing attack resulting in malware execution and suspected system compromise via C2 communication.

---

⭐ SOC investigation completed following detection → analysis → impact assessment → response workflow.

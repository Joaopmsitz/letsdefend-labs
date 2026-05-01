# 🚨 Incident Report: Javascript Code Detected in URL (SOC166)

## 📌 Summary
A medium severity alert was triggered indicating suspicious JavaScript code embedded in a URL, suggesting a potential cross-site scripting (XSS) attempt.

## 📌 Resumo (Português)
Um alerta de severidade média foi gerado indicando código JavaScript suspeito em uma URL, sugerindo uma possível tentativa de ataque XSS.

---

## 🧾 Alert Details
- **Incident ID:** SOC166  
- **Category:** Web Attack  
- **Severity:** Medium  

---

## 🔍 Investigation

The investigation began by analyzing the HTTP request associated with the alert.

A suspicious URL was identified containing encoded JavaScript code.

This type of behavior is commonly associated with cross-site scripting (XSS) attacks, where attackers attempt to inject malicious scripts into web applications.

The payload appeared to include JavaScript functions intended to execute in the victim's browser.

Further analysis suggested that the attack was targeting a web application's input field, aiming to execute client-side code.

No evidence of successful script execution or abnormal responses was observed during log analysis.

---

## 🚨 Findings

- Suspicious JavaScript code detected in URL  
- Possible XSS attack attempt  
- No evidence of successful exploitation  

---

## 🔗 Indicators of Compromise (IOCs)

- Suspicious pattern: JavaScript code embedded in URL  
- Technique: Cross-Site Scripting (XSS)  
- Target: Web application input field  

---

## 🧠 MITRE ATT&CK Mapping

- **T1059.007** – JavaScript  
- **T1189** – Drive-by Compromise  

---

## 🛠️ Tools Used

- SIEM (Let's Defend platform)  
- Log analysis  

---

## ✅ Conclusion

The alert represents a potential XSS attack attempt.

Although malicious JavaScript code was identified in the request, no evidence of successful execution was observed.

The attack was unsuccessful.

---

## 📚 Lessons Learned

- Validate and sanitize user inputs  
- Detect encoded or obfuscated scripts in URLs  
- Monitor web traffic for client-side attack patterns  

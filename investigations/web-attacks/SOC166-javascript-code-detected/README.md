# 🚨 SOC166 - JavaScript Code Detected in URL

## 📌 Summary

A medium-severity alert was triggered indicating suspicious JavaScript code embedded in a URL, suggesting a potential Cross-Site Scripting (XSS) attempt.

---

## 🧾 Alert Details

- **Incident ID:** SOC166  
- **Category:** Web Attack  
- **Severity:** Medium  
- **Attack Type:** Cross-Site Scripting (XSS)  

---

## 🔍 Detection & Analysis

The investigation began with analysis of an HTTP request containing a suspicious encoded payload in the URL.

A JavaScript-based payload was identified, similar to:
**<script>alert(1)</script>**


### Observations:

- Encoded JavaScript detected in URL  
- Attempt to inject client-side script  
- Targeted web application input field  
- No evidence of sanitization on input observed  

---

## 🚨 Findings

- Suspicious JavaScript payload detected  
- Possible XSS attack attempt  
- No evidence of successful execution  
- No abnormal response behavior observed  

---

## 🔗 Indicators of Compromise (IOCs)

- Payload: Encoded JavaScript in URL  
- Technique: Cross-Site Scripting (XSS)  
- Target: Web application input field  

---

## 🧠 MITRE ATT&CK Mapping

- T1059.007 – JavaScript Execution  
- T1059 – Command and Scripting Interpreter  

---

## 🛠️ Response

- Attack classified as True Positive attempt  
- No successful exploitation confirmed  
- Input validation recommended  

---

## 📚 Conclusion

This incident represents a potential XSS attack attempt through JavaScript injection in a URL. The attack was detected and did not result in successful execution.

---

⭐ SOC investigation completed following detection → analysis → validation → response workflow.

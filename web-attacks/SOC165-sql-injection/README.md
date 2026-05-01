# 🚨 Incident Report: SQL Injection Attempt (SOC165)

## 📌 Summary
A high severity alert was triggered indicating a possible SQL Injection attempt targeting a web application.

## 📌 Resumo (Português)
Um alerta de alta severidade foi gerado indicando uma possível tentativa de SQL Injection em uma aplicação web.

---

## 🧾 Alert Details
- **Incident ID:** SOC165  
- **Category:** Web Attack  
- **Severity:** High  

---

## 🔍 Investigation

The investigation began by analyzing the HTTP request logs associated with the alert.

A suspicious payload was identified in the request:

```
' OR 1=1 --
```

This payload is commonly used to manipulate SQL queries and bypass authentication mechanisms.

The attacker attempted to bypass authentication by injecting malicious SQL code into a web application's input field.

Further analysis indicated that the request was targeting a web application's login endpoint.

Multiple requests with similar payloads were observed, suggesting repeated or automated attack attempts.

---

## 🚨 Findings

- SQL Injection payload detected  
- Attempt to bypass authentication  
- Repeated malicious requests observed  

---

## 🔗 Indicators of Compromise (IOCs)

- Suspicious payload: ' OR 1=1 --  
- Technique: SQL Injection (Authentication Bypass)  
- Target: Web application login endpoint  

---

## 🧠 MITRE ATT&CK Mapping

- **T1190** – Exploit Public-Facing Application  

---

## 🛠️ Tools Used

- SIEM (Let's Defend platform)  
- Log analysis  

---

## ✅ Conclusion

The alert represents a confirmed SQL Injection attempt.

No changes in HTTP response status were observed, indicating that the attack was unsuccessful.

---

## 📚 Lessons Learned

- Importance of input validation  
- Monitoring repeated malicious requests  
- Detecting SQL patterns in web logs  

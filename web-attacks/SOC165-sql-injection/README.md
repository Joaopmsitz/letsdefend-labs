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

The investigation began by reviewing the alert details and associated HTTP request logs.

Key information analyzed:
- Source IP address  
- Requested URL  
- HTTP response status  

A suspicious payload was identified in the request URL. The payload contained common SQL Injection patterns such as:

```
' OR 1=1 --
```

This type of payload is typically used to bypass authentication mechanisms.

The repeated requests from the same source IP indicated multiple attack attempts.

---

## 🚨 Findings

- Malicious SQL payload detected  
- Multiple request attempts observed  
- Attempt to bypass authentication  

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

After analyzing the HTTP response status, no evidence of successful exploitation was found.  
The attack was unsuccessful.

---

## 📚 Lessons Learned

- Importance of input validation  
- Monitoring repeated requests from same IP  
- Detecting SQL patterns in web logs  

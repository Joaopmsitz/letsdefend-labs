# 🚨 SOC165 - SQL Injection Attempt Detected

## 📌 Summary

A high-severity alert was triggered indicating a potential SQL Injection attempt targeting a web application authentication endpoint.

---

## 🧾 Alert Details

- **Incident ID:** SOC165  
- **Category:** Web Attack  
- **Severity:** High  
- **Attack Type:** SQL Injection  

---

## 🔍 Detection & Analysis

The investigation started with the analysis of HTTP request logs from the affected endpoint.

A malicious payload was identified:
**' OR 1=1 --**

### Observations:

- Payload is commonly used for authentication bypass  
- Targeted login endpoint of a web application  
- Multiple repeated requests detected (possible automation)  
- Injection attempts aimed at manipulating SQL query logic  

---

## 🚨 Findings

- SQL Injection attempt confirmed  
- Authentication bypass technique identified  
- Repeated malicious requests observed  
- No successful exploitation confirmed  

---

## 🔗 Indicators of Compromise (IOCs)

- Payload: `' OR 1=1 --`  
- Technique: SQL Injection (Authentication Bypass)  
- Target Endpoint: Web application login page  

---

## 🧠 MITRE ATT&CK Mapping

- T1190 – Exploit Public-Facing Application  

---

## 🛠️ Response

- Attack classified as True Positive  
- No evidence of successful compromise  
- Monitoring of endpoint recommended  
- Input validation improvements suggested  

---

## 📚 Conclusion

This incident represents a confirmed SQL Injection attempt against a public-facing application. The attack was detected and did not result in successful exploitation.

---

⭐ SOC analysis completed following detection → investigation → validation → response workflow.

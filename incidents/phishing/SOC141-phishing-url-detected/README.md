# 🚨 SOC141 - Phishing URL Detected

## 📌 Summary

A security alert was triggered after an internal user accessed a suspicious URL identified as a phishing domain. The investigation focused on validating the malicious URL, analyzing network activity, and checking endpoint behavior.

## 🧾 Alert Details

    Incident ID: SOC141
    Category: Phishing
    Severity: Security Analyst
    Event ID: 86
    User: ellie
    Hostname: EmilyComp
    Source IP: 172.16.17.49
    Destination IP: 91.189.114.8
    Destination Domain: mogagrocol.ru
    URL: http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io

## 🔍 Investigation

The investigation focused on proxy logs, threat intelligence analysis, and endpoint activity.

Key Findings:

    Suspicious phishing URL accessed by internal endpoint
    Domain reputation analysis showed malicious indicators
    Proxy logs confirmed communication with the suspicious domain
    User interaction with the phishing URL was confirmed
    Endpoint investigation identified suspicious rundll32.exe execution activity

## 🌐 Network Activity

    Protocol: HTTP
    Destination Port: 80
    Destination IP: 91.189.114.8

The endpoint established communication with a known suspicious phishing domain.

## 🚨 Impact

    Successful phishing URL access
    Possible malicious execution on the endpoint
    Potential host compromise requiring further investigation

## 🔗 Indicators of Compromise (IOCs)

    Domain: mogagrocol.ru
    IP Address: 91.189.114.8
    URL: http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php

## 🧠 MITRE ATT&CK Mapping

    T1566 – Phishing
    T1204 – User Execution
    T1059 – Command and Scripting Interpreter

## 🛠️ Response Actions

    Incident classified as True Positive
    Affected endpoint should be contained
    Malicious indicators should be blocked
    Additional endpoint forensic analysis recommended

## 📚 Conclusion

This incident represents a phishing attack where a user accessed a malicious URL. The investigation confirmed communication with the phishing domain and identified suspicious endpoint activity, requiring containment and additional analysis.

⭐ SOC investigation completed following detection → analysis → impact assessment → response workflow.

# 🛡️ SOC Analyst Playbook  
A practical, real‑world playbook for SOC Analysts focusing on incident response, SIEM queries, log analysis, detection engineering, and security operations best practices.

---

## 📌 Purpose  
This playbook is designed to help SOC analysts quickly reference:
- Incident response procedures  
- Detection and triage workflows  
- SIEM queries (Splunk, Elastic, QRadar)  
- Log analysis techniques  
- Threat hunting methodologies  
- MITRE ATT&CK mappings  

---

## 📁 Repository Structure  
```
SOC-Analyst-Playbook/
│
├── Incident-Response/
│   ├── IR-Checklist.md
│   ├── Triage-Guide.md
│   ├── Containment-Steps.md
│   └── Evidence-Collection.md
│
├── SIEM-Queries/
│   ├── Splunk/
│   │   ├── Authentication-Queries.md
│   │   ├── Network-Queries.md
│   │   └── Malware-Queries.md
│   ├── Elastic/
│   └── QRadar/
│
├── Log-Analysis/
│   ├── Windows-Logs.md
│   ├── Linux-Logs.md
│   ├── Firewall-Logs.md
│   └── Proxy-Logs.md
│
├── Threat-Hunting/
│   ├── Hunt-Methodology.md
│   ├── ATTACK-Mapping.md
│   └── Hunt-Queries.md
│
└── Playbooks/
    ├── Phishing.md
    ├── Malware-Infection.md
    ├── Brute-Force.md
    └── Suspicious-Login.md
```

---

## 🚨 Incident Response Templates  
### **IR Checklist**
- Identify alert source  
- Validate alert  
- Determine severity  
- Collect logs & evidence  
- Contain the threat  
- Eradicate malicious artifacts  
- Recover systems  
- Document findings  
- Submit lessons learned  

### **Triage Questions**
- What triggered the alert?  
- Is this normal behavior?  
- What user/system is involved?  
- Is there lateral movement?  
- Are there indicators of compromise?  

---

## 🔍 Sample SIEM Queries  

### **Splunk — Suspicious Login**
```
index=windows EventCode=4625 OR EventCode=4624
| stats count by Account_Name, Workstation_Name, EventCode
| where count > 10
```

### **Splunk — PowerShell Abuse**
```
index=windows powershell.exe
| stats count by CommandLine, User, Computer
| where count > 5
```

### **Elastic — Rare Process Execution**
```
process where event.type == "start" and process.executable not in (known_good_processes)
```

---

## 🧪 Log Analysis Guides  
### **Windows Logs**
- 4624 — Successful login  
- 4625 — Failed login  
- 4688 — Process creation  
- 7045 — New service installed  

### **Linux Logs**
- `/var/log/auth.log`  
- `/var/log/syslog`  
- `/var/log/secure`  

---

## 🎯 Threat Hunting  
- Establish a hypothesis  
- Identify relevant data sources  
- Run queries  
- Validate findings  
- Document results  
- Map to MITRE ATT&CK  

---

## 📚 MITRE ATT&CK Examples  
- **T1059** — Command Execution  
- **T1078** — Valid Accounts  
- **T1021** — Remote Services  
- **T1047** — WMI Execution  

---

## 📫 Contributions  
This playbook will grow over time as I add more detection rules, IR workflows, and threat hunting content.


# 🛡️ Incident Response Checklist

## 1. Alert Validation
- Identify alert source (SIEM, EDR, IDS, user report)
- Confirm if the alert is true positive or false positive
- Review associated logs and artifacts

## 2. Initial Triage
- Identify impacted user, host, or system
- Determine scope (single system vs. multiple)
- Check for repeated or related alerts
- Assess severity and urgency

## 3. Evidence Collection
- Collect relevant logs (Windows, Linux, firewall, proxy)
- Capture running processes and network connections
- Gather file hashes, suspicious binaries, or scripts
- Export SIEM events related to the incident

## 4. Containment
- Isolate affected host(s)
- Disable compromised accounts
- Block malicious IPs, domains, or hashes
- Stop malicious processes or services

## 5. Eradication
- Remove malware or malicious artifacts
- Patch vulnerabilities
- Reset credentials
- Clean registry entries or scheduled tasks

## 6. Recovery
- Restore systems to normal operation
- Reconnect isolated hosts
- Monitor for recurring activity
- Validate system integrity

## 7. Documentation & Reporting
- Document timeline of events
- Record actions taken and evidence collected
- Update incident ticket
- Submit lessons learned

---

This checklist is part of the SOC Analyst Playbook and will continue to expand as new use cases and workflows are added.

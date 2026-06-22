# 🔍 Incident Triage Guide

## 1. Understand the Alert
- What triggered the alert?
- Which system, user, or application is involved?
- Is this behavior normal or unusual?

## 2. Gather Context
- Review related events in SIEM
- Check recent login activity
- Look for repeated alerts from the same host/user
- Identify any correlated alerts (EDR, firewall, proxy)

## 3. Assess Severity
- Is the system critical?
- Is sensitive data involved?
- Is there evidence of compromise?
- Is lateral movement possible?

## 4. Validate the Alert
- Confirm if it’s a true positive or false positive
- Compare activity against baseline behavior
- Check threat intelligence for IOCs

## 5. Determine Next Steps
- Contain immediately if malicious
- Escalate to Tier 2/IR team if needed
- Document findings in the ticket

---

This guide helps analysts quickly determine the nature and urgency of an alert.

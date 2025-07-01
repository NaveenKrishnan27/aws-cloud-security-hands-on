# Day 18 – GuardDuty Threat Detection with SNS Alerts

✅ **What I Did**
- Enabled Amazon GuardDuty to monitor AWS account activity.
- Simulated a security threat using the `UnauthorizedAccess:EC2/SSHBruteForce` finding.
- Created an EventBridge rule to detect GuardDuty findings.
- Set up an SNS topic to send real-time email alerts for threat detection.

🧠 **Key Learnings**
- GuardDuty can detect threats like SSH brute force, reconnaissance, and credential compromise using AWS log sources.
- EventBridge allows automated reactions to security events.
- SNS integration is useful for real-time alerting to system administrators or security teams.

📸 **Screenshots**
GuardDuty dashboard, simulated finding, EventBridge rule, SNS topic and subscription, and received email alert in `screenshots/`

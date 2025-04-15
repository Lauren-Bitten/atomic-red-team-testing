# 🧪 T1059.001 – PowerShell Execution Test

This test simulates the use of PowerShell to execute a script as part of a threat actor's execution phase. It was performed using the Atomic Red Team framework to validate detection in CrowdStrike Falcon.

---

## 🧾 Test Details

- **MITRE Technique ID:** T1059.001
- **Test Name:** PowerShell Execution
- **Tool:** Atomic Red Team
- **Command Executed:** Simulated credential dumping via PowerShell
- **Test Number:** 1
- **Execution Date:** April 15, 2025
- **Target Host:** Test-Host-01
- **User:** test_user

---

## 🔍 Detection Outcome

- **Result:** ✅ Detected
- **Platform:** CrowdStrike Falcon
- **Response:** Host was automatically contained
- **Visibility:** Multiple alerts tied to PowerShell, cmd.exe, and credential access behavior

---

## 🖼️ Detection Screenshot

![image](https://github.com/user-attachments/assets/d51128f8-9a13-405a-bfa9-512b3f93a639)

_Figure: CrowdStrike alert for T1059.001 – Simulated credential dumping detection._

---

## 💡 Takeaways

- PowerShell-based simulation triggered multiple detections
- CrowdStrike contained the device automatically
- This test validated proper alerting on script-based execution and credential access attempts

---



# 🧪 Atomic Red Team Testing - CrowdStrike Containment Simulation

This repository documents a hands-on cybersecurity test using the [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team) framework to simulate MITRE ATT&CK techniques in a monitored environment. The test triggered real-time detections in CrowdStrike Falcon, including automatic host containment.

---

## 📌 Test Summary

- **MITRE Technique:** [T1059.001 - PowerShell](https://attack.mitre.org/techniques/T1059/001/)
- **Tool Used:** Atomic Red Team + PowerShell
- **Security Platform:** CrowdStrike Falcon
- **Target Host:** `L-23200-011`
- **Outcome:** Falcon correctly identified and auto-contained the simulated credential dumping behavior
- **Command Simulated:** Invoke-Mimikatz via PowerShell (non-malicious simulation)

---

## 📂 Repository Contents

| Folder | Description |
|--------|-------------|
| `T1059.001_PowerShell_Execution/` | Screenshots and notes from the first successful Atomic test |
| `containment-report/` | Official Word document summarizing the containment response |
| `atomic-red-team-setup.md` | Setup steps taken to configure and run Atomic Red Team tests safely |

---

## 🛠 How to Reproduce This Test

1. Clone the Atomic Red Team repo:
   ```powershell
   git clone https://github.com/redcanaryco/atomic-red-team.git C:\AtomicRedTeam
   ```

2. Install the PowerShell module:
   ```powershell
   Install-Module -Name Invoke-AtomicRedTeam -Scope CurrentUser -Force
   Import-Module Invoke-AtomicRedTeam
   ```

3. Run the PowerShell execution test:
   ```powershell
   Invoke-AtomicTest T1059.001 -TestNumbers 1 -PathToAtomicsFolder "C:\AtomicRedTeam\atomics" -Confirm
   ```

4. Monitor alerts in your EDR (e.g., CrowdStrike Falcon)

5. Document and clean up:
   ```powershell
   Invoke-AtomicTest T1059.001 -TestNumbers 1 -PathToAtomicsFolder "C:\AtomicRedTeam\atomics" -Cleanup
   ```

---

## ✅ Lessons Learned

- Atomic Red Team is effective for validating detection rules
- CrowdStrike properly flagged and contained simulated credential dumping
- Testing environments should be pre-approved and closely monitored

---

## 👩🏽‍💻 Author

**Lauren Bitten**  
System Administrator | Cybersecurity Enthusiast  
[LinkedIn](https://www.linkedin.com/in/lauren-bitten-992745196/)  
[GitHub](https://github.com/Lauren-Bitten)

---

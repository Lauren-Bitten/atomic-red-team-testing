
# ⚙️ Atomic Red Team Setup Instructions (Windows)

This guide walks you through setting up and running Atomic Red Team tests safely on a Windows test machine.

---

## 🧰 Prerequisites

- ✅ Windows 10/11 test device
- ✅ PowerShell 5.1 or later
- ✅ Internet access (or download Atomic tests manually)
- ✅ EDR agent installed (e.g., CrowdStrike Falcon)
- ✅ Admin privileges

---

## 📦 Step 1: Install Git (Optional)

Git is used to clone the Atomic Red Team repository:

1. Download Git from: https://git-scm.com/download/win
2. Install with default options

---

## 💻 Step 2: Install Atomic Red Team PowerShell Module

Open PowerShell as Administrator:

```powershell
Install-Module -Name Invoke-AtomicRedTeam -Scope CurrentUser -Force
Import-Module Invoke-AtomicRedTeam
```

---

## 📁 Step 3: Download Atomic Red Team Repo

### Option A: Clone with Git

```powershell
git clone https://github.com/redcanaryco/atomic-red-team.git C:\AtomicRedTeam
```

### Option B: Download ZIP

1. Go to https://github.com/redcanaryco/atomic-red-team
2. Click **Code > Download ZIP**
3. Extract to `C:\AtomicRedTeam`

---

## 🧪 Step 4: Run Your First Test

Example: PowerShell Execution (T1059.001)

```powershell
Invoke-AtomicTest T1059.001 -TestNumbers 1 -PathToAtomicsFolder "C:\AtomicRedTeam\atomics" -Confirm
```

---

## 🧼 Step 5: Cleanup (Optional)

Remove any changes made by the test:

```powershell
Invoke-AtomicTest T1059.001 -TestNumbers 1 -PathToAtomicsFolder "C:\AtomicRedTeam\atomics" -Cleanup
```

---

## 🔐 Safety Notes

- Only run tests on **isolated or designated test systems**
- Always alert your SOC or blue team before testing
- Validate detection and log visibility in your SIEM/EDR platform

---


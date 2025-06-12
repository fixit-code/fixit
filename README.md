# Internal Device Update Package

This repository is used to temporarily host update files for internal device management across our network.

## NSSM (Non-Sucking Service Manager)

This package includes `nssm.exe` to run our internal update script as a Windows service.
NSSM is a trusted open-source tool used by many developers and sysadmins. It is not malware.

Learn more at: https://nssm.cc/

## 📦 oobe.zip

This ZIP archive contains:

- A small CMD script that checks for internet connectivity.
- It automatically starts or stops a custom Windows service named `winupdatedrv` based on internet availability.
- **No background miners, auto-installers, or unauthorized processes** are included.

### ✅ Purpose

This script is used to:
- Help devices auto-recover update service when internet becomes available.
- Ensure the update service stops when there is no connection (to reduce errors or retries).

### ⚠️ Important Notes

- This repository is **not used to distribute malware**.
- The `oobe.zip` file is used **temporarily** during update waves, then removed once deployment is complete.
- The batch script inside is for **internal service control only**, and **does not alter user systems beyond starting/stopping a custom service**.

### 🔒 Security & Transparency

All included scripts are open and readable. If you have any questions or concerns about the contents of `oobe.zip`, feel free to inspect or contact the repository maintainer.

---

**Maintainer:**   FixIT
**Contact:** fixittutorial@gmail.com
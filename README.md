# Windows Hyper-V Manager

This repository provides scripts to safely **enable or disable Hyper-V and related Windows features**, and to check their status.

## Quick Notes
- Run all scripts as **Administrator**.
- A **restart** is required for many changes to take effect.
- Scripts use `DISM` and `bcdedit` commands.

---

## Enable Hyper-V
Run `enable_hyperv.bat` or follow:
1. Go to **Turn Windows features on or off**.
2. Enable **all Hyper-V sections**.
3. Restart your PC.

---

## Disable Hyper-V
Run `disable_hyperv.bat` or follow:
```cmd
bcdedit /set hypervisorlaunchtype off
DISM /Online /Disable-Feature /FeatureName:VirtualMachinePlatform
DISM /Online /Disable-Feature /FeatureName:HypervisorPlatform
DISM /Online /Disable-Feature /FeatureName:Containers-DisposableClientVM

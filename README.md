# Windows Hyper-V Manager

This repository provides scripts to safely **enable or disable Hyper-V and related Windows features**, and to check their status.

## Quick Notes
- Run all scripts as **Administrator**.
- A **restart** is required for many changes to take effect.
- Scripts use `DISM` and `bcdedit` commands.

---

## Enable Hyper-V
follow:
1. Go to **Turn Windows features on or off**.
2. Enable **all Hyper-V sections**.
3. ```cmd
   bcdedit /set hypervisorlaunchtype off
   DISM /Online /Disable-Feature /FeatureName:VirtualMachinePlatform
   DISM /Online /Disable-Feature /FeatureName:HypervisorPlatform
   DISM /Online /Disable-Feature /FeatureName:Containers-DisposableClientVM
4. Restart your PC.
5. Install VirtualBox from this link: [VirtualBox 7.2.4](https://download.virtualbox.org/virtualbox/7.2.4/VirtualBox-7.2.4-170995-Win.exe)
6. After installation, set up your OS in VirtualBox.
---

## Disable Hyper-V
follow:
```cmd
bcdedit /set hypervisorlaunchtype off
DISM /Online /Disable-Feature /FeatureName:VirtualMachinePlatform
DISM /Online /Disable-Feature /FeatureName:HypervisorPlatform
DISM /Online /Disable-Feature /FeatureName:Containers-DisposableClientVM


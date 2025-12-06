⚡ Quick Notes – Hyper-V Management
Important: Always run scripts as Administrator.
Many changes require a system restart to take effect.

🛠 Scripts Used
DISM – Windows feature management
bcdedit – Boot configuration
PowerShell – WindowsOptionalFeature commands

✅ Enabling Hyper-V
Open “Turn Windows Features On or Off”.
Ensure all Hyper-V sections are enabled.
Restart your PC to apply changes.

❌ Disabling Hyper-V
Run the disable_hyperv.ps1 script as Administrator.
Restart your PC to fully remove Hyper-V.

🔍 Checking Hyper-V Status
Use check_hyperv.ps1 to inspect current settings:
Boot configuration (bcdedit)
Installed Windows features (DISM)

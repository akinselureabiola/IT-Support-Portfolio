# Issue Title: Windows Update Failing to Install

# Problem Scenario
A user reports that Windows Updates repeatedly fail to install. Updates show errors and the system prompts restart without completing installation.

# Environment
- Device: Windows 10 workstation
- Update service: Windows Update
- Network: Corporate LAN or home Wi-Fi
- Security: Standard user permissions

# Troubleshooting Steps Performed
1. Verified the device had reliable network connectivity
2. Checked Windows Update history for error codes
3. Restarted the Windows Update service
4. Ran Windows Update Troubleshooter via:
5. Ensured system had enough disk space to apply updates
6. Rebooted PC and attempted update again
7. Installed pending driver updates if required
8. Verified successful installation in Update History tab

# Root Cause
Windows version is out of support, and Microsoft no longer delivers security updates to the build.

# Resolution
Verified system version and confirmed end-of-support message in Windows Update. Recommended upgrade to a current supported Windows version (Windows 10 22H2 or Windows 11) to restore update capability.

# Prevention / Recommendations
- Ensure device is restarted regularly
- Maintain at least 10–15GB of free disk space
- Avoid interrupting update installation
- Enable automatic updates where possible

# Tools Used
- Windows Update Troubleshooter
- Command Prompt (admin)
- Windows Services console
- Settings → Update history

# Skills Demonstrated
- Patch management and update troubleshooting
- Windows service control familiarity
- Command line maintenance tasks
- Endpoint security hygiene

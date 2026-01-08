# Issue Title: Slow Computer Performance on Windows 10/11

# Problem Scenario
A user reports that their computer is running unusually slow. Applications take long to open and the system freezes intermittently.

# Environment
- Device: Dell laptop running Windows 10/11
- User: Standard employee account
- Network: Home setup

#  Troubleshooting Steps
1. Confirmed issue by logging into the user profile
2. Opened Task Manager to check CPU, memory, and disk usage
3. Identified high-memory startup applications running in background
4. Disabled unnecessary startup programs in Task Manager
5. Checked available disk space and cleared temporary files using Disk Cleanup:
- running 'cleanmgr' on command prompt
6. Uninstalled unused applications consuming resources
7. Ran Windows Update and verified latest patches installed
8. Restarted machine and verified performance improvement

# Root Cause
Too many unnecessary startup programs and outdated system patches resulted in reduced performance.

# Resolution
Optimized startup applications, freed disk space, installed updates, and user confirmed a noticeable improvement in system speed.

# Prevention / Recommendation
- Limit unnecessary startup applications
- Encourage users to reboot PCs regularly
- Schedule automatic system updates
- Educate employees on storage hygiene

# Tools Used
- Task Manager (Startup & Performance Tabs)
- Disk Cleanup
- Settings → Apps & Features
- Windows Update

# 📸 Screenshot
![Task Manager](screenshots/Screenshot-resource-usage.png)
![Startup Apps](screenshots/Screenshot-disabling-unused-apps.png)
![Windows Update](screenshots/Screenshot-windows-update.png)

# Key Skills Demonstrated
- Windows OS performance diagnosis
- Memory and CPU usage monitoring
- System optimization and cleanup
- End-user communication and education

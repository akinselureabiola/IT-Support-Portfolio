# Slow Computer Performance — Windows 10/11 Optimization

## Ticket Information

- **Category:** Windows / Performance / Desktop Support
- **Priority:** P3 – Medium
- **Impact:** Single user experiencing degraded system performance
- **SLA Target:** 4 hours
- **Resolution Time:** 1 hour
- **Status:** Resolved

---

## Scenario

**User Reported:**

> “My computer is extremely slow and keeps freezing.”

The user reported:

- Applications taking long to open
- System freezing intermittently
- Slow login time
- Overall degraded performance

No error messages were displayed.

---

## Environment

- **Device:** Dell Laptop
- **Operating System:** Windows 10 / Windows 11
- **User Account:** Standard Employee Account
- **Network:** Home setup
- **Antivirus:** Microsoft Defender (Active)

---

## Initial Symptoms

Observed on affected device:

- High memory usage at startup
- Multiple applications auto-launching
- Disk usage spiking intermittently
- System responsiveness significantly reduced

No hardware failure indicators present.

---

## Business Impact

If unresolved:

- Reduced employee productivity
- Increased task completion time
- Potential missed deadlines
- Increased support dependency

Issue impacted user efficiency but did not affect wider infrastructure.

---

## Investigation Steps

### Step 1 — Validate Performance Issue

Logged into user profile and confirmed:

- Noticeable system lag
- Delayed application response

Opened:

Task Manager → Performance Tab

Observed:

- High memory usage
- Several startup programs consuming resources

---

### Step 2 — Review Startup Applications

Opened:

Task Manager → Startup Tab

Identified:

- Multiple high-impact startup applications
- Non-essential programs running at login

Disabled unnecessary startup applications.

---

### Step 3 — Check Disk Space and Temporary Files

Opened:

Disk Cleanup (cleanmgr)

Removed:

- Temporary files
- System cache
- Recycle Bin contents

Confirmed sufficient free disk space available.

---

### Step 4 — Remove Unused Applications

Navigated to:

Settings → Apps & Features

Uninstalled:

- Unused resource-heavy applications
- Outdated third-party software

---

### Step 5 — Verify System Updates

Opened:

Settings → Windows Update

Checked for pending updates.

Installed:

- Latest Windows security patches
- Performance-related updates

Restarted system after updates completed.

---

## Root Cause

System slowdown was caused by:

- Excessive startup applications consuming memory
- Accumulated temporary files
- Outdated system patches

These combined factors resulted in reduced system performance.

---

## Resolution Steps

1. Disabled unnecessary startup programs
2. Cleared temporary files using Disk Cleanup
3. Uninstalled unused applications
4. Installed pending Windows updates
5. Restarted device
6. Re-tested performance

---

## Verification

After optimization:

- Startup time significantly improved
- Applications launched faster
- CPU and memory usage normalized
- No system freezes observed
- User confirmed noticeable performance improvement

System performance restored successfully.

---

## Tools Used

- Task Manager (Performance & Startup Tabs)
- Disk Cleanup (cleanmgr)
- Settings → Apps & Features
- Windows Update

---

## Screenshots

## Screenshots (Evidence)

### High Memory Usage
![Task Manager - High Memory Usage](screenshots/task-manager-memory.png)

### Startup Programs Impact
![Startup Programs](screenshots/startup-impact.png)

---

## Skills Demonstrated

- Windows OS performance troubleshooting
- Resource usage monitoring (CPU / Memory / Disk)
- Startup optimization
- Disk cleanup and storage management
- Patch management validation
- Structured desktop support workflow
- End-user communication and education

---

## Key Takeaway

Slow system performance is often caused by:

1. Excessive startup applications
2. Insufficient disk space
3. Outdated system patches

A structured troubleshooting approach ensures efficient diagnosis and resolution without unnecessary system reinstallation.

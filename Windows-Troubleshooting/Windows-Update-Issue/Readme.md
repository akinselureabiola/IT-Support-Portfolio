# Windows Update Failing to Install — Patch Management Troubleshooting

## Ticket Information

- **Category:** Windows / Patch Management / Desktop Support
- **Priority:** P2 – High
- **Impact:** Endpoint unable to receive security and feature updates
- **SLA Target:** 4 hours
- **Resolution Time:** 1 hour 15 minutes
- **Status:** Resolved

---

## Scenario

**User Reported:**

> “Windows updates keep failing and won’t install.”

The user reported:

- Repeated update failures
- System prompting restart without completing installation
- Error messages displayed in Update History
- Security updates not installing

The issue persisted after multiple restart attempts.

---

## Environment

- **Device:** Windows 10 Workstation
- **Update Service:** Windows Update
- **Network:** Corporate LAN / Home Wi-Fi
- **User Permissions:** Standard User
- **Security:** Microsoft Defender enabled

---

## Initial Symptoms

Observed on affected device:

- Windows Update showing "Failed to Install"
- Error codes displayed in Update History
- Pending restart notifications
- No active system crashes

System remained operational but unpatched.

---

## Business Impact

If updates fail to install:

- Security vulnerabilities remain unpatched
- Compliance risks increase
- Device exposed to potential exploits
- Long-term system instability possible

Although device remained functional, security posture was compromised.

---

## Investigation Steps

### Step 1 — Verify Network Connectivity

Confirmed stable internet connection.

Tested:

    ping google.com

Result: Successful

Network connectivity not identified as root cause.

---

### Step 2 — Review Update History

Navigated to:

    Settings → Update & Security → Windows Update → View Update History

Observed repeated failures.

---

### Step 3 — Restart Windows Update Service

Opened:

    services.msc

Restarted:

    Windows Update Service (wuauserv)

Attempted update installation again.

Issue persisted.

---

### Step 4 — Run Windows Update Troubleshooter

Navigated to:

    Settings → Troubleshoot → Additional Troubleshooters → Windows Update

Executed built-in troubleshooter.

---

### Step 5 — Verify Disk Space

Checked available disk space:

    This PC → Local Disk (C:)

Confirmed sufficient free space (greater than 15GB available).

---

### Step 6 — Verify Windows Version

Opened:

    winver

Observed Windows version had reached End of Support.

Confirmed current build no longer receiving updates.

---

## Root Cause

The installed Windows build had reached end-of-support status.

Because of this:

- Microsoft no longer delivered security patches
- Update installation attempts repeatedly failed
- System could not receive cumulative updates

Failure was version-related, not network or service-related.

---

## Resolution Steps

1. Confirmed unsupported Windows version.
2. Verified official Microsoft end-of-support status.
3. Recommended upgrade to supported version:
   - Windows 10 22H2
   - Or upgrade to Windows 11
4. Backed up user data as precaution.
5. Initiated Windows Feature Update / Upgrade process.
6. Verified update capability restored after upgrade.

---

## Verification

After upgrade:

- Windows Update successfully downloaded and installed updates
- No further installation errors observed
- System restarted successfully
- Update History confirmed successful installation
- User confirmed system operating normally

Patch management functionality restored.

---

## Tools Used

- Windows Update Troubleshooter
- Services Console (services.msc)
- Command Prompt (Administrative)
- winver command
- Settings → Update History
- Microsoft Support Lifecycle Documentation

---

## Skills Demonstrated

- Patch management troubleshooting
- Windows service control
- Version lifecycle awareness
- OS upgrade validation
- Endpoint security assessment
- Structured troubleshooting methodology
- Clear user communication

---

## Key Takeaway

When Windows Updates repeatedly fail:

1. Verify network connectivity
2. Check Update History for error codes
3. Restart update services
4. Confirm disk space availability
5. Validate Windows version support lifecycle



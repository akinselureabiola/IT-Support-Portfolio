# IT Support Ticket Lifecycle — End-to-End Incident Resolution

## Ticket Information

- **Category:** IT Operations / Service Desk / ITIL Process
- **Priority:** P3 – Medium
- **Impact:** Single user connectivity issue
- **SLA Target:** 4 hours (First response within 15 minutes)
- **Resolution Time:** 40 minutes
- **Status:** Resolved

---

## Scenario

**User Reported (via Service Desk Portal):**

> “Cannot connect to office Wi-Fi. Others are connected.”

The user submitted a ticket through the help desk portal reporting inability to connect to the corporate wireless network. Other employees in the same location were not experiencing issues.

---

## Environment

- **Device:** Windows 10/11 Laptop
- **Network:** Corporate Wi-Fi (DHCP Enabled)
- **Authentication:** WPA2 Enterprise
- **User Account:** Standard Domain User
- **Support Model:** ITIL-based Service Desk Workflow

---

## Initial Symptoms

Observed during first contact:

- Wi-Fi network visible but not connecting
- “No Internet, Secured” message displayed
- Other users connected successfully
- No system-wide outage reported

Issue appeared isolated to a single endpoint.

---

## Business Impact

If unresolved:

- User unable to access email, shared drives, and internal systems
- Reduced productivity
- Increased dependency on IT support

Although impact was limited to one user, connectivity issues directly affect daily operations.

---

## Ticket Lifecycle Process

### 1 — Ticket Received

- Ticket submitted via Service Desk Portal
- Category assigned: Connectivity Issue
- Priority set to: P3
- Auto-generated ticket ID
- Status set to: Open

---

### 2 — Triage and First Response

Acknowledged ticket within SLA (under 15 minutes).

Asked clarifying questions:

- Current physical location?
- Is anyone else affected?
- Has the device been recently updated?
- Are other networks connecting successfully?

Updated ticket status to:

    In Progress

---

### 3 — Troubleshooting and Diagnosis

Performed structured troubleshooting:

1. Confirmed Wi-Fi adapter was enabled
2. Attempted connection to correct SSID
3. Ran:

    ipconfig

Observed:

    No IPv4 address assigned

4. Opened Device Manager and disabled/re-enabled wireless adapter
5. Released and renewed DHCP lease:

    ipconfig /release
    ipconfig /renew

Confirmed valid IP address assigned from DHCP server.

---

### 4 — Communication with User

- Explained troubleshooting steps clearly
- Managed expectations
- Provided reassurance that issue was isolated
- Kept ticket updated with documented findings

Maintained professional communication throughout.

---

### 5 — Solution Applied

- Re-enabled wireless adapter
- Renewed DHCP lease
- Reconnected to corporate SSID

User regained full network access.

Ticket status updated to:

    Resolved — Pending User Confirmation

---

### 6 — User Validation

User confirmed:

- Internet access restored
- Shared drives accessible
- Email functioning normally

Ticket status updated to:

    Closed

Final resolution notes documented in ticket system.

---

## Root Cause

Wireless network adapter had entered an unstable state and failed to obtain a DHCP lease.

This prevented the device from receiving a valid IP address required for network communication.

---

## Verification

- Valid IPv4 address assigned
- Internet connectivity restored
- Internal resources accessible
- No further connection errors reported
- User confirmed successful resolution

---

## Tools Used

- Service Desk Ticketing System (Simulated)
- Device Manager
- Command Prompt
- ipconfig
- Windows Network Settings

---

## Skills Demonstrated

- ITIL-based ticket lifecycle management
- SLA adherence and prioritization
- Structured troubleshooting methodology
- DHCP diagnostics
- Clear documentation practices
- Customer communication skills
- Incident closure workflow

---

## Key Takeaway

Effective IT support is not only about fixing technical issues but also about:

1. Proper ticket categorization
2. SLA compliance
3. Clear documentation
4. Consistent communication
5. Structured troubleshooting
6. Professional incident closure

Strong ticket lifecycle management is essential for enterprise IT service delivery.

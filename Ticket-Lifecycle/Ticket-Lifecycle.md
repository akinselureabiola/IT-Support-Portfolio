# Issue Title: IT Support Ticket Lifecycle — End-to-End Resolution

# Scenario Overview
A user reports a technical issue through the company’s help desk system. This case study demonstrates how the ticket flows from report to resolution following ITIL-style processes.

# 1. Ticket Received
- Source: User submitted ticket through Service Desk Portal
- Category: Connectivity Issue
- Priority: P3 (User-facing, low business impact)
- Description: “Cannot connect to office Wi-Fi. Others are connected.”

# 2. Triage and First Response
- Acknowledged within SLA (15 minutes)
- Asked clarifying questions:
  - Location?
  - Is anyone else affected?
  - Device recently updated?

Updated ticket comments and assigned status: **In Progress**

# 3. Troubleshooting & Diagnosis
Performed remote and in-person checks:
1. Confirmed Wi-Fi enabled
2. Validated SSID connection attempt
3. Ran `ipconfig` to confirm no IP assigned
4. Restarted adapter in Device Manager
5. Confirmed DHCP lease was granted

Documented findings in ticket

# 4. Communication With User
- Explained steps in simple language
- Managed user expectations
- Advised potential next steps if issue persisted

# 5. Solution Applied
- Enabled adapter
- Reconnected to SSID
- User regained network access

Ticket moved to **Resolved — Pending User Confirmation**

# 6. User Validation
User tested connection and confirmed success.
Ticket closed with summary notes.

# Outcome
Wi-Fi issue resolved within SLA.
User satisfied and confirmed closure.

# Skills Demonstrated
- ITIL ticket handling
- Communication & documentation
- Root cause analysis
- SLA management
- Customer service mindset

# Tools Referenced
- Ticketing system (simulated)
- Device Manager
- ipconfig
- Windows network settings

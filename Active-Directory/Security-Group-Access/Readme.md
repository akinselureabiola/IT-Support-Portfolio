# Security Group Access (Shared Folder Permission Issue)

## Ticket Information

- **Category:** Active Directory / File Server / Access Control  
- **Priority:** P3 – Medium  
- **Impact:** Single user unable to access shared company folder  
- **SLA Target:** 4 hours  
- **Resolution Time:** 50 minutes  
- **Status:** Resolved  

---

## Scenario

**User Reported:**

> “I can’t access the shared company folder.”

When attempting to open the shared folder, the user received:

    Access Denied

Other users were able to access the folder successfully.

---

## Environment

- **Domain:** bpurple.com  
- **Domain Controller:** DC01 (192.168.10.10)  
- **Client Machine:** CLIENT01 (Domain-joined)  
- **Shared Folder Path:** \\DC01\Finance-Share  
- **Security Group:** Finance-Access  
- **Virtualization:** VirtualBox (Internal Network + NAT)  
- **DNS Server:** 192.168.10.10  

---

## Network Architecture Diagram

![Active Directory Lab Network Architecture](ad-lab-network-architecture.png)

---

**Configuration Notes:**

- Adapter 1 → Internal Network (intnet)  
- Adapter 2 → NAT (Internet access)  
- DNS Server → 192.168.10.10  
- Domain → bpurple.com  

---

## Initial Symptoms

On CLIENT01:

    \\DC01\Finance-Share

Result:

    Access Denied

Connectivity validation:

    ping 192.168.10.10
    ping dc01.bpurple.com

Result: Successful  

Network and DNS were functioning correctly.

---

## Business Impact

Without proper access:

- User unable to retrieve or store business files  
- Team collaboration disrupted  
- Potential delays in finance operations  
- Increased support workload  

This issue affects productivity but is limited to a single user.

---

## Investigation Steps

### Step 1 — Validate Network Connectivity

Executed:

    ping 192.168.10.10

Result: Successful  

Confirmed network communication with Domain Controller.

---

### Step 2 — Validate Share Availability

Accessed shared folder from another user account.

Result: Successful  

Confirmed that the shared folder and server were operational.

---

### Step 3 — Review Share and NTFS Permissions

On DC01:

Opened:

    C:\Finance → Properties → Sharing → Advanced Sharing
    Security Tab → NTFS Permissions

Verified:

- Share permissions assigned to: Finance-Access (Modify)
- NTFS permissions assigned to: Finance-Access (Modify)
- No direct user permissions configured

Permissions were correctly configured at group level.

---

### Step 4 — Verify Group Membership

Opened:

    Active Directory Users and Computers

Navigated to:

    Finance-Access Security Group

Checked membership.

User was **not listed** as a member of Finance-Access.

---

## Root Cause

The user was not a member of the security group assigned to the shared folder.

Although Share and NTFS permissions were correctly configured, access was denied because the user lacked required group membership.

Permission enforcement was functioning as designed.

---

## Resolution Steps

1. Opened:

    Active Directory Users and Computers

2. Located:

    Finance-Access Security Group

3. Added user:

    john

4. Saved changes.

5. Instructed user to log off and log back in to refresh Kerberos authentication token.

---

## Verification

- User logged back into CLIENT01  
- Accessed:

    \\DC01\Finance-Share

- Folder opened successfully  
- No "Access Denied" message  
- User confirmed issue resolved  

Access restored successfully.

---

## Skills Demonstrated

- Active Directory user and group management  
- Share vs NTFS permission understanding  
- Group-based access control design  
- Kerberos token refresh awareness  
- Structured troubleshooting methodology  
- Enterprise documentation standards  

---

## Key Takeaway

In enterprise environments, permissions should be assigned to security groups — not individual users.

When troubleshooting access issues:

1. Confirm connectivity  
2. Confirm share functionality  
3. Verify Share permissions  
4. Verify NTFS permissions  
5. Confirm user group membership  

Security group-based access control ensures scalable and manageable permission administration.

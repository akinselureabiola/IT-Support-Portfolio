# Issue Title: User Cannot Access Shared Folder (Access Denied)

# Problem Scenario
A user reports being unable to access a shared network folder needed for work and sees an “Access Denied” error. Other users in the same department can access it.

# Environment
- Windows workstation (10/11)
- Shared folder hosted on local server or file server
- NTFS and Share permissions
- Active Directory security group membership

# Troubleshooting Steps
1. Confirmed user is connected to the network
2. Verified correct shared folder path (\\Server\DepartmentShare)
3. Tested access by browsing to UNC path manually
4. Confirmed other users could access the folder
5. Checked user's AD group membership
6. Added missing security group ( Marketing-Share)
7. Verified permissions on shared folder (NTFS + Share)
8. Forced new permissions using:

9. Logged user out and back in
10. User confirmed folder access now works

# Root Cause
User account was **not added to the correct AD security group**, so the system denied access.

# Resolution
Added user to correct group, refreshed group policy, and validated access.

# Prevention / Recommendation
- Maintain onboarding checklist to ensure group access is assigned
- Standardize department-based security groups
- Grant least privilege privileges only

# Tools Used
- Active Directory Users and Computers
- Permissions tab (Security Properties)
- gpupdate /force
- Command Prompt (basic testing)
- Windows File Explorer UNC navigation

# Key Skills Demonstrated
- NTFS and network file permission troubleshooting
- Group membership analysis and correction
- Active Directory security understanding
- User assistance and clear communication

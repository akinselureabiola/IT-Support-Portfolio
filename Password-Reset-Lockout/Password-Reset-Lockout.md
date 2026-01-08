# Issue Title: User Account Locked After Multiple Failed Login Attempts

# Problem Scenario
User reports being unable to sign in to their workstation. Error message displayed: "Account locked due to too many failed login attempts". User claims they forgot their password.

# Environment
- System: Windows 10 / Windows 11
- Domain: bpurple.com
- Directory service: Active Directory
- User type: Standard employee account

# Troubleshooting Steps
1. Verified user's identity (security questions / employee ID)
2. Confirmed lockout status in Active Directory
3. Checked account status properties
4. Cleared account lockout flag
5. Reset user password with strong temporary password
6. Ensured password meets complexity requirements
7. Instructed user to change password upon login
8. Confirmed successful workstation sign-in

# Root Cause
User entered an incorrect password multiple times which triggered domain lockout policy.

# Resolution
Unlocked account in Active Directory and reset password. User logged in successfully and updated password.

# Prevention / Recommendation
- Provide password guidelines to users
- Encourage use of password manager
- Communicate lockout policy expectations
- Suggest MFA

# Tools Used
- Active Directory Users and Computers (ADUC)
- Company lockout policy

# Key Skills Demonstrated
- Active Directory account administration
- Identity verification / security procedures
- Password reset protocol
- User communication and instruction

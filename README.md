# Revoking User Sessions and Disabling Accounts in Microsoft Entra ID

## Project Overview

Identity and Access Management (IAM) is a critical component of modern cybersecurity practices. One of the most important administrative responsibilities is ensuring that users who should no longer have access to organizational systems are removed immediately.

This project demonstrates how to manually **revoke active user sessions** and **disable a user account** in **Microsoft Entra ID (formerly Azure Active Directory)**.

Although many organizations rely on automated processes to handle user offboarding, administrators must understand how to manually perform these actions in urgent scenarios such as:

- Employee termination
- Department transfers
- Security investigations
- Suspected compromised accounts
- Insider threat mitigation

Revoking sessions ensures that all active authentication tokens are invalidated, while disabling the account prevents future login attempts.

---

# Objectives

The objective of this project is to demonstrate how administrators can:

- Locate and manage users in Microsoft Entra ID
- Revoke active user sessions
- Disable user accounts
- Understand the security impact of session management

---

# Technologies Used

- Microsoft Entra ID (Azure Active Directory)
- Azure Portal
- Identity and Access Management (IAM)

---

# Walkthrough

## Step 1: Locate the User

Navigate to **Microsoft Entra ID → Users** and locate the account that requires access removal.

Select the target user from the list to open the user management panel.

![Locate User](images/step1_users.png)

---

## Step 2: Revoke Active Sessions

Within the user's profile page, locate the **Revoke Sessions** option.

Selecting this option invalidates all currently active authentication tokens associated with the user.

![Revoke Sessions](images/step2_revoke_sessions.png)

---

## Step 3: Confirm Session Revocation

A confirmation prompt will appear asking if you want to revoke all active sessions.

Select **Yes** to confirm.

![Confirm Revocation](images/step3_confirm_revoke.png)

After confirmation, the user will be required to reauthenticate on all devices.

---

## Step 4: Access User Properties

Next, navigate to the user's profile and review the available configuration options.

![User Profile](images/step4_user_profile.png)

The **Properties** section contains settings related to the user's account status.

---

## Step 5: Disable the Account

Scroll down to the **Settings** section and locate **Account Enabled**.

Uncheck **Account Enabled** to disable the account.

![Disable Account](images/step5_disable_account.png)

Once disabled, the user will no longer be able to sign into Microsoft services.

---

# Why Revoking Sessions is Important

Disabling an account alone may not immediately terminate existing authenticated sessions. If a user already has an active session token, they may still be able to access resources until that token expires.

Revoking sessions ensures:

- Immediate termination of authenticated access
- All devices are signed out
- Authentication tokens become invalid
- Access control changes take effect instantly

---

# Real World Security Scenarios

### Employee Offboarding
When an employee leaves an organization, administrators must ensure they immediately lose access to company resources.

### Department Transfers
Users changing roles may need immediate removal from systems associated with their previous department.

### Security Incidents
If an account is suspected of being compromised, revoking sessions and disabling the account prevents further unauthorized activity.

### Administrative Investigations
During disciplinary investigations, immediate access removal may be required to protect sensitive data.

---

# Security Concepts Demonstrated

This project demonstrates several important cybersecurity principles:

- Identity and Access Management (IAM)
- Session Management
- Access Revocation
- Insider Threat Mitigation
- Incident Response

---

# Security Framework Alignment

This process aligns with best practices from major cybersecurity frameworks.

## NIST SP 800-53

Relevant controls include:

- AC-2: Account Management
- AC-7: Unsuccessful Login Attempts
- IA-5: Authenticator Management

## CIS Critical Security Controls

Relevant controls include:

- CIS Control 5: Account Management
- CIS Control 6: Access Control Management

---

# Key Takeaways

- Disabling an account does not always terminate active sessions immediately
- Session revocation invalidates authentication tokens
- Both actions together ensure immediate removal of access
- Manual knowledge of these actions is critical during security incidents

---

# Future Improvements

Possible enhancements to this project include:

- Automating session revocation using PowerShell
- Using Microsoft Graph API for identity management
- Monitoring revocation events through audit logs
- Implementing conditional access policies

---

# Author

David Padilla 
Focused on Cloud Security, Identity and Access Management, and Incident Response

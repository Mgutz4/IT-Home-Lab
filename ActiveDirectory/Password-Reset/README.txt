LAB: Password Reset & Account Unlock (Active Directory)

AUTHOR: Mark Gutierrez

---

OVERVIEW:

This lab demonstrates a common IT support scenario involving a locked-out user account in an Active Directory environment. The objective was to simulate failed login attempts, trigger an account lockout based on domain policy, and perform administrative recovery by unlocking the account and resetting the password.

---

OBJECTIVES:

* Simulate user account lockout due to failed login attempts
* Identify account lockout status in Active Directory
* Reset user password
* Unlock user account
* Verify successful login on a domain-joined client machine
* Analyze related security events in Event Viewer

---

ENVIRONMENT:

* Windows Server 2022 (Domain Controller)
* Windows 10 (Client Machine - CLIENT02)
* Domain: corp.local
* Tools Used:

  * Active Directory Users and Computers (ADUC)
  * Group Policy Management (GPMC)
  * Event Viewer
  * Command Prompt (whoami, gpresult)

---

STEPS PERFORMED:

1. Account Lockout Simulation

   * Performed multiple failed login attempts on CLIENT02
   * Triggered account lockout based on configured domain policy

2. Lockout Verification

   * Opened Active Directory Users and Computers (ADUC)
   * Navigated to the HR Organizational Unit (OU)
   * Confirmed account lockout status in user properties

3. Password Reset & Account Unlock

   * Reset user password using ADUC
   * Enabled "User must change password at next logon"
   * Unlocked the user account

4. Client Login Verification

   * Logged into CLIENT02 using updated credentials
   * Successfully authenticated to the domain
   * Verified user context using:

     * Command: whoami

5. Event Log Analysis

   * Opened Event Viewer on the Domain Controller
   * Navigated to:
     Windows Logs → Security
   * Identified:

     * Event ID 4740 (Account Locked Out)
   * (Optional) Verified failed login attempts on client:

     * Event ID 4625 (Failed Logon)

---

RESULTS:

* Successfully simulated and resolved a user account lockout
* Restored user access through password reset and account unlock
* Verified authentication from the client machine
* Confirmed relevant security events in Event Viewer

---

KEY CONCEPTS:

* Active Directory User Management
* Account Lockout Policies
* Password Reset Procedures
* Authentication & Security Logging
* Event Viewer Analysis
* Client-Server Interaction in Domain Environments

---

LESSONS LEARNED:

* Account lockout events (Event ID 4740) are logged on the Domain Controller
* Failed login attempts (Event ID 4625) may be logged on the client machine
* Group Policy settings directly impact account lockout behavior
* Cross-verification between server and client is essential for troubleshooting

---

SCREENSHOTS INCLUDED:

* AD_Account_Locked.png
* Password_Reset_and_Account_Unlock.png
* Password_Reset_Prompt_Successful.png
* Whoami_Verification.png

---

LAB: Workstation Control via Group Policy (Active Directory)

AUTHOR: Mark Gutierrez

---

OVERVIEW:

This lab demonstrates how Group Policy Objects (GPOs) are used to manage and restrict user environments within an Active Directory domain. The objective was to apply user-based restrictions, such as limiting access to the Control Panel, and verify enforcement on domain-joined client machines.

---

OBJECTIVES:

* Create and link Group Policy Objects (GPOs) to Organizational Units (OUs)
* Configure user-based restrictions (e.g., Control Panel access)
* Apply policies to specific user groups (HR Users)
* Verify policy enforcement on client machines
* Demonstrate centralized management of user environments

---

ENVIRONMENT:

* Windows Server 2022 (Domain Controller)
* Windows 10 (Client Machine - CLIENT02)
* Domain: corp.local
* Tools Used:

  * Group Policy Management (GPMC)
  * Active Directory Users and Computers (ADUC)
  * Command Prompt (gpupdate, gpresult)

---

STEPS PERFORMED:

1. GPO Creation

   * Opened Group Policy Management Console (GPMC)
   * Created new GPOs including:

     * HR Drive Mapping
     * Workstation Restrictions (Control Panel Access)

2. GPO Configuration

   * Configured user restrictions under:
     User Configuration → Administrative Templates
   * Disabled access to Control Panel and system settings
   * Configured drive mapping using Group Policy Preferences

3. GPO Linking

   * Linked GPOs to the HR Organizational Unit (OU)
   * Ensured policies targeted the correct users

4. Policy Application

   * Forced policy update on client machine using:

     * Command: gpupdate /force

5. Policy Verification

   * Verified applied policies using:

     * Command: gpresult /r
   * Logged into CLIENT02 and confirmed restrictions were enforced

---

RESULTS:

* Successfully applied user-based restrictions through Group Policy
* Restricted access to Control Panel for targeted users
* Verified policy enforcement on domain-joined client machine
* Demonstrated centralized control of user environments

---

KEY CONCEPTS:

* Group Policy Management
* OU-Based Policy Targeting
* User Configuration vs Computer Configuration
* Administrative Templates
* Policy Application & Verification

---

LESSONS LEARNED:

* GPOs must be properly linked to OUs to apply to intended users
* User-based policies require correct OU placement and login context
* gpupdate and gpresult are essential tools for policy troubleshooting
* Group Policy provides centralized control over user environments

---

SCREENSHOTS INCLUDED:

* 02_Control_Panel_Disabled_New_GPO.png
* 03_Employees_Disabled_Panel_GPO.png
* 04_Editing_GPO.png
* 05_GPO_Integrated_Succesfully.png

---
---

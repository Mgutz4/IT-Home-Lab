LAB COMPONENT: Group Policy Management

OVERVIEW:
This section demonstrates the creation and application of Group Policy Objects (GPOs) within an Active Directory environment.

OBJECTIVE:
- Create and link GPOs to Organizational Units (OUs)
- Configure user-based policies
- Apply policies to domain users
- Verify policy enforcement on client machines

CONFIGURATION:
- Created multiple GPOs including:
  - HR Drive Mapping
  - User Restrictions (e.g., Control Panel access)
- Linked GPOs to appropriate OUs (HR Users)
- Configured policies under:
  - User Configuration
  - Administrative Templates
  - Preferences (Drive Mapping)

TESTING:
- Applied policies using:
  gpupdate /force
- Verified applied policies using:
  gpresult /r
- Confirmed policy effects on CLIENT02

RESULT:
- GPOs successfully applied to targeted users
- Policies enforced based on OU structure
- User environment controlled centrally

SKILLS DEMONSTRATED:
- Group Policy Management
- OU-based policy targeting
- User configuration control
- Policy verification and troubleshooting
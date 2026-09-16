# Basic Employee Onboarding (AD)(RBAC)

## Problem Statement

Northstar Medical Group needed a more organized way to manage employee accounts and access. The previous MSP left the Active Directory environment without a consistent structure, relying on manual processes and inconsistent user and group assignments. This made account management harder and increased the risk of employees receiving access or policies that did not match their roles. For a healthcare organization, inconsistent access controls can also create security and HIPAA compliance concerns.

## Solution Overview

I built a Windows Server Active Directory environment for Northstar Medical Group using the NMG.com domain. I created Organizational Units (OUs) for Finance, HR, IT, and Operations to organize employee accounts by department. I created corresponding security groups and implemented a flat role-based access control (RBAC) structure to manage department-based access. I provisioned 15 employee accounts using consistent usernames, UPNs, department information, and group assignments. I then used the environment to troubleshoot and resolve an access issue involving incorrect OU placement and security group membership.

## Video Walkthrough

Coming soon.

## Tools Used

- Windows Server
- Active Directory Domain Services (AD DS)
- Active Directory Users and Computers (ADUC)
- VirtualBox
- Group Policy
- Role-Based Access Control (RBAC)
- GitHub

## Project Timeline

### Day 1 - Domain Setup
- Configured the Windows Server environment
- Created the NMG.com domain
- Promoted the server to a domain controller
- Verified domain controller health using dcdiag

### Day 2 - OU and Security Group Design
- Created Organizational Units for Finance, HR, IT, and Operations
- Created department-based security groups
- Established the structure for role-based access control

### Day 3 - User Provisioning and RBAC
- Provisioned 15 employee accounts
- Used consistent username and UPN naming conventions
- Assigned users to their appropriate departmental OUs
- Assigned users to department-based security groups
- Verified security group memberships

### Day 4 - Support Ticket NMG-0047
- Investigated an HR user's access issue
- Identified incorrect OU placement and group membership
- Moved the affected user to the correct HR OU
- Corrected the user's HR security group membership
- Verified the changes in Active Directory
- Documented the root cause, resolution, and verification

### Day 5 - Documentation and Portfolio
- Organized project screenshots and documentation
- Documented the RBAC structure
- Packaged the support ticket resolution
- Created this GitHub case study

## Key Accomplishments

- Built the NMG.com Active Directory domain from scratch
- Designed a department-based OU structure for Finance, HR, IT, and Operations
- Implemented RBAC using security groups mapped to each department
- Provisioned 15 employee accounts using consistent naming and attribute standards
- Configured and verified department security group memberships
- Diagnosed a multi-cause access issue involving incorrect OU placement and group membership
- Corrected the Active Directory configuration and verified the resolution
- Documented the incident with root cause, remediation, and verification details

## Support Ticket - NMG-0047

During the lab, I investigated an access issue affecting Jane Cooper, an HR Payroll Specialist who was unable to access the same HR resources as her teammates and was receiving different desktop policies.

I reviewed her Active Directory account and identified two configuration issues: her account was located in the wrong Organizational Unit and her security group membership did not match her HR role.

I moved Jane's account to the HR OU and corrected her membership to the HR-Users security group. I then verified that her account appeared in the correct OU and confirmed her membership in HR-Users.

The full resolution and root cause analysis are included in the Incident-Reports folder.

## Repository Structure

Basic-Employee-Onboarding-AD-RBAC/

- Documentation/
  - Domain configuration documentation
  - OU and security group documentation
  - User list documentation
  - RBAC structure documentation

- Screenshots/
  - Day 1 - Domain setup and domain controller verification
  - Day 2 - OU and security group configuration
  - Day 3 - User provisioning and group membership verification
  - Day 4 - NMG-0047 remediation and verification

- Incident-Reports/
  - NMG-0047-Resolution.txt

- README.md

## Skills Demonstrated

- Active Directory administration
- Windows Server administration
- Domain controller configuration
- Organizational Unit management
- User account provisioning
- Security group administration
- Role-Based Access Control (RBAC)
- Identity and access troubleshooting
- Root cause analysis
- Incident resolution
- Technical documentation

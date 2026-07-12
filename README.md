<h1 align="center"> IAM & Zero Trust Lab</h1>

## Overview

This project demonstrates the design and implementation of a practical Identity and Access Management (IAM) and Zero Trust security lab using Microsoft Entra ID (formerly Azure Active Directory). The objective of this lab is to simulate how modern organizations manage digital identities, user access, administrative permissions, and security controls within a cloud environment.

The project focuses on implementing fundamental IAM concepts such as user provisioning, security groups, Role-Based Access Control (RBAC), administrative role assignments, least privilege, and the Joiner-Mover-Leaver (JML) lifecycle. It also documents enterprise security policies, access review procedures, and identity governance practices that are commonly used in production Microsoft Entra ID environments.

Although Microsoft Entra ID Free was used to build the majority of this lab, the project has been designed following Microsoft's Zero Trust security principles. Features requiring Microsoft Entra ID Premium, including Conditional Access and advanced Multi-Factor Authentication (MFA) policies, are documented as planned implementations to demonstrate understanding of enterprise identity security.

This project serves as a practical portfolio demonstrating hands-on experience with Microsoft Entra ID administration, identity management, RBAC implementation, security group management, and identity governance concepts commonly used by SOC Analysts, IAM Engineers, Azure Administrators, and Microsoft Security professionals.

## Project Objectives

The primary objectives of this project are:

- Build a cloud-based Identity and Access Management environment using Microsoft Entra ID.
- Create and manage organizational users and identities.
- Organize users using Security Groups.
- Implement Role-Based Access Control (RBAC).
- Apply the Principle of Least Privilege.
- Assign administrative roles based on business responsibilities.
- Demonstrate enterprise Joiner-Mover-Leaver (JML) identity lifecycle management.
- Perform access reviews and permission validation.
- Document enterprise security policies.
- Develop architecture documentation suitable for production environments.
- Build a professional GitHub portfolio project demonstrating practical Microsoft Entra ID administration.

## Project Architecture

The architecture is centered around Microsoft Entra ID, which acts as the organization's cloud identity provider. Every user identity is managed centrally through Microsoft Entra ID. Users are assigned to Security Groups based on their departments and organizational responsibilities.

Administrative permissions are assigned through Role-Based Access Control (RBAC), ensuring users receive only the permissions required for their job functions. This implementation follows Microsoft's Zero Trust model by verifying identities, enforcing least privilege, and securing access to enterprise resources.

The architecture also demonstrates user lifecycle management through Joiner, Mover, and Leaver processes while incorporating documentation for Conditional Access, Multi-Factor Authentication, and access review procedures.

A detailed architecture diagram is available inside the **Architecture** folder.

## Technologies Used

- Microsoft Azure
- Microsoft Entra ID (Azure Active Directory)
- Identity and Access Management (IAM)
- Role-Based Access Control (RBAC)
- Zero Trust Security Model
- Microsoft Azure Portal
- Microsoft 365 Identity Services
- Security Groups
- Administrative Roles
- GitHub
- Microsoft Excel
- Microsoft Word
- PDF Documentation

## Environment

The lab was deployed using Microsoft Entra ID Free within the Microsoft Azure Portal.

Environment components include:

- Microsoft Entra ID Tenant
- Microsoft Entra ID Users
- Security Groups
- Administrative Roles
- Azure Portal
- Microsoft Azure Cloud Platform

## Implemented Features

### Microsoft Entra ID Tenant

A dedicated Microsoft Entra ID tenant was created to simulate an enterprise identity environment. This tenant serves as the centralized identity provider responsible for authentication, authorization, and user management.

### User Management

Multiple users were created to represent different departments and organizational roles. Each user was assigned appropriate profile information, organizational attributes, department membership, and administrative permissions where required.

Sample users include:

- Muhammad Awais
- Umer
- Asad
- Ahmed
- Bilal

These users simulate real employees working across multiple departments.

### Security Groups

Department-based Security Groups were created to simplify identity management and permission assignment.

Implemented groups include:

- HR
- IT
- Managers
- Contractors

Users were assigned to the appropriate Security Group based on their organizational responsibilities.

### Role-Based Access Control (RBAC)

Role-Based Access Control was implemented by assigning Microsoft Entra administrative roles according to organizational responsibilities.

Configured administrative roles include:

- Global Administrator
- Helpdesk Administrator
- Security Administrator
- Standard User

RBAC ensures users receive only the permissions required to perform their assigned tasks.

### Least Privilege Implementation

The project follows Microsoft's Principle of Least Privilege.

Instead of assigning Global Administrator permissions to every user, administrative access is delegated using specialized built-in Microsoft Entra roles.

Examples include:

- Global Administrator assigned only to the tenant administrator.
- Helpdesk Administrator assigned to the manager responsible for password resets.
- Security Administrator assigned to the IT security user.
- Standard users receive no administrative permissions.

This reduces the attack surface and limits unnecessary privileged access.

### Joiner-Mover-Leaver (JML) Workflow

A complete identity lifecycle management process was documented.

The workflow demonstrates how organizations securely manage employee onboarding, department transfers, and employee offboarding.

The workflow includes:

- New employee provisioning
- Department changes
- Permission reviews
- User deprovisioning
- Group membership updates
- Account removal

### Access Review

An access review document was created to evaluate existing user permissions and determine whether each user still requires assigned access.

The review includes:

- User
- Department
- Assigned Role
- Decision
- Reviewer
- Review Date

This process demonstrates periodic permission validation commonly performed within enterprise organizations.

### Security Policies

Enterprise security policies were documented covering:

- Password Policy
- RBAC Policy
- Least Privilege Policy
- Security Group Policy
- Access Review Policy
- Joiner-Mover-Leaver Policy
- Identity Governance

Conditional Access and Multi-Factor Authentication policies are included as planned implementations due to Microsoft Entra ID Free licensing limitations.

## Zero Trust Principles

The project follows Microsoft's Zero Trust security framework.

Key principles include:

- Verify every identity before granting access.
- Grant minimum permissions required.
- Assume breach and continuously validate trust.
- Secure identities, applications, and resources.
- Continuously monitor user access and permissions.

These principles help reduce unauthorized access while improving organizational security.

## Repository Structure

```text
Microsoft-Entra-IAM-ZeroTrust-Lab/
│
├── Architecture/
│   ├── Architecture.png
│   └── README.md
│
├── Documents/
│   ├── Access_Review.xlsx
│   ├── JML_Workflow.pdf
│   ├── Project_Report.pdf
│   ├── RBAC_Matrix.xlsx
│   ├── Security_Policies.pdf
│   └── README.md
│
├── Screenshots/
│   ├── Users.jpeg
│   ├── Groups.jpeg
│   ├── HR_Group.jpeg
│   ├── IT_Group-members.jpeg
│   ├── Manager_Group.jpeg
│   ├── Contractors_Group.jpeg
│   ├── Roles and administrators.jpeg
│   ├── Assigned_roles.jpeg
│   ├── Assignments.jpeg
│   └── README.md
│
├── LICENSE
└── README.md
```

## Screenshots

The Screenshots folder contains evidence of the implementation, including:

- Microsoft Entra ID Tenant
- Users
- Security Groups
- Group Memberships
- Administrative Roles
- Role Assignments
- RBAC Configuration

These screenshots demonstrate the successful implementation of the IAM environment.

## Learning Outcomes

Through this project, I gained practical experience in:

- Microsoft Entra ID Administration
- Identity and Access Management
- User Provisioning
- Security Group Management
- Role-Based Access Control
- Administrative Role Assignment
- Least Privilege Implementation
- Identity Governance
- Access Reviews
- Joiner-Mover-Leaver Lifecycle
- Enterprise Identity Management
- Zero Trust Security Concepts
- Microsoft Azure Administration

## Limitations

This project was implemented using Microsoft Entra ID Free.

The following enterprise features require Microsoft Entra ID Premium P1/P2 and are documented as future enhancements:

- Conditional Access Policies
- Risk-Based Conditional Access
- Advanced Multi-Factor Authentication Policies
- Privileged Identity Management (PIM)
- Identity Protection
- Automated Access Reviews
- Lifecycle Workflows

## Future Enhancements

Future improvements planned for this project include:

- Enable Microsoft Entra ID Premium P2 Trial
- Configure Conditional Access Policies
- Implement Multi-Factor Authentication
- Integrate Microsoft Defender for Identity
- Integrate Microsoft Sentinel
- Configure Privileged Identity Management
- Implement Identity Protection Policies
- Automate Joiner-Mover-Leaver Workflows
- Configure Lifecycle Workflows
- Implement Passwordless Authentication
- Integrate Enterprise Applications
- Connect Microsoft 365 Services

## Conclusion

This project demonstrates a practical implementation of Identity and Access Management using Microsoft Entra ID within a cloud environment. By combining Security Groups, Role-Based Access Control, administrative role assignments, and documented identity lifecycle management, the project reflects enterprise IAM practices aligned with Microsoft's Zero Trust framework.

The experience gained through this implementation provides practical knowledge of identity administration, access governance, and cloud security concepts that are directly applicable to SOC Analyst, IAM Engineer, Azure Administrator, and Microsoft Security Engineer roles.

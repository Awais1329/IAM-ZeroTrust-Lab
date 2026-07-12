# Architecture

## Microsoft Entra ID IAM & Zero Trust Architecture

The following architecture illustrates the implementation of an Identity and Access Management (IAM) and Zero Trust security lab using Microsoft Entra ID (formerly Azure Active Directory). The environment demonstrates how users, security groups, role-based access control (RBAC), and the Joiner-Mover-Leaver (JML) lifecycle work together to secure enterprise identities and resources.


## Architecture Overview

The architecture is built around **Microsoft Entra ID**, which serves as the central identity provider. All users authenticate through Entra ID before accessing organizational resources. User permissions are managed using **Security Groups** and **Role-Based Access Control (RBAC)** while following the **Least Privilege** principle.

The environment also incorporates **Zero Trust Security**, ensuring that every access request is verified before granting access to organizational resources.

## Components

### 1. Microsoft Entra ID

Microsoft Entra ID acts as the central Identity and Access Management platform responsible for:

- User authentication
- Identity management
- Group management
- Role assignments
- Authorization
- Access control

Every user must authenticate through Microsoft Entra ID before accessing enterprise resources.



### 2. Users

The lab contains multiple users representing different job roles within an organization.

| User | Job Role | Entra Role |
|-------|----------|------------|
| Muhammad Awais | IT Administrator | Global Administrator |
| Umer | Manager | Helpdesk Administrator |
| Asad | IT Engineer | Security Administrator |
| Ahmed | Contractor | Standard User |
| Bilal | HR Employee | Standard User |

Each user is assigned permissions according to their responsibilities.



### 3. Security Groups

To simplify identity management, users are organized into Security Groups.

The groups include:

- HR
- IT
- Managers
- Contractors

Instead of assigning permissions individually, access is granted through group membership.

This approach improves scalability and simplifies administration.



### 4. Role-Based Access Control (RBAC)

The project implements Role-Based Access Control (RBAC) to ensure users receive only the permissions required to perform their job functions.

Implemented roles include:

- Global Administrator
- Security Administrator
- Helpdesk Administrator
- Standard User

RBAC follows the **Least Privilege** principle by preventing unnecessary administrative access.



### 5. Access to Organizational Resources

After authentication and authorization, users can access organizational resources based on their assigned roles.

Example resources include:

- Microsoft 365 Services
- Enterprise Applications
- Azure Portal Resources
- Security & Compliance Services

Access is granted only if the user has sufficient permissions.



### 6. Zero Trust Principles

The architecture follows Microsoft's Zero Trust security model.

The implementation is based on five principles:

- Verify every user identity
- Enforce Least Privilege Access
- Assume Breach
- Secure applications and infrastructure
- Continuously monitor identities and access

These principles help reduce unauthorized access and improve overall security.



### 7. Conditional Access (Planned)

Conditional Access is planned as part of the lab using Microsoft Entra ID Premium P2.

The planned policies include:

- Require Multi-Factor Authentication (MFA)
- Allow access only from trusted locations
- Require compliant devices
- Risk-based access policies
- Application-based access control

> **Note:** Conditional Access was not implemented because Microsoft Entra ID Free does not support this feature. It can be demonstrated using a Microsoft Entra ID Premium P2 trial.



### 8. Access Review

Access Reviews help ensure users maintain only the permissions required for their current responsibilities.

Regular reviews include:

- Reviewing user accounts
- Verifying group memberships
- Checking administrative roles
- Removing unnecessary permissions
- Enforcing Least Privilege



### 9. Joiner-Mover-Leaver (JML) Workflow

The architecture also demonstrates the user lifecycle management process.

#### Joiner

When a new employee joins the organization:

- Create user account
- Add user to the appropriate security group
- Assign required role
- Grant access to resources


#### Mover

When an employee changes departments:

- Remove previous group membership
- Assign new group
- Update RBAC role if required
- Review existing permissions



#### Leaver

When an employee leaves the organization:

- Remove group memberships
- Revoke active sessions
- Delete or disable the account
- Remove all organizational access



## Security Benefits

This architecture provides several security improvements:

- Centralized Identity Management
- Role-Based Access Control (RBAC)
- Least Privilege Access
- Security Group-Based Authorization
- Simplified User Lifecycle Management
- Improved Administrative Control
- Zero Trust Security Implementation
- Better Visibility into User Access



## Technologies Used

- Microsoft Azure
- Microsoft Entra ID
- Identity & Access Management (IAM)
- Zero Trust Security Model
- Role-Based Access Control (RBAC)
- Security Groups
- Microsoft 365
- Azure Portal



## Summary

This project demonstrates how Microsoft Entra ID can be used to implement a secure Identity and Access Management solution based on Zero Trust principles. By combining Security Groups, RBAC, administrative roles, and the Joiner-Mover-Leaver lifecycle, the environment provides centralized identity management while ensuring users receive only the minimum permissions required to perform their responsibilities.

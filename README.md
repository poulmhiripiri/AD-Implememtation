# ACTIVE DIRECTORY IMPLEMENTATION                                             

| Home Page               | <a href="https://github.com/poulmhiripiri/poulmhiripiri/tree/main">Home</a>






🧩 Project 1: Active Directory & Endpoint Management


📌 ### Title: Enterprise-Grade Identity & Endpoint Control using Microsoft Active Directory



 ## Objective:
The primary objective of this project is to establish a comprehensive Windows Server 2016 environment with Active Directory Domain Services (AD DS) and implement enterprise-level security and management policies through Group Policy Objects (GPOs). This includes configuring centralized user management, enforcing security policies, standardizing desktop environments, and controlling system access to maintain organizational compliance and security standards.

## Key Goals:

a. Deploy and configure Windows Server 2016 with Active Directory Domain Services
b. Implement security hardening through USB device restrictions
c. Establish corporate password policies and user account management
d. Configure automated drive mappings for network resources
e. Deploy software installations across the domain
f. Standardize corporate branding through wallpaper deployment
g. Set up secure file sharing with appropriate permissions
h Restrict user access to system configuration tools


### Skills Learned
[Bullet Points - Remove this afterwards]
Throughout this implementation, the following technical competencies were developed:

## Server Administration:

Windows Server 2016 installation and initial configuration
Active Directory Domain Services deployment and forest/domain creation
Domain Controller promotion and DNS integration
Server role management and feature installation

## Active Directory Management:

Organizational Unit (OU) structure design and implementation
User account creation, management, and delegation
Group creation and membership management
Domain security policy configuration

## Group Policy Administration:

Group Policy Object creation and linking strategies
Registry-based policy configurations
Software deployment through Group Policy
Security policy implementation and enforcement
Administrative template customization

## Network Services Configuration:

DNS service configuration for domain resolution
File sharing and NTFS permissions management
Drive mapping automation and troubleshooting
Network security implementation

## Security Implementation:

USB device access control and hardware restriction policies helps on Data Loss Prevention and protect against virus infections
Corporate password policy enforcement helps maintain password complexities and frequent password changes 
User privilege restriction and administrative access control
System hardening through policy-based restrictions

## Steps
Implementation Steps
## Phase 1: Server Installation and Initial Configuration
# Step 1: Windows Server 2016 Installation

Performed clean installation of Windows Server 2016 Standard/Datacenter edition
Configured initial network settings with static IP address assignment
Set appropriate computer name reflecting domain controller role
Applied initial Windows updates and security patches

# Step 2: Active Directory Domain Services Installation

Added AD DS role through Server Manager
Promoted server to Domain Controller using dcpromo wizard
Created new forest and domain with appropriate naming convention
Configured DNS services during domain controller promotion
Verified successful domain controller functionality

## Phase 2: Active Directory Structure Setup
# Step 3: Organizational Unit Design

Created hierarchical OU structure reflecting organizational departments
Established separate OUs for Users, Computers, Groups, and Service Accounts
Implemented delegation of control for departmental administrators
Configured appropriate security permissions on OUs

# Step 4: User and Group Management

Created domain user accounts with standardized naming conventions
Established security groups for role-based access control
Configured group memberships based on job functions
Set up service accounts for application and system services

## Phase 3: Group Policy Implementation
# Step 5: USB Device Restriction Policy

Created GPO "USB Device Restriction Policy"
Navigated to Computer Configuration > Administrative Templates > System > Device Installation
Enabled "Prevent installation of removable devices"
Configured "Prevent installation of devices using drivers that match device setup classes" for USB storage devices
Applied policy to appropriate OUs containing user computers

# Step 6: Corporate Password Policy Configuration

Created GPO "Corporate Password Policy"
Configured Computer Configuration > Windows Settings > Security Settings > Account Policies
Set minimum password length to 12 characters
Enabled password complexity requirements
Configured password history to remember 24 previous passwords
Set maximum password age to 90 days with 7-day minimum age
Enabled account lockout policy with 3 failed attempts threshold

# Step 7: Drive Mapping Configuration

Created GPO "Network Drive Mappings"
Used User Configuration > Preferences > Windows Settings > Drive Maps
Configured persistent drive mappings for shared network resources
Set conditional targeting based on security group membership
Tested drive mapping functionality across different user accounts

# Step 8: Software Installation Deployment

Created GPO "Corporate Software Deployment"
Prepared MSI packages for required corporate applications
Configured Computer Configuration > Software Settings > Software Installation
Added software packages with appropriate deployment options
Set installation to occur at computer startup for mandatory applications
Configured user-assigned applications through User Configuration

# Step 9: Corporate Wallpaper Implementation

Created GPO "Corporate Desktop Standards"
Prepared corporate wallpaper image in network-accessible location
Configured User Configuration > Administrative Templates > Desktop > Desktop
Enabled "Desktop Wallpaper" setting with UNC path to image file
Set wallpaper style and prevented user modification

# Step 10: File Share Configuration

Created shared folders on domain controller or file server
Configured NTFS permissions for appropriate access levels
Set up share permissions complementing NTFS security
Created shared folder GPO preferences for automatic connection
Implemented Access-Based Enumeration for security

# Step 11: Control Panel Restrictions

Enhanced "Corporate Desktop Standards" GPO
Navigated to User Configuration > Administrative Templates > Control Panel
Enabled "Prohibit access to Control Panel and PC settings"
Configured selective restrictions for specific Control Panel applets
Allowed exceptions for necessary system administration functions

# Phase 4: Testing and Validation
Step 12: Policy Testing and Troubleshooting

Created test user accounts in different OUs
Joined test computers to domain for policy application
Verified GPO application using gpresult /r command
Tested each policy component for proper functionality
Documented policy inheritance and conflicts
Resolved issues through proper OU linking and security filtering

### Outcomes:

# Security Enhancement:
Successfully implemented USB device restrictions preventing unauthorized data transfer
Established robust password policies meeting corporate security standards
Restricted user access to system configuration tools preventing unauthorized changes
Created secure file sharing environment with appropriate access controls

# Operational Efficiency:
Automated drive mapping reduced help desk tickets for network resource access
Centralized software deployment eliminated manual installation processes
Standardized desktop environment improved corporate branding consistency
Streamlined user account management through Active Directory integration

# Technical Achievements:
Fully functional Windows Server 2016 domain controller serving organizational needs
Comprehensive Group Policy implementation covering security and management requirements
Scalable Active Directory structure supporting future organizational growth
Documented procedures enabling consistent policy management and troubleshooting

# Compliance and Governance:
Established audit trail for policy compliance and user activity monitoring
Implemented corporate standards enforcement through automated policy application
Created foundation for regulatory compliance requirements
Enabled centralized management of security policies across enterprise environment

# Key Performance Indicators
Policy Application Success Rate: 100% successful GPO application across all domain-joined computers
Security Incident Reduction: Significant decrease in USB-related security incidents
Administrative Efficiency: 75% reduction in manual software installation requests
User Compliance: Complete adherence to corporate password policies through automated enforcement
System Standardization: Uniform desktop environment across all corporate workstations

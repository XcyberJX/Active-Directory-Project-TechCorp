# Home Lab Notes

Documenting my home lab as I build hands-on skills. The company used is for project/labs purpose only and is not an actual company.

## Current Setup

**Hypervisor:** Oracle VirtualBox

**VMs:**
| VM | Role | Notes |
|---|---|---|
| TechCorp DC | Domain Controller (AD DS) | Promoted to a domain controller running Active Directory Domain Services |
| TechCorp Client | Domain-joined client | Connects to TechCorp DC, used to test user auth, GPOs, and domain policies |

## What I'm Practicing

- Creating Active Directory Domain Services from scratch
- Promoting a Windows Server VM to a Domain Controller
- Joining a client machine to the domain
- Creating and managing user accounts / OUs
- Testing login, permissions, and Group Policy behavior from the client side

## Why This Matters for Help Desk

A huge share of tickets involves AD-related issues. Stuff like locked accounts, password resets, permission errors, group policy not applying, or login failures. Building this from scratch gives me an understanding of what's happening "behind the scenes" when I'm troubleshooting these issues on the job.

## Overview
I am a System Administrator for a growing company called TechCorp. The goal is to create an Active Directory structure, create standardized Organizational Units, make users with proper group memberships, and implement basic security. I was able to complete this task in 5 phases with each phase ensuring progress toward the objective. 

---
# Phase 1 (Environment Setup)
## 1. Hypervisor: Oracle VirtualBox
## 2. Virtual Machine 1 will be the Domain Controller
 * Installed Windows Server Evaluation ISO
 * Set a static IP address (192.168.1.10)
 * Promoted the server to a Domain Controller using AD DS
 * Named the Domain "TechCorp.local"
## 3. Virtual Machine 2 will be the Client Workstation
 * Installed the Evaluation ISO for Windows 11 Enterprise
 * Have the machine join the Domain TechCorp.local

--- 
# Phase 2 (Create the OU structure)
I remembered making an OU structure makes it easy to manage and deploy Group Policy.
* <img width="237" height="255" alt="OU Structure" src="https://github.com/user-attachments/assets/ebfbf43b-d33f-4275-8005-3f6888d8b364" />

---
# Phase 3 (Create Users and Security Groups)
## 1. Security Groups (Role-Based Access Control)
 * Created security groups inside "TechCorp/Groups/Security Groups:
    * GRP_HR_Employees: For HR department access.
    * GRP_Finance_Employees: For Finance department access.
    * GRP_IT_Helpdesk: For IT staff members who perform basic admin tasks.
    * <img width="382" height="138" alt="GRPs created" src="https://github.com/user-attachments/assets/a154a263-780f-45c7-9f18-2a0e6c2f2056" />
## 2. User Accounts
 * Created users inside of their respective departments:
    * Jane Doe | jdoe | HR | GRP_HR_Employees
    * John Smith | jsmith | Finance | GRP_Finance_Employees
    * Alexa Rivera | arivera | IT | GRP_IT_Helpdesk
        * Jane Doe: <img width="512" height="457" alt="User Jane Doe" src="https://github.com/user-attachments/assets/c11a1368-a452-4626-891a-d951a1a858a9" />
        * John Smith: <img width="492" height="430" alt="User John Smith" src="https://github.com/user-attachments/assets/ef5fd68d-2eb3-4ba2-b1a0-79af045653be" />
        * Alexa Rivera: <img width="512" height="428" alt="User Alexa Rivera" src="https://github.com/user-attachments/assets/c8102377-0b3b-40d8-b13d-abd197b99770" />
* All users are set to "users must change password at next login"
  
---
# Phase 4 (Key Task to Implement)
## 1. Delegation of Control
* Gave the IT staff permission to reset passwords for users in the HR department
   * <img width="758" height="520" alt="IT department now has permission to reset HR department passwords" src="https://github.com/user-attachments/assets/972d186d-6021-46f8-bf58-def376c07282" />
    * <img width="775" height="495" alt="Clicking finish completes the wizard" src="https://github.com/user-attachments/assets/e4edaaa5-85a6-45b5-8243-0c41a40f6018" />
## 2. User Template
* Created a user template named _Template_HR
    * <img width="702" height="425" alt="Template created for HR employees" src="https://github.com/user-attachments/assets/171f703c-7add-4e1f-b7c7-41bbd49af196" />
* Configured the default settings (Department name, Company, Login restrictions, and job title)
    * <img width="455" height="585" alt="Organization - credentials set for template" src="https://github.com/user-attachments/assets/fc4ef087-06b2-4766-bc3c-b77e07c60bf3" />
    * <img width="378" height="132" alt="Account options - set for template" src="https://github.com/user-attachments/assets/6a86bd7e-c58f-4d36-8b34-346e225f6474" />
    * <img width="525" height="321" alt="Login hours - set for template" src="https://github.com/user-attachments/assets/d3eb3ac2-28cb-4ccb-8e4e-e32a8f3b3b28" />
* Can copy this template when creating HR users to save you time and reduce human errors
## 3. Multiuser creation using PowerShell
* Created an csv(Comma Separated Values) file saved as users.csv inside of a notepad with all of the stored code
    * <img width="1227" height="815" alt="CSV file creation" src="https://github.com/user-attachments/assets/a6002b19-975b-404a-bc3a-a5816578d365" />
* Ran PowerShell ISE as an administrator and wrote the following code:
    * <img width="653" height="380" alt="The script used in PowerShell " src="https://github.com/user-attachments/assets/4cb5f44e-cc69-4e90-ad82-fd32d57ca31c" />
      

# WORK IN PROGRESS...
   
    
   
   
 


---
*Part of my IT portfolio — see my [profile README](../..) for the full picture.*

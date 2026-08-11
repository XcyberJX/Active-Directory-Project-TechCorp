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
1. Hypervisor: Oracle VirtualBox
2. Virtual Machine 1 will be the Domain Controller
    * Installed Windows Server Evaluation ISO
    * Set a static IP address (192.168.1.10)
    * Promoted the server to a Domain Controller using AD DS
       * New Forest: TechCorp.local
       * Functional Level: Windows 2022
3. Rebooted the VM and confirmed DC promotion was a success

# WORK IN PROGRESS...
   
    
   
   
 


---
*Part of my IT portfolio — see my [profile README](../..) for the full picture.*

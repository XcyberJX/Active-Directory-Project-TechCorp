# Home Lab Notes

Documenting my home lab as I build hands-on skills.

## Current Setup

**Hypervisor:** Oracle VirtualBox

**VMs:**
| VM | Role | Notes |
|---|---|---|
| TechCorp DC | Domain Controller (AD DS) | Promoted to a domain controller running Active Directory Domain Services |
| TechCorp Client | Domain-joined client | Connects to TechCorp DC, used to test user auth, GPOs, and domain policies |

## What I'm Practicing

- Standing up Active Directory Domain Services from scratch
- Promoting a Windows Server VM to a Domain Controller
- Joining a client machine to the domain
- Creating and managing user accounts / OUs
- Testing login, permissions, and Group Policy behavior from the client side

## Why This Matters for Help Desk

A huge share of tickets involve AD-related issues. Stuff like locked accounts, password resets, permission errors, group policy not applying, or login failures. Building this from scratch gives me an understanding of what's happening "behind the scenes" when I'm troubleshooting these issues on the job.

MORE TO COME...
---
*Part of my IT portfolio — see my [profile README](../..) for the full picture.*

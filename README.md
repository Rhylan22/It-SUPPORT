# IT Knowledge Base & Standard Operating Procedures

## Overview

This project documents a collection of SOPs and knowledge base articles I built to simulate the kind of internal IT documentation used in enterprise help desk environments. Good documentation reduces repeat tickets, speeds up resolution time, and helps onboard new technicians faster.

---

## SOP Index

| SOP # | Title | Category |
|---|---|---|
| SOP-001 | Password Reset Procedure | Account Management |
| SOP-002 | Account Lockout Resolution | Account Management |
| SOP-003 | New Employee Onboarding Checklist | Onboarding |
| SOP-004 | Employee Offboarding Checklist | Offboarding |
| SOP-005 | Printer Offline Troubleshooting | Hardware |
| SOP-006 | VPN Connection Troubleshooting | Network |
| SOP-007 | Ticket Escalation Guidelines | Help Desk Process |

---

## SOP-001 — Password Reset Procedure

**Category:** Account Management
**Applies To:** All domain users
**Last Updated:** 2025

### Steps
1. Verify caller identity — confirm full name, department, and employee ID
2. Open Active Directory Users & Computers
3. Search for user account by name or username
4. Right-click account → Reset Password
5. Set temporary password meeting complexity requirements
6. Check "User must change password at next logon"
7. Confirm with user they can log in successfully
8. Log ticket as resolved with resolution notes

**Notes:** Never reset a password without identity verification. Document every reset in the ticketing system.

---

## SOP-002 — Account Lockout Resolution

**Category:** Account Management
**Applies To:** All domain users

### Steps
1. Verify caller identity
2. Open Active Directory Users & Computers
3. Search for user account
4. Check account status — confirm locked (lock icon visible)
5. Right-click → Properties → Account tab → Unlock Account
6. Ask user to attempt login
7. If lockout repeats — investigate cause (bad cached credentials, mobile device, mapped drive)
8. Document resolution in ticket

---

## SOP-003 — New Employee Onboarding Checklist

**Category:** Onboarding
**Trigger:** HR submits new hire request minimum 3 business days before start date

### Checklist
- [ ] Create Active Directory user account in correct OU
- [ ] Set username following naming convention (first.last)
- [ ] Assign to appropriate security groups and distribution lists
- [ ] Configure Microsoft 365 account and mailbox
- [ ] Set up workstation with standard software image
- [ ] Install role-specific software if required
- [ ] Configure email signature template
- [ ] Test login with user present on Day 1
- [ ] Provide user with credentials and IT contact info
- [ ] Log equipment assigned in IT inventory system
- [ ] Close onboarding ticket with all steps documented

---

## SOP-004 — Employee Offboarding Checklist

**Category:** Offboarding
**Trigger:** HR notifies IT of departure minimum 24 hours in advance (immediate for terminations)

### Checklist
- [ ] Disable Active Directory account immediately (do NOT delete)
- [ ] Remove from all security groups and distribution lists
- [ ] Forward email to manager or designated recipient
- [ ] Revoke VPN and remote access
- [ ] Disable Microsoft 365 license (retain mailbox per retention policy)
- [ ] Retrieve company equipment and log return in inventory
- [ ] Change passwords on any shared accounts the user had access to
- [ ] Document all actions taken in offboarding ticket

---

## SOP-005 — Printer Offline Troubleshooting

**Category:** Hardware
**Common Cause:** Network issue, print spooler crash, IP change

### Steps
1. Confirm printer shows offline in Windows (Settings → Printers)
2. Check physical connection — power on, network cable or Wi-Fi connected
3. Print configuration page directly from printer to confirm IP
4. Compare IP to what's configured in Windows — update if changed
5. Restart Print Spooler service:
   - Open Services.msc → Print Spooler → Restart
6. Clear print queue if stuck jobs present
7. Test print
8. If unresolved — check printer manufacturer portal for firmware or driver updates

---

## SOP-006 — VPN Connection Troubleshooting

**Category:** Network

### Steps
1. Confirm VPN client is installed and up to date
2. Verify user credentials are correct
3. Check if internet connection is active without VPN
4. Disable third-party firewall or antivirus temporarily to test
5. Flush DNS: `ipconfig /flushdns`
6. Restart VPN client
7. If still failing — collect error code and escalate to L2 with full notes

---

## SOP-007 — Ticket Escalation Guidelines

**Category:** Help Desk Process

### When to Escalate to Level 2
- Issue cannot be resolved within 30 minutes at Tier 1
- Requires server-side changes beyond AD account management
- Suspected hardware failure (motherboard, RAM, storage)
- Security incident or data breach suspected
- Issue affects multiple users simultaneously

### Escalation Notes Must Include
- User name, department, contact info
- Detailed description of issue and symptoms
- All troubleshooting steps already attempted
- Any error codes or screenshots captured
- Priority level and business impact

**Never escalate without complete notes.** Incomplete escalations slow resolution and frustrate users.

---

## Skills Demonstrated

`IT Documentation` `SOP Writing` `Knowledge Base` `Onboarding` `Offboarding` `Account Management` `Escalation Process` `Help Desk Process` `Ticket Management` `Active Directory` `Printer Support` `VPN Troubleshooting`

# IT Support Portfolio · Martin Mandev

Troubleshooting tutorials, knowledge base articles and a write-up of my home lab, built while preparing for IT support and service desk roles. Every example comes from systems I set up, broke on purpose and fixed myself.

## Home lab

A small company network running in VirtualBox on my own PC:

| Component | Details |
|---|---|
| **Domain controller** | Windows Server 2025 · Active Directory (`mydomain.com`) · DNS · DHCP · NAT routing |
| **Client** | Windows 11 Pro, joined to the domain, receiving its address from the DC |
| **Active Directory** | OUs per department, security groups, a shared Sales folder with NTFS permissions, a drive mapped by Group Policy, an account lockout policy |
| **Ticketing** | Jira Service Management: tickets worked end to end, from first reply to resolution |
| **Linux** | Ubuntu (WSL): permissions, users and groups, services, logs; OverTheWire Bandit levels 0–15 |
| **Web hosting** | a local WordPress site, broken and repaired four different ways |

**Tickets worked in the lab:** password resets, account lockouts traced to their source (Event ID 4740), new starters and leavers, "access denied" on shared folders, a team-wide printer outage, DNS and IP misconfigurations. A full new-starter setup, including groups and a mapped drive, takes about three minutes.

## Tutorials

In-depth guides for new support staff, explaining why each step matters:

1. [My internet doesn't work: a beginner's guide to finding out why](tutorials/01-internet-not-working.md)
2. [Password reset and account unlock in Active Directory](tutorials/02-password-reset-and-unlock.md)
3. [Four common WordPress errors and how to fix them](tutorials/03-wordpress-errors.md)
4. ["Access denied" on a shared folder: permissions and mapped drives](tutorials/04-shared-folder-access-denied.md)

## Knowledge base articles

Short, step-by-step procedures, written the way a service desk would use them:

- [Account locked out](kb-articles/account-locked-out.md) · *for the service desk*
- [Websites won't load on your PC](kb-articles/websites-wont-load.md) · *for users*
- [Print jobs stuck in the queue](kb-articles/print-jobs-stuck.md) · *for the service desk*

## Certifications

- **Google IT Support Professional Certificate** · Google / Coursera, 2020

Next
Azure Fundamentals (AZ-900) · ITIL basics

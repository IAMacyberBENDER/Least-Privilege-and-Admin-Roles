# Project Title
Least Privilege and Admin Roles

## Project Overview

This project builds on the Northwind Services Entra ID tenant from the Directory Foundation Lab. The goal is to assign administrative roles based on the principle of least privilege, giving each administrator only the permissions they need to perform their responsibilities while limiting unnecessary access and security risk.

## Business Scenario

Northwind Services is a small company with 16 employees across Executive, IT, Finance, Sales, and HR, along with two contractors who have fixed end dates. As the company manages its users and Entra ID environment, it needs to determine who should be able to perform administrative tasks such as resetting passwords, creating user accounts and groups, managing access, and investigating sign-in activity. The goal is to give the appropriate employees the smallest administrative role necessary to perform their jobs while avoiding excessive privileges that could create security and audit risks.

## Tools Used

- Microsoft Entra ID

## What I Built

The main sections of work.

## Screenshots

I signed in as the Help Desk Technician and successfully
reset a regular user's password. I then attempted to create
a new user, but the action was blocked because the
account did not have the required permissions. This
confirmed that the assigned role allows password-reset
support without granting broader user-management access.

The screenshot shows a blocked action and demonstrates that least privilege is working as intended. <img width="1169" height="1603" alt="IMG_5347" src="https://github.com/user-attachments/assets/0d1ba59c-a8ae-45a9-8354-485f98575186" />

## Security Lessons Learned

In this lab, I learned that least privilege is not about distrusting the people who use the system. It is about limiting what can happen if an account is compromised. Every account is a possible entry point, so I focused on giving each Northwind administrator only the permissions needed for their job.

For example, the Help Desk Tech does not need a broad administrative role just to reset a regular employee's password. Giving them a narrower role limits the potential impact if that account is compromised. In contrast, assigning Global Administrator would provide far more access than the Help Desk Tech needs and would create much greater risk if the account were phished.

I also learned that the required permission depends on the target, not just the action. "Reset a password" sounds like one task, but the required privilege changes depending on whose password is being reset. Resetting a regular employee's password is different from resetting the password of an administrator because changing an administrator's authentication could provide a path to greater privileges.

## Future Improvements
Assign roles to role-assignable groups instead of individuals, which needs P1

Use Privileged Identity Management so admin rights are activated when needed rather than held permanently, which needs P2

Scope roles to administrative units so a regional admin only manages their own users, which needs P1 for the scoped admin

Run periodic access reviews on who holds administrative roles, which needs Microsoft Entra ID Governance or the Entra Suite

Add phishing-resistant credentials to the emergency access accounts

Alert on any emergency access account sign-in

                 

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

![Description of the image](screenshots/practice-shot.png)

## Security Lessons Learned

What this taught me about why it matters.

## Future Improvements
Assign roles to role-assignable groups instead of individuals, which needs P1



Use Privileged Identity Management so admin rights are activated when needed rather than held permanently, which needs P2



Scope roles to administrative units so a regional admin only manages their own users, which needs P1 for the scoped admin



Run periodic access reviews on who holds administrative roles, which needs Microsoft Entra ID Governance or the Entra Suite



Add phishing-resistant credentials to the emergency access accounts



Alert on any emergency access account sign-in

What I would do next, honestly.

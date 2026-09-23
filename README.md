# Project Title
Least Privilege and Admin Roles

## Project Overview

This project builds on the Northwind Services Entra ID tenant from the Directory Foundation Lab. The goal is to assign administrative roles based on the principle of least privilege, giving each administrator only the permissions they need to perform their responsibilities while limiting unnecessary access and security risk.

## Business Scenario

Northwind Services is a small company with 16 employees across Executive, IT, Finance, Sales, and HR, along with two contractors who have fixed end dates. As the company manages its users and Entra ID environment, it needs to determine who should be able to perform administrative tasks such as resetting passwords, creating user accounts and groups, managing access, and investigating sign-in activity. The goal is to give the appropriate employees the smallest administrative role necessary to perform their jobs while avoiding excessive privileges that could create security and audit risks.

## Tools Used

- Microsoft Entra ID

## What I Built

For this project I continued working with the Northwind Services Microsoft Entra ID tenant I created in part 1 and focused on building a least-privilege administrative structure.

                                  Role Review and Ticket Exercise

I first reviewed the available built-in Entra administrative roles to understand the different levels of administrative access and identify which roles matched the tasks Northwind needed. I then completed a six-ticket exercise where I made my own initial role selections before comparing them with Microsoft's least-privileged role recommendations. This helped me identify where my assumptions were too broad, especially around password resets, user management, and reading reports.

                            Administrative Role Assignments

Based on the results of the ticket exercise, I assigned the **Password Administrator** role to the Help Desk Tech because they only need to reset passwords for regular employees. I assigned the **User Administrator** role to the Systems Administrator because they need to create and manage regular user accounts. I assigned the **Reports Reader** role to the IT Manager because their responsibility is to review sign-in and audit information rather than make administrative changes.

The remaining Northwind employees were intentionally left without administrative roles because their job responsibilities do not require directory administration. This keeps administrative permissions limited to the employees who actually need them.

                                            Permission Testing

I tested the Help Desk Tech account in a separate browser session by performing an action it was allowed to perform and then attempting an administrative action it was not allowed to perform. The blocked action provided evidence that the permission boundary was working as intended and that the Help Desk Tech could not perform tasks outside the scope of the assigned role.

                                   Emergency Access and Security Gaps

I also created two emergency access accounts and documented the security gaps that would still need to be addressed in a production environment. This included documenting the need for stronger authentication, appropriate Conditional Access exclusions, and monitoring for emergency account activity.


                               Global Administrator and Privileged Role Review

After completing the role assignments, I reviewed the tenant's Global Administrator count and total privileged role assignments and compared them with Microsoft's recommended limits. I started with one Global Administrator and ended with three after creating the two emergency access accounts, keeping the tenant within Microsoft's recommendation of fewer than five Global Administrators.

I also reviewed the PRIVILEGED label on the roles I assigned to understand which assignments could affect authentication or provide a path to greater access and which role was limited to read-only visibility. I performed these checks to make sure the Northwind tenant stayed within Microsoft's recommended best practices for both Global Administrator assignments and the use of privileged roles.


                                        Audit and Documentation

Finally, I reviewed the Entra audit logs to verify that the administrative role assignments were recorded. I captured screenshots showing the role assignments, blocked action, privileged role information, and audit trail. I documented the role decisions, ticket exercise, testing results, emergency access accounts, audit evidence, and least-privilege reasoning in the project documentation.

The result is a working Entra ID role structure that demonstrates how administrative access can be intentionally limited, tested, and monitored instead of giving users broad permissions simply because they need to perform one administrative task.


## Screenshot
***The screenshot shows a blocked action and demonstrates that least privilege is working as intended.**

I signed in as the Help Desk Technician and successfully
reset a regular user's password. I then attempted to create
a new user, but the action was blocked because the
account did not have the required permissions. This
confirmed that the assigned role allows password-reset
support without granting broader user-management access.

                                                         [View blocked action screenshot](screenshots/one-blocked-action.jpg)



  


**Screenshot of the role list with the privilege label visible .**


This screenshot shows five privileged role assignments in the tenant. Four of these assignments were created as part of the Northwind project, while one was the default Global Administrator assignment created when the tenant was initially set up and was not part of the project.

Microsoft recommends maintaining two or more emergency access accounts for emergency or “break-glass” scenarios. The tenant also remains below Microsoft’s recommendation of fewer than 10 privileged role assignments


This screenshot shows that the selected administrative role was successfully assigned to a Northwind team member. The assignment reflects the least-privilege approach used in this step, giving the user the permissions needed to perform their responsibilities without assigning a broader role than necessary.





**Screenshot of a complete role administrative assignment**

This screenshot shows the Help Desk Tech being assigned the Password Administrator role. The Help Desk Tech’s responsibility is to reset passwords for regular staff, so I assigned the narrowest administrative role that provides the permissions needed to perform that task. This demonstrates the principle of least privilege by giving the account only the access required for its responsibilities without assigning a broader role than necessary.



## Security Lessons Learned

In this Project, I learned that least privilege is not about distrusting the people who use the system. It is about limiting what can happen if an account is compromised. Every account is a possible entry point, so I focused on giving each Northwind administrator only the permissions needed for their job.

For example, the Help Desk Tech does not need a broad administrative role just to reset a regular employee's password. Giving them a narrower role limits the potential impact if that account is compromised. In contrast, assigning Global Administrator would provide far more access than the Help Desk Tech needs and would create much greater risk if the account were phished.

I also learned that the required permission depends on the target, not just the action. "Reset a password" sounds like one task, but the required privilege changes depending on whose password is being reset. Resetting a regular employee's password is different from resetting the password of an administrator because changing an administrator's authentication could provide a path to greater privileges.

## Future Improvements
Assign roles to role-assignable groups instead of individuals, which needs P1

Use Privileged Identity Management so admin rights are activated when needed rather than held permanently, which needs P2

Scope roles to administrative units so a regional admin only manages their own users, which needs P1 for the scoped admin

Run periodic access reviews on who holds administrative roles, which needs Microsoft Entra ID Governance or the Entra Suite

Add phishing-resistant credentials to the emergency access accounts

Alert on any emergency access account sign-in

                 

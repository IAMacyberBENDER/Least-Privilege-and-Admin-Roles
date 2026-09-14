Here are six tickets that land at a real help desk. For each ticket, I identified the smallest Microsoft Entra ID administrative role I believe is needed to complete the Job. 

     1.Reset the password for a salesperson who is locked out.
     2.Create an account for a new hire starting Monday.
     3.Create a new security group for the Finance team.
     4.Give the systems admin the ability to create user accounts.
     5.Look at sign-in logs to investigate a suspicious login.
     6.Reset the password for another administrator.

                                  Ticket Exercise

Before checking Microsoft's documentation, I made my best guess for the smallest role that could complete each ticket. After comparing my answers with Microsoft's Least privileged roles by task reference, I found that some of my assumptions were too broad.

1. Reset the password for a salesperson who is locked out

My initial guess: Helpdesk Administrator

Correct answer: Password Administrator

What I got wrong: I assumed Helpdesk Administrator because this sounds like a normal help desk password-reset task. However, Microsoft lists Password Administrator as the least privileged role for resetting the password of a non-administrator. Helpdesk Administrator can also reset passwords for non-administrators, but it is not the least-privileged answer for this specific task.

2. Create an account for a new hire starting Monday

My initial guess: Global Administrator

Correct answer: User Administrator

What I got wrong: I assumed creating a new user account required a broad administrative role. It does not. Microsoft lists User Administrator as the least privileged role for creating users. Giving someone Global Administrator would provide far more access than they need for this task.

3. Create a new security group for the Finance team

My initial guess: User Administrator

Correct answer: Groups Administrator

What I got wrong: I assumed user and group management were basically the same thing. They are not. Microsoft specifically lists Groups Administrator as the least privileged role for creating a group. User Administrator can also perform the task, but it has broader responsibilities than necessary.

4. Give the systems admin the ability to create user accounts

My initial guess: User Administrator

Correct answer: Privileged Role Administrator

What I got wrong: I focused on the permission being granted instead of the action being performed. The task is not simply creating a user. It is assigning an administrative role to another person. Microsoft lists Privileged Role Administrator as the least privileged role for managing role assignments.

This was an important distinction because assigning administrative roles is itself a privileged action.

5. Look at sign-in logs to investigate a suspicious login.

Initial guess: Reports Reader
Correct answer: Reports Reader

Why: Reports Reader provides read-only access to reporting data, allowing an administrator to view sign-in and audit information without giving them unnecessary permissions to modify users, groups, or other resources.

6. Reset the password for another administrator

My initial guess: Helpdesk Administrator
Correct answer: It depends on the administrator being targeted.

Microsoft separates this into different levels:

Limited administrator: User Administrator
Privileged administrator: Privileged Authentication Administrator



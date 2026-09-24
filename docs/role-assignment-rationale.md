***Each of the three assignments: the person, the role, what they need to do, and specifically why the next role up was too much***
  
  
  
Aiden Cross —  Help Desk Tech — Password Administrator

The Help Desk Tech will reset passwords for regular employees who do not have administrative roles. In this scenario,    Password Administrator is the appropriate role because it provides the permissions needed for the task without giving the Help Desk Tech broader administrative access. This follows the principle of least privilege because the required role depends on the target. If the target were a user with an administrative role, a different and more privileged role would be required.



Marisol Vega — Systems Administrator — User Administrator

I assigned the User Administrator role to the Systems Administrator because their responsibilities at Northwind include creating and managing normal user accounts. A broader administrative role, such as Privileged Role Administrator, would provide permissions beyond what is necessary for normal user management. Assigning User Administrator keeps the Systems Administrator's access focused on the tasks they are responsible for and follows the principle of least privilege.




Daniel Brook — IT Manager — Reports Reader

The IT Manager needs to review sign-in logs, audit information, and reports so they can monitor activity in the environment and investigate potential issues. The Reports Reader role provides read-only visibility into this information without giving the IT Manager the ability to make administrative changes. This supports the principle of least privilege because the manager needs visibility for oversight, not the ability to directly manage users, groups, or security settings. A broader administrative role would provide more access than necessary because the IT Manager's responsibility in this lab is primarily monitoring, reviewing, and investigating activity.


 ***Roles Assigned to the Remaining Employees***
 
The remaining Northwind employees are not assigned Entra ID administrative roles because their job responsibilities do not require them to manage the identity environment. They can still access the applications, files, and other resources they need to perform their jobs through normal user access and group-based permissions.

Administrative roles are limited to employees who need to perform specific administrative tasks, such as managing users, groups, passwords, or reports. Keeping regular employees without administrative roles follows the principle of least privilege by giving them only the access they need to do their jobs and avoiding unnecessary administrative permissions.


#***Why Twelve Employees Have No Admin Role***

The remaining 12 Northwind employees were not assigned Microsoft Entra administrative roles because their normal job responsibilities do not require them to manage the directory. They still receive the access they need to perform their jobs through normal user accounts, groups, and resource permissions. Administrative roles are reserved for employees whose responsibilities require directory-level administrative actions. This follows the principle of least privilege by avoiding unnecessary elevated permissions and reducing the number of accounts that can make administrative changes to the tenant.

 
***The one thing from the ticket exercise that most surprised me***
                             
The thing that surprised me most was that the role needed to reset a password depends on who the target user is.         At first, I thought resetting any user's password would require the same role. I learned that resetting a regular employee's password can be handled with the Password Administrator role, while resetting the password of an administrator may require a more privileged role. This showed me that least privilege depends not only on the task being performed, but also on the target of that task.


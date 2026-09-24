Break-Glass Emergency Access Accounts

                                  What I Built

I created two dedicated emergency access accounts for the Northwind Services Entra ID tenant:

  -EmergencyAccess1@IAMChris.onmicrosoft.com

  -EmergencyAccess2@IAMChris.onmicrosoft.com

Both accounts are cloud-only and have the Global Administrator role assigned permanently. Neither account is named after or tied to an individual employee.

These accounts are intended for emergency tenant recovery if normal administrative access becomes unavailable.

Privileged Account Count

Before creating the emergency accounts, the tenant had one Global Administrator account. (This account is not part of project)

After creating the two emergency accounts, the tenant has three Global Administrator accounts:

My administrative account (Is not part of project, created by default) 

Emergency Access 1

Emergency Access 2

The emergency accounts are not included in the Northwind employee or contractor headcount because they exist only for tenant recovery.




                                       Gaps list 


 -Phishing-resistant authentication such as FIDO2/passkeys or certificate-based authentication has not been configured.
 
 -The emergency accounts have not been connected to my personal phone or Authenticator account.
 
 -Conditional Access policies for emergency access accounts have not yet been configured.
 
 -Automated monitoring and alerting for emergency-account sign-ins has not yet been implemented.
 
 -A formal process for securely storing and accessing the emergency credentials has not yet been implemented.


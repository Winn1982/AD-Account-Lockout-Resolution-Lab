# AD-Account-Lockout-Resolution-Lab
## Objective
Simulated a real-world helpdesk scenario involving a locked Active Directory user account in a Windows domain environment. Practiced diagnosing account lockout conditions, resetting credentials, unlocking the account, and validating successful authentication on a domain-joined Windows 10 client machine.

 ## Lab Environment

Windows Server 2022 (Domain Controller)

Active Directory Domain Services (AD DS)

Windows 10 (Domain-joined VM)

Oracle VirtualBox

 ## Scenario

A domain user account became locked due to multiple failed login attempts. The user reported being unable to sign in.

 ## Troubleshooting & Resolution Steps

Accessed Active Directory Users and Computers (ADUC)

Navigated to affected user account

Confirmed account lockout status under Account tab

Unlocked the account

Reset user password

Enforced “User must change password at next logon”

Tested authentication on Windows 10 domain client

Verified successful login and password change

 ## Skills Demonstrated

Active Directory user account management

Account lockout troubleshooting

Password reset procedures

Domain authentication validation

Helpdesk-style incident resolution workflow

IAM fundamentals (identity lifecycle + access control)

 ## Outcome

Successfully restored user access by unlocking the account and enforcing a secure password reset process, validating end-to-end domain authentication functionality.


## Troubleshooting Workflow
User "jdoe" entered his passwrong wrong three times and was prompted that his account was locked out and to contact his administrator. 

<p align="center"><img width="400" height="400" alt="Jdoe Gets locked out of account" src="https://github.com/user-attachments/assets/94b31746-b4c1-4101-a907-35dcf343ae9e" />

Administrator logs in and navigates to Active Directory Users and Computers.

<p align="center"><img width="400" height="400" alt="Admin logs in and goes to Active Directory Users and Computers" src="https://github.com/user-attachments/assets/1cc6ca7f-f350-4ebd-b814-a6a60a99674b" />

Administrator navigates to _EMPLOYEES and finds the user John Doe.

<p align="center"><img width="400" height="400" alt="In AD users and computers, navigate to _EMPLOYEES and locate user John Doe" src="https://github.com/user-attachments/assets/e2655d33-5e64-450d-84eb-3cfe171e30b1" />

Administrator accesses John Doe's properties and clicks on "Account" and sees that the account is currently locked out on the Active Directory Domain Controller. 

<p align="center"><img width="400" height="400" alt="Go to account tab for john doe and see that he is locked out" src="https://github.com/user-attachments/assets/743e30fa-3772-4925-9b6f-5a57cb268b8a" />

Administrator checked the box next to "Unlock Account" and checked the box that the user must change their password at the next login.

<p align="center"><img width="400" height="400" alt="Click unlock and select user must change password at next login" src="https://github.com/user-attachments/assets/fce9a969-8434-40d5-8b0c-da69cd6fce81" />

User "jdoe" enters his password and is prompted to change his password. 

<p align="center"><img width="400" height="400" alt="Jdoe entered password and now has to change password" src="https://github.com/user-attachments/assets/1b380321-fb18-4263-8b6b-8ec98435922f" />

User "jdoe" was able to login in to the Windows 10 Virtual Machine successfully, this was confirmed to be his account by typing "whoami" in Powershell and it shows he was logged into the Domain Controller. 

<p align="center"><img width="400" height="400" alt="jdoe was able to login successfully" src="https://github.com/user-attachments/assets/71a005d9-0eb9-4831-b7e5-3a94d8ea6483" />







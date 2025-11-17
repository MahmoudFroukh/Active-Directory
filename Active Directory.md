## Active Directory

### Network Diagram

<img width="1071" height="681" alt="Active Directory drawio" src="https://github.com/user-attachments/assets/ce3c4524-33a8-4dd5-b120-8e19542c22cc" />

### Creating a new organizational unit and adding a user

<img width="1105" height="654" alt="New OU and User" src="https://github.com/user-attachments/assets/aba1ac21-f5c1-4eb2-a9f5-e80ea7f47cac" />

- We will create a new OU and call it `_ADMINS`.
- Now we can create a new user in this `Organizational Unit`.
- Then we add this user to the `Domain Admins`.
- Now we can sign in with this user instead of the default Admin account

### Creating Users Using Powershell

<img width="897" height="892" alt="PowerShell Script" src="https://github.com/user-attachments/assets/45bd70fe-de82-4320-a0d8-9efe1dd9b1d2" />

- Using this powershell script, we can create about 1000 users.
- Since this is a lab, we will also run the command `Set-ExecutionPolicy Unrestricted`
- This will let us run powershell commands.

<img width="965" height="407" alt="Users being created" src="https://github.com/user-attachments/assets/ba7c13ad-de99-44b3-a466-69091f43d2de" />

- Make sure we are in the correct directory.
- Now we can run it.

<img width="915" height="671" alt="Users Created" src="https://github.com/user-attachments/assets/38b3945d-0661-4d4e-90cd-a26eb563b0be" />

- Now when we go back to `Active Directory Users and Computer` we see all the new users that were created.

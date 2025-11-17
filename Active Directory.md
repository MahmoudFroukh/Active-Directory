## Active Directory

### Summary

This lab simulates a small Active Directory environment using VMWware with a Domain Controller providing DHCP, DNS, and NAT services to one internal client. Two network segments are used: An external network (home router) for internet access, and an internal isolated network for Active Directory services.

### Network Diagram

<img width="1071" height="681" alt="Active Directory drawio" src="https://github.com/user-attachments/assets/ce3c4524-33a8-4dd5-b120-8e19542c22cc" />

- The Domain Controller has two NICs: one connected to the home network for internet access, and one on an internal VMware network with a static IP `172.16.0.1` used for all AD services.
- The interanl network uses the `172.16.0.x` range, where clients receive IP addressing `172.16.0.100-200` from the DC's DHCP scope.
- The Windows 11 client connects only to the internal VMware network and relies on the DC for DHCP, DNS, and domain joining.
- This setup isolates lab traffic from the home network while still allowing internal machines to reach the internet through the DC's NAT, creating a realistic and safe AD practice environment.

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
- Now we can run the script.

<img width="915" height="671" alt="Users Created" src="https://github.com/user-attachments/assets/38b3945d-0661-4d4e-90cd-a26eb563b0be" />

- When we go back to `Active Directory Users and Computers` we see all the new users that were created.

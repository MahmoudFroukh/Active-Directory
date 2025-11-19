## Active Directory

### Summary

This lab simulates a small Active Directory environment using VMware with a Domain Controller providing DHCP, DNS, and NAT services to one internal client. Two network segments are used: An external network (home router) for internet access, and an internal isolated network for Active Directory services.

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

### Setting up our client computer

<img width="1025" height="622" alt="Client1" src="https://github.com/user-attachments/assets/62b071cf-bbba-4c2c-9819-d76f9e4ad2d0" />

- Here we can see that `CLIENT1` now has an IP address and a default gatway.
- Now we can ping `mydomain.com`.

<img width="320" height="387" alt="Joining the domain" src="https://github.com/user-attachments/assets/0f38f5c1-5ae7-407f-b4fe-634c1d8a6f3d" />

- Here we are joining the domain.

<img width="709" height="429" alt="Member of the domain" src="https://github.com/user-attachments/assets/6bbb384f-4a37-4de0-b5d2-49b872a97563" />
<img width="994" height="394" alt="Lease" src="https://github.com/user-attachments/assets/add4ae47-2fa8-423a-bae6-caaa3d2371f0" />

- Now we can see that `CLIENT1` is a member of computers and our DHCP server gave it an address.

### Resetting a Users Password From a Lockout

<img width="408" height="535" alt="User account lockout" src="https://github.com/user-attachments/assets/aa0a5b06-85c1-4cd3-8a35-d2d67cef021d" />

- We find the user first using the `find` function.
- Then we `Unlock` the account.

### Creating a Group Policy Object

<img width="1414" height="610" alt="Creating a GPO" src="https://github.com/user-attachments/assets/98ff93da-1fcf-44de-aba2-91504e5ea373" />

- Here I created a GPO and called it `Screen Saver`
- This will enable the screensaver and make it password protected.

<img width="1413" height="442" alt="Linking a GPO" src="https://github.com/user-attachments/assets/2816de91-a99d-4d63-adda-c89370174fd8" />

- Now I have it linked to the `Accounting` OU.
- This is a great GPO for the Accounting team as they will be dealing with the money of the company.



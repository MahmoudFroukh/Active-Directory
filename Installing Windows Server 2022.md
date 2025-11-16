## Steps

### Step 1 - What we need:

- We will need to install a hypervisor.
- I chose to use Vmware workstation pro.
- We will also need a Windows Server 2022 iso file.

### Step 2 - Creating the virtual machine:

<img width="423" height="427" alt="Creating the machine2" src="https://github.com/user-attachments/assets/bdea2d09-50e8-4d0a-bc0e-c57a8363918b" />

- We will choose the recommended option.

<img width="422" height="427" alt="Choosing the iso" src="https://github.com/user-attachments/assets/da5592cf-db21-4960-9f14-c1986bab82b5" />

- Then we choose the Windows Server 2022 iso file.

<img width="423" height="426" alt="Setting up the localadmin account" src="https://github.com/user-attachments/assets/35d4caec-3a08-4227-87bf-fc8c594d2889" />

- Leave the product key field empty.
- Choose Windows Server 2022 Datacenter.
- Now we set up a localadmin account.

<img width="423" height="425" alt="Storage options" src="https://github.com/user-attachments/assets/f7b36d15-759c-4530-8ef7-b1986afc226f" />

- Set the amount of storage you want.
- Keep the default value of splitting the virtual disk into multiple files.

<img width="427" height="429" alt="Settings" src="https://github.com/user-attachments/assets/33518952-1d17-4178-b2ec-19599c1b26fb" />

- I gave my machine more memory and more cpu cores.

### Step 3 - Booting the machine up:

<img width="750" height="306" alt="image" src="https://github.com/user-attachments/assets/24342a7b-85ad-431e-838e-3d808d0b6038" />

- You may get this error when you boot the machine for the first time, don't worry we can fix it.

<img width="754" height="729" alt="Fixing the power on error" src="https://github.com/user-attachments/assets/84109734-d234-47ef-bbd4-b4eddec38260" />

- Once you power the machine off, go to the settings of the machine then into floppy, then turn this setting off.
- After this, we can power the machine back up again.

<img width="1019" height="765" alt="Updateing the machine" src="https://github.com/user-attachments/assets/e608f409-f7f5-4b43-ba54-5fad2a48820f" />

- After we log in with the local admin account we created, we will update the machine following best security practices.
- Restart the machine when the updates are done so they can take full effect.

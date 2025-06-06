
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket-Post-Installation</h1>
This tutorial outlines the post-installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket

<h2>Operating Systems Used </h2>

- Windows 10 (22H2)</b> 

<h2>List of Post-Install Configuration Objectives</h2>

 - Section 1: Intro to URLs and Admin Panel vs Agent Panel
 - Section 2: [Roles](https://docs.osticket.com/en/latest/Admin/Agents/Roles.html)
 - Section 3: [Departments](https://docs.osticket.com/en/latest/Admin/Agents/Departments.html)
 - Section 4: [Teams](https://docs.osticket.com/en/latest/Admin/Agents/Teams.html)
 - Section 5: [Agents](https://docs.osticket.com/en/latest/Admin/Agents/Agents.html) & [Users](https://docs.osticket.com/en/latest/Agent/Users/User%20Directory.html)
 - Section 6: [Service Level Agreements (SLA)](https://docs.osticket.com/en/latest/Admin/Manage/SLA%20Plans.html)
 - Section 7: [Help Topics](https://docs.osticket.com/en/latest/Admin/Manage/Help%20Topic.html)

<h2>Configuration Sections</h2>

<p>

<h2>Section 1 - Intro to URLs and Admin Panel vs Agent Panel</h2>
 
 - Once you get logged into the VM and osTicket, it will direct you to the Agent Panel

![osticket Step 1a](https://github.com/user-attachments/assets/29d1c80b-8b67-4339-be91-16db4941e3e4)

 - Noticed the highlighted area that says "Admin Panel" and selected it.

![osticket Step 1b](https://github.com/user-attachments/assets/768b1824-c6fc-4362-9bbf-e963c16f8544)

- Notice that under this panel, it lists "Dashboard", "Settings", "Manage", "Email", and "Agents". This is where we will be primarily working today with this project.

- Admin Panel - This is used by the System Admin to configure settings on the backend.

- Agent Panel - This is used by the Help Desk Agents or Support Specialists to view and work on tickets.

<h2>Section 2 - Roles</h2>

- We are going to create a Role called "Supreme Admin" and give it every permission we can. (In real life, this is bad to do, but for practice purposes, it's okay)

- Go hover your mouse over "Agents" and then select "Roles"

![osticket Step 2a](https://github.com/user-attachments/assets/b7415f1b-294b-4a15-aba6-938923a7f318)

- Select Add New Role

![osticket Step 2b](https://github.com/user-attachments/assets/83c08153-22df-47fb-bd2c-6566f6a77e72)

- Add the Name: "Supreme Admin" and then select Permissions

![osticket Step 2c](https://github.com/user-attachments/assets/e4352cb7-898e-414d-902d-a1634a738a11)

- Select every permission available to select in each tab, and then select "Add Role"
  
![osticket Step 2d](https://github.com/user-attachments/assets/f14f5231-55c2-4b91-ac2e-80300f179ba1)

- Congratulations, we've have created your first role in osTicket

![osticket Step 2e](https://github.com/user-attachments/assets/0670770f-e7d8-4e3f-97ec-ccfe77baef00)

<h2>Section 3 - Departments</h2>

- In this section, we are going to create a Department called "SysAdmins"

- Within the Admin Panel, click "Agents" > "Departments" > "Add New Department"

![osticket Step 3a](https://github.com/user-attachments/assets/fe98c0b2-2337-4750-b63e-1b9ea3b1b1bb)

- Under Settings, leave Parent as "Top-Level Department" and name the department "SysAdmins" then "Create Dept"

![osticket Step 3b](https://github.com/user-attachments/assets/79472fed-4046-4201-b155-88f02b0927eb)

- Congratulations, we've created a Department

![osticket Step 3c](https://github.com/user-attachments/assets/7ae60fe5-0452-436b-bd91-d74d226541e3)

<h2>Section 4 - Teams</h2>

- Next we will create a Team called "Online Banking"
- Admin Panel > Teams > Add New Team

![osticket Step 4a](https://github.com/user-attachments/assets/bfb55d91-fbba-4eef-b749-5bfa34713a94)

- Name the team "Online Banking" and select "Create Team"

![osticket Step 4b](https://github.com/user-attachments/assets/c1d30a29-193c-4e34-999b-000dbe910e43)

- Note: you will more than likely have to navigate back to Agents > Teams to see that the team is created. (At least I did)

![osticket Step 4c](https://github.com/user-attachments/assets/a49aac28-95aa-4c79-9da6-4d8a73d821bb)

- Before moving on to the next session, let's check to make sure a setting is turned off
- Go to "Settings" > "User" > and make sure the box that says "Require registration and login to create tickets" is unchecked

![osticket Step 4d](https://github.com/user-attachments/assets/449ace6a-1bf3-47ae-bb6e-e083f04bb047)

<h2>Section 5 - Agents</h2>














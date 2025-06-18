
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket-Post-Installation</h1>
This tutorial outlines the post-installation of the open-source help desk ticketing system osTicket.<br />

<h2>Prerequisites</h2>

- [Creating a VM in the Cloud](https://github.com/thechrisheller/Creating-VM-Azure) 
- [osTicket: Installation](https://github.com/thechrisheller/osTicket-Installation)

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

- Congratulations, we've created your first role in osTicket

![osticket Step 2e](https://github.com/user-attachments/assets/0670770f-e7d8-4e3f-97ec-ccfe77baef00)

<h2>Section 3 - Departments</h2>

- In this section, we are going to create a Department called "SysAdmins"

- Within the Admin Panel, click "Agents" > "Departments" > "Add New Department"

![osticket Step 3a](https://github.com/user-attachments/assets/fe98c0b2-2337-4750-b63e-1b9ea3b1b1bb)

- Under Settings, leave Parent as "Top-Level Department" and name the department "SysAdmins," then "Create Dept."

![osticket Step 3b](https://github.com/user-attachments/assets/79472fed-4046-4201-b155-88f02b0927eb)

- Congratulations, we've created a Department

![osticket Step 3c](https://github.com/user-attachments/assets/7ae60fe5-0452-436b-bd91-d74d226541e3)

<h2>Section 4 - Teams</h2>

- Next, we will create a Team called "Online Banking"
- Admin Panel > Teams > Add New Team

![osticket Step 4a](https://github.com/user-attachments/assets/bfb55d91-fbba-4eef-b749-5bfa34713a94)

- Name the team "Online Banking" and select "Create Tea.m"

![osticket Step 4b](https://github.com/user-attachments/assets/c1d30a29-193c-4e34-999b-000dbe910e43)

- Note: You will more than likely have to navigate back to Agents > Teams to see that the team is created. (At least I did)

![osticket Step 4c](https://github.com/user-attachments/assets/a49aac28-95aa-4c79-9da6-4d8a73d821bb)

- Before moving on to the next session, let's check to make sure a setting is turned off
- Go to "Settings" > "User" > and make sure the box that says "Require registration and login to create tickets" is unchecked

![osticket Step 4d](https://github.com/user-attachments/assets/449ace6a-1bf3-47ae-bb6e-e083f04bb047)

<h2>Section 5 - Agents & Users</h2>

- In this section, we will create 2 agents and 2 users
- Let's start with the two agents

- Admin Panel > Agents > Agents
- Add New Agent

![osticket Step 5a](https://github.com/user-attachments/assets/626660e8-d649-4866-890d-2b5834f27626)

- Fill in the first and last name and a Username.
- NOTE: Keep track of your username and password for each agent and user you create!!!

![osticket Step 5b](https://github.com/user-attachments/assets/eb18ffa4-baff-413c-bde0-c1e0c4de8a45)

- Uncheck "send the agent a password reset email (this is for practice use only; normally, this would be used in real life)
- Uncheck "Require password change at next login so you don't have to change the password in the next lab

![osticket Step 5c](https://github.com/user-attachments/assets/f5c7dd7b-f88d-4b7f-b97e-5b930387711a)

- For the admin user you are creating, which in this case for me is Jane Admin, go to "Access" and select the department "SysAdmins" and the Role "Supreme Admin" for this agent

![osticket Step 5d](https://github.com/user-attachments/assets/3fcfab9a-9a93-41a6-8092-d1fa6c8528e6)

- In the next project, if you are unable to see submitted Tickets, add Extended Access Support | Supreme Admin
  
![Update pic](https://github.com/user-attachments/assets/cf136554-2c14-404f-80e7-7adf38427611)

- Let's go ahead and assign Jane Admin to the team "Online Banking"
- Select Add Next to "Online Banking"
- Go to Teams > Select Online Banking from the drop-down

![osticket Step 5e](https://github.com/user-attachments/assets/ce1e8953-8ff9-4735-8fe8-896cab9f4ca3)

- To get back to Agents, select "Agents" and then "Agents" on the lower bar

![osticket Step 5f](https://github.com/user-attachments/assets/8fdee5ca-0928-4f54-86d8-42ee5c4211a1)

- Let's create a support user named John Support
- Do the same steps as before in the main account area, and remember the login credentials for later on

![osticket Step 5g](https://github.com/user-attachments/assets/5bc95117-6170-4c80-8657-a1b35ec51787)

- Give John the department called "Support" and "View Only" Role, and then create

![osticket Step 5h](https://github.com/user-attachments/assets/eedf597c-e082-4490-8477-5965cdefe39f)

- Notice that both agents are created once you work your way back to the agents tab

![osticket Step 5i](https://github.com/user-attachments/assets/0165f2d3-d598-42e0-b212-6bc274e1b4d4)

- Let's go back to the Agent Panel. This is where we are going to create a couple of users
- Agent Panel > User > User Directory
- Add User

![osticket Step 5k](https://github.com/user-attachments/assets/071f4664-3fc7-484d-af8b-0c4aa0ac2e15)

- Add in a fake email here and make up a name, but remember the name for later

![osticket Step 5L](https://github.com/user-attachments/assets/4bf3ca16-1aac-46af-985a-583a2f8f2525)

- Repeat the step, and this is something of what it should look like

![osticket Step 5m](https://github.com/user-attachments/assets/040d69eb-c70f-4039-ac81-2d1c145a0645)

- We have successfully created a couple of agents and users!

<h2>Section 6 - Service Level Agreements (SLA)</h2>

- The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed.
- Admin Panel > Manage > SLA

![osticket Step 6a](https://github.com/user-attachments/assets/6b84e61f-2e13-4209-9c35-a87b3a54825a)

- We are going to call our first SLA "SEV-A" and it will be the most urgent of the 3 we are going to create
- Grace Period 1 hour, which means this needs to be worked on and fixed pretty much ASAP
- Schedule it for 24/7

![osticket Step 6b](https://github.com/user-attachments/assets/25ba92f6-84f7-4583-9670-29d8bf27f8e3)

- Repeat the process over and name the next one "SEV-B", and a grace period of 4-hour, and to be scheduled 24/7 as well

![osticket Step 6c](https://github.com/user-attachments/assets/d9abba92-22fc-4105-a651-b7dd23fa6232)

-  This 3rd SLA is going to be a little different. We are going to call it "SEV-C" and it has an 8-hour grace period and is only scheduled Monday-Friday from 8 am-5 pm

![osticket Step 6d](https://github.com/user-attachments/assets/a0879117-9ed8-4d1c-bce5-b860afba098c)

- We have created our 3 SLA's
- Congrats!!!

![osticket Step 6e](https://github.com/user-attachments/assets/e8924f24-aff7-4298-b2c5-319ef031fa90)

<h2>Section 7 - Help Topics</h2>

- For the final section of this project, we will add some Help Topics.
- From Admin Panel, click Manage > Help Topics > Add New Help Topic

![osticket Step 7a](https://github.com/user-attachments/assets/d8014972-08e8-466b-a517-d2548e50d525)

- Let's create a topic called "Business Critical Outage" and select the parent topic it falls under. In this case, the parent topic is "Report a Problem".

![osticket Step 7b](https://github.com/user-attachments/assets/1f649762-dc3b-4b58-a043-72366a171616)

- Let's create a couple more topics and select the parent topic for each
- Personal Computer Problem

![osticket Step 7c](https://github.com/user-attachments/assets/5d83a8ef-27f5-408f-ad31-0636ceaed08b)

- Equipment Request

![osticket Step 7d](https://github.com/user-attachments/assets/d458dd18-990a-4b1c-9fbf-ca60f9eeefe3)

- Password Reset

![osticket Step 7e](https://github.com/user-attachments/assets/50d55bda-241d-4762-9cd0-90851bfa3dac)

- Other

![osticket Step 7f](https://github.com/user-attachments/assets/0624d6cc-e0db-4a6b-a242-b46e74714a9e)

- We have finally reached the end of the lab and have created all of our Help Topics for this part of the lab

![osticket Step 7g](https://github.com/user-attachments/assets/cae8974d-6bca-44f7-b81f-e012e543e3dc)

<h2>Conclusion</h2>

- This concludes our project. We have completed the post-install configurations for osTicket. Make sure to turn off your VM so that you are not being billed while not in use. 

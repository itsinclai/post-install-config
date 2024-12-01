<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
<p>This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.</p>

<p>After successfully installing osTicket, the next step is to configure the system to suit your organization's needs. These steps outline how to set up roles, departments, teams, and other critical settings to ensure a smooth ticketing process.</p>


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Explore osTicket Portal
- Make configurations to prepare for solving mock tickets

<h2>Configuration Steps</h2>

<b>Step 1: Configure Roles</b>

![image](https://github.com/user-attachments/assets/7b77fb0e-c885-43cf-a711-1310567e3ac0)

<p>
Navigate to Admin Panel > Agents > Roles. You’ll notice predefined roles, such as “View Only” and “Expanded Access.”

- For example, if you click on View Only and go to Permissions, no permissions are selected, meaning agents assigned this role have limited access.
</p>

![image](https://github.com/user-attachments/assets/12781801-8880-412b-ba61-6c03552d6d4a)

- If you check Expanded Access, you’ll see more permissions are enabled.

![image](https://github.com/user-attachments/assets/bc079eb2-aec5-4274-b7c1-33b55276d63a)

For the purpose of this step, we will create a new role.

- Click Add a New Role.
- Name the role (e.g., Supreme Admin) and define its permissions.
- The Supreme Admin role will have full access to all system features.

<b>Step 2: Configure Departments</b>

Departments in osTicket determine ticket visibility and help organize your help desk operations. For example, a ticket about networking issues can be assigned to the Networking department, while system administration tickets go to SysAdmins. This ensures tickets are routed to the right teams.

![image](https://github.com/user-attachments/assets/025b80ba-e6c4-439e-a870-6c3ddc65624a)

- Navigate to Admin Panel > Agents > Departments.
- Click Add a New Department and name it (e.g., SysAdmins).

![image](https://github.com/user-attachments/assets/677c2a4a-72dc-45ac-bb02-54d4794512cf)

<b>Step 3: Configure Teams</b>

Teams allow you to group agents from different departments to collaborate on specific ticket types or projects. For example, an Online Banking Team might include agents from both the SysAdmins and Support departments.

![image](https://github.com/user-attachments/assets/f83f0661-640b-4c20-8c77-4bee30d414a7)

- Navigate to Admin Panel > Agents > Teams.
- Click Add New Team.
- Name the team (e.g., Online Banking) and assign members from various departments.

<b>Step 4: Allow Anyone to Create Tickets</b>

This setting determines how users interact with your ticketing system. By allowing unregistered users to create tickets, you lower the barrier to entry for getting help. Conversely, requiring registration ensures more control and accountability over user submissions.

![image](https://github.com/user-attachments/assets/3f93a857-6d1d-49c6-9ee9-e61b348a6d84)

- Navigate to Admin Panel > Settings > User Settings.
- UNCHECK the box for Registration Required to allow anyone to create tickets.

<b>Step 5: Configure Agents (Workers)</b>


Agents are the individuals responsible for managing tickets. Each agent must have an account with assigned roles, departments, and teams to ensure they can perform their tasks effectively.

- Navigate to Admin Panel > Agents > Add New.
- Create accounts for your agents:
- Jane (Dept: SysAdmins, Role: Supreme Admin, Team: Online Banking)
- John (Dept: Support, Role: Expanded Access)

![image](https://github.com/user-attachments/assets/71cb9b15-c584-434d-918b-0d0613f85662)

<b>Step 6: Configure Users (Customers)</b>

Users are your customers or end-users who will be submitting tickets. Setting up user accounts helps you track interactions and manage tickets more effectively.

- Navigate to Agent Panel > Users > Add New.
- Add user profiles for your customers:
- Karen
- Ken

![image](https://github.com/user-attachments/assets/bf8e2d76-be97-4896-85eb-cb820279aa42)

Next we will assign Jane access and give her the role of Supreme Admin that we created earlier. We will place Jane in the SysAdmins department and assign her to the online banking team as well.

<b>Step 7: Configure SLAs (Service Level Agreements)</b>

SLAs define the timeframes within which tickets must be resolved based on their priority. For example, a critical system outage might require resolution within an hour, while a password reset might allow for an 8-hour response time.

![image](https://github.com/user-attachments/assets/5c4edf58-b035-49da-ae5a-e290afc5fb34)

- Navigate to Admin Panel > Manage > SLA.
- Set up SLAs based on urgency:
- Sev-A: Grace Period: 1 hour, Schedule: 24/7
- Sev-B: Grace Period: 4 hours, Schedule: 24/7
- Sev-C: Grace Period: 8 hours, Schedule: Business Hours

![image](https://github.com/user-attachments/assets/9a29e99b-8365-4bf1-a166-0f732ed19987)

<b>Step 8: Configure Help Topics</b>

Help Topics categorize tickets when they are created, making it easier for users to specify their issue and for agents to prioritize and route tickets.

![image](https://github.com/user-attachments/assets/9e8bf8fd-2212-4ffa-9c75-61fd4e337599)

- Navigate to Admin Panel > Manage > Help Topics.
- Add help topics to cover common issues:
- Business Critical Outage
- Personal Computer Issues
- Equipment Request
- Password Reset
- Other

![image](https://github.com/user-attachments/assets/5de6620f-801a-4d3d-8629-63b152212a53)



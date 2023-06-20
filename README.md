<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles
- Configure Departments
- Configure Teams
- Configure Ticket Permissions
- Configure Help Topics

<h2>Configuration Steps</h2>

<p>
Log back into the osTicket Admin Panel with the credentials created in the previous lab [http://localhost/osTicket/scp/login.php].
<p align="center"><img src="blank" height="70%" width="70%" alt="osticket admin panel"/> </p>
</p>
<br />

<p>
<b>Step 1: Configure Roles</b>
<br />
 
 "<a href="https://docs.osticket.com/en/latest/Admin/Agents/Roles.html">Roles</a> are the permissions granted to Agents per Department that they have access to. Each Role has a set of permissions that can be checked/unchecked for agents given that Role in association with a Department they have access to. An unlimited number of roles can be created and assigned to Agents with access to various departments."
</p>
<br />

<p>
Go to Admin Panel -> Agents -> Roles -> Add New Role. Enter the name "Supreme Admin" for the role and then navigate to the Permissions tab. Enable every permission in "Tickets", "Tasks" and "Knowledgebase".
<p align="center"><img src="blank" height="70%" width="70%" alt="configure roles"/> </p>
<p align="center"><img src="blank" height="70%" width="70%" alt="configure roles"/> </p>
<p align="center"><img src="blank" height="70%" width="70%" alt="configure roles"/> </p>
<p align="center"><img src="blank" height="70%" width="70%" alt="configure roles"/> </p>
</p>
<br />

<p>
<b>Step 2: Configure Departments</b>
<br />
 
"Since tickets are routed through <a href="https://docs.osticket.com/en/latest/Admin/Agents/Departments.html">Departments</a> in the help desk, there are many settings that can be set for each Department."
</p>
<br />

<p>
Go to Admin Panel -> Agents -> Departments -> Add New Department. Name the new department "System Administrators" and click Create Dept.
<p align="center"><img src="blank" height="70%" width="70%" alt="configure departments"/> </p>
<p align="center"><img src="blank" height="70%" width="70%" alt="configure departments"/> </p>
</p>
<br />

<p>
<b>Step 3: Configure Teams</b>
<br />

"<a href="https://docs.osticket.com/en/latest/Admin/Agents/Teams.html">Teams</a> allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter."
</p>
<br />

<p>
Go to Admin Panel -> Agents -> Teams -> Add New Teams. Name the team "Level II Support", add yourself to the team and select Create Team.
<p align="center"><img src="blank" height="70%" width="70%" alt="configure teams"/> </p>
<p align="center"><img src="blank" height="70%" width="70%" alt="configure teams"/> </p>
<p align="center"><img src="blank" height="70%" width="70%" alt="configure teams"/> </p>
</p>
<br />

<p>
<b>Step 4: Allow anyone to create tickets</b>
<br />
Go to Admin Panel -> Settings -> User Settings. Uncheck the box that says "Require registration and login to create tickets" and save changes.
</p>
<br />

<p>
<b>Step 5: Configure Agents</b>
<br />
 
"<a href="https://docs.osticket.com/en/latest/Admin/Agents/Agents.html">Agents</a> are given access to the help desk with the intent to respond and resolve the tickets. When adding an Agent to the help desk, they will need to be assigned to a Primary Department and given a Primary Role for the Tickets/Tasks routed to that department. Agents can be given Extended Access to additional departments of the help desk as well as assigned different Roles to those departments; this can be configured in the Access tab of the Agent’s Profile."
</p>
<br />

<p>
Go to Admin Panel -> Agents -> Add New Agent. For this lab we will be creating two agents. For each agent fill out the Name, Email and Username fields then set a password (do not require a reset or change). 
</p>
<br />

<p>
In the Access Tab assign Agent 1 to the "Systems Administrators" Department and give extended access to the Support Department. Assign Agent 2 to the "Support" Department.
</p>
<br />

<p>
<b>Step 6: Configure Users</b>
<br />
 
"<a href="https://docs.osticket.com/en/latest/Agent/Users/User%20Directory.html">Users</a> are the ticket owners of the tickets in the help desk."
</p>
<br />

<p>
Go to Agent Panel -> Users -> Add User. Create two users with an email and name.
</p>
<br />

<p>
<b> Step 7: Configure SLA</b>
<br />
 
  "<a href="https://docs.osticket.com/en/latest/Admin/Manage/SLA%20Plans.html">SLA</a> Plans or Service Level Agreements, are unlimited in osTicket. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed."

<p>
Go to Admin Panel -> Manage -> SLA. We will create three different SLA's.
<br />
 - Sev A (1 hour, 24/7)
<br />
 - Sev B (4 hours, 24/7)
<br />
 - Sev C (8 hours, business hours)
</p>
<br />
 

<p>
<b> Step 8: Configure Help Topics</b>
<br />
 
 "<a href="https://docs.osticket.com/en/latest/Admin/Manage/Help%20Topic.html">Help Topics</a> will help streamline your end-user’s help desk experience to ensure proper assignment and prompt response to the ticket."
</p>
<br />

<p>
Go to Admin Panel -> Manage -> Help Topics. We will create four different Help Topics.
<br />
- Business Critical Outage
<br />
- Personal Computer Issues
<br />
- Equipment Request
<br />
- Password Reset
</p>
<br />

<p>
Congratulations, you have completed the post-installation configuration for osTicket! In the next lab we will go over the lifecycle of a ticket. 
</p>
<br />

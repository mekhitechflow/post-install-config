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
- Allow anyone to create tickets so that we can see them on our end to resolve them.
- Configure Agents (Workers)
- Configure Users (Customers)... these are the people who are creating the tickets!
- Configure SLAs (Service Level Agreements), make several, and change the importance of each one!
- configure Help Topics 

<h2>Configuration Steps</h2>

<p>
This tutorial goes over the post configuration of setting up osTicket!
</p>
<p>
To create agents in osTicket, start by logging into the admin panel of your osTicket system. Once logged in, navigate to the Users section and select Agents from the drop-down menu. This will take you to the Agents management page. To add a new agent, click on the Add New Agent button. You’ll be directed to a form where you need to enter the agent’s details, including their full name, email address, username, and a secure password. Optionally, you can provide their phone number. Next, set the appropriate permissions for the agents by selecting their roles, which determine their level of access and responsibilities for this lab we are creating a Supreme Admin they will be given all permissions. Assign the agent to relevant departments and groups if applicable. After filling out all the required information and configuring permissions, save the changes to create the new agent. The agent will now appear in the list and will be able to log in using their credentials. If you didn’t choose to send the password via email, make sure to provide the agent with their login details and any necessary instructions on accessing the system.
</p>
<p>
<img width="953" alt="Agents" src="https://github.com/user-attachments/assets/1bd159c8-fd0c-4570-aee6-c1bb51d0c93c">
</p>
<br />

<p>
To create a new department in osTicket, start by logging into the admin panel of your osTicket system. Once logged in, go to the Admin Panel and select Departments from the menu. This will bring you to the department's management page. Click on the Add New Department button to open the department creation form. Enter "System Administrators" as the department name. You can also provide a description of the department to clarify its purpose or scope. Configure the department settings according to your needs, such as setting it as a default department for certain types of tickets if desired. After filling out all the necessary details, click Save Changes to create the new department. The "System Administrators" department will now be listed among your existing departments and can be assigned to agents or used for ticket routing as needed.
</p>
<p>
<img width="949" alt="Departments" src="https://github.com/user-attachments/assets/9f276913-0c08-4e85-93e8-55ef7ecf7166">
</p>
<br />

<p>
To create help topics in osTicket, begin by logging into the admin panel of your system. Navigate to the Admin Panel and select Help Topics from the menu. On the Help Topics management page, click on the Add New Help Topic button to open the creation form. For each help topic, enter the name and description to define its purpose. Create the following help topics: "Business Critical Outage," which should be highlighted due to its high importance and urgency; "Personal Computer Issues," for issues related to individual workstations; "Password Reset," addressing requests for password recovery and management; and "Equipment Request," for requests related to hardware or other equipment. It’s important to categorize these help topics based on their varying levels of importance, as this will help in prioritizing and managing tickets effectively. After entering all necessary details for each help topic, click Save Changes to finalize their creation. These help topics will assist in organizing incoming support requests and setting the stage for implementing Service Level Agreements (SLAs) based on their importance and urgency.
</p>
<p>
<img width="949" alt="Help Topic" src="https://github.com/user-attachments/assets/94d8100b-177b-4e14-b4ca-ffc4c244ed02">
</p>
<br />

<p>
We are now going to create a "Supreme Admin" role in osTicket. Begin by logging into the admin panel of your osTicket system. Navigate to the Admin Panel and select Roles from the menu. On the Roles management page, click on the Add New Role button to open the role creation form. Name the new role "Supreme Admin" to reflect its comprehensive permissions. Configure this role to have access to all available permissions within the system, ensuring it includes every administrative function, from user management and ticket configuration to system settings. This setup will grant the role complete control over the osTicket environment. Once you’ve configured the permissions, click Save Changes to create the role. The "Supreme Admin" role will now be listed among your existing roles and can be assigned to users requiring full system access.
</p>
<p>
<img width="895" alt="Roles" src="https://github.com/user-attachments/assets/5217e6cf-a82e-44d0-819b-53674b46613d">
</p>
<br />

<p>
This step allows anyone to create tickets. Admin Panel->Settings->User Settings.
</p>
<p>
<img width="951" alt="v" src="https://github.com/user-attachments/assets/82053403-58b5-4b32-9bb8-2d7361d1413f">
</p>
<br />

<p>
SLAs Plans provide a length of time in which the help desk is expected to take in order to solve a specific ticket. SLA Plans are created by going to Admin Panel->Manage->SLA Plans. Each SLA has a schedule and within that schedule, there is a grace period. In this example, SEV-A has a 24/7 and a one-hour grace period.
</p>
<p>
<img width="949" alt="SLA" src="https://github.com/user-attachments/assets/78688ac4-ce03-45b5-83f5-76b13ca7ec08">
</p>
<br />

<p>
Since we have already configured a new department we will set up a new team. Teams allow you to pull agents from different departments you can have an A team that has top technicians from specific departments. For example, you can create a help topic that correlates with a product you produce, and assign it to a team of agents that specialize in that particular product. To set up a team go to Agents->Teams. A Level I support team has been created by default, in this example, we will create a Level II Support Team.
</p>
<p>
<img width="954" alt="Teams" src="https://github.com/user-attachments/assets/7d402515-0c00-4295-9ea8-826c0e4fd749">
</p>
<br />

<p>
Lastly, we will need to create users. Users are customers who create tickets when they are having issues. A user is identified with their E-mail address. To create a user follow this path Agent Panel->Users->User Directory->Add new.
</p>
<p>
<img width="951" alt="Users" src="https://github.com/user-attachments/assets/42ce117f-846c-4017-92dd-ec0cc657f206">
</p>
<br />

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post installation setup</h1>
This tutorial outlines the post installation process of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- OsTicket

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Prerequisetes</h2>
- Have completed part <a href="https://github.com/TimjMerida/osTicket-pt2-Installing-osTicket/blob/main/README.md">Two</a> of the 4 part tutorial
- Be connected to the Windows VM via RDP  
- Logged into osTicket

<h2>Objectives</h2>
Our objective in this tutorial is to set up osTicket for use in a help desk environment. We will configure departments, teams and users as well as set up SLA's (Service Level Agreements) for our fictional help desk support. 

<h2>Post Install</h2>

<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The first step in our post installation setup is to configure our roles. We will make a role called head admin that will be able do do anything we need to set up osTicket.
  
In osTicket we need to be in the admin panel. You can toggle between admin panel and agent panel on the top right. 
In the admin paned go to agents - roles and add a new role. 
</p>
<br />

<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I will name the new role head admin but you can name it whatever you want. Under permisions we will check every box under tasks, tickets and Knowledgebase for this role. Then add role. In an actual help desk environment a role may only have certain permissions that are needed for their job.
</p>
<br />

<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next is to set up departments. Departments are ways to section different agents (help desk employees) for the department they work in. We will use this later when assigning tickets in part 4.

Departments is in the admin panel under agents. We are going to add a new department named System Administrators. There are plenty of settings we can make for each department after the tutorial I recommend playing around with creating new departments but for now we can leave them as is. Then create a second department named Network department. 
</p>
<br />

<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next is to set up our teams. From the osTicket website "Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter.". We can use teams to put together department managers or specialists that can work on a major issue. For example if there is a outage at a bank we might have a set team who can handle the issue ranging form electritions to network engineers.
  
In the admin panel under agents is teams and we will add a new team. We can name this team Level 1 support. Click create team and make another team named Level 2 support.
</p>
<br />

<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will allow anyone to create a ticket. Under admin panel go to settings - users - settings. Under Authentication settings make sure registration required is unchecked. This allows anyone to create a ticket from the portal (part 4).
</p>
<br />


<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we will add our agents. Agents are the employees who will work the tickets. Under the admin panel go to agents and create new agents. We will make two agents, Jessica and David.
  
For Jessica we will fill out as follows. 

Name: Jessica Vaner

Email: JessV@osTicket.com

Usernamne: Jess_Vaner

Password: Password12321

For the password click set password and uncheck set agent password. This allows us to set the password for the agent. Also uncheck require password change at the next login.

Then under access we can change the agents department and role. We will make jessica a Systems Administrator and be a head Admin for the role. Then under teams we can change her to be level 2 support. 
Click add and then create to make the agent Jessica Vaner. Do the same with David using the following details. 

Name: David Bale 

Email: DavidB@osTicket.com

Username: David_Bale

Password: Password12321 

Department: Network department

Role: Head admin       
</p>
<br />


<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />


<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />


<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />


<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />


<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />


<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />


<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

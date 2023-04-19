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

- Windows 10</b> 

<h2>Prerequisetes</h2>
- Have completed part <a href="https://github.com/TimjMerida/osTicket-pt2-Installing-osTicket/blob/main/README.md">Two</a> of the 4 part tutorial
- Be connected to the Windows VM via RDP  
- Logged into osTicket

<h2>Objectives</h2>
Our objective in this tutorial is to set up osTicket for use in a help desk environment. We will configure departments, teams and users as well as set up SLA's (Service Level Agreements) for our fictional help desk support. 

<h2>Post Install</h2>

<p>
<img src="https://user-images.githubusercontent.com/128980344/232943697-18bb8084-f80c-41b3-9fa8-9e9588d7a4a2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The first step in our post installation setup is to configure our roles. We will make a role called head admin that will be able do do anything we need to set up osTicket.
  
In osTicket we need to be in the admin panel. You can toggle between admin panel and agent panel on the top right. 
In the admin paned go to agents - roles and add a new role. 
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/232943763-671290f1-45b1-495d-95db-c549f581cbb0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I will name the new role head admin but you can name it whatever you want. Under permisions we will check every box under tasks, tickets and Knowledgebase for this role. Then add role. In an actual help desk environment a role may only have certain permissions that are needed for their job.
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/232943823-a03758e4-e326-435c-96bf-7403fadee06f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://user-images.githubusercontent.com/128980344/232943870-b0c06599-c093-40bc-bd06-1e1eb955fcbd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next is to set up departments. Departments are ways to section different agents (help desk employees) for the department they work in. We will use this later when assigning tickets in part 4.

Departments is in the admin panel under agents. We are going to add a new department named System Administrators. There are plenty of settings we can make for each department after the tutorial I recommend playing around with creating new departments but for now we can leave them as is. Then create a second department named Network department. 
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/232943944-6b09cea3-5d02-47f3-93fd-c70c17b15663.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next is to set up our teams. From the osTicket website "Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter.". We can use teams to put together department managers or specialists that can work on a major issue. For example if there is a outage at a bank we might have a set team who can handle the issue ranging form electritions to network engineers.
  
In the admin panel under agents is teams and we will add a new team. We can name this team Level 1 support. Click create team and make another team named Level 2 support.
</p>
<br />

<p>
<img src="https://user-images.githubusercontent.com/128980344/232943985-0f236a9f-385b-471f-b083-0061670c6d6e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we will allow anyone to create a ticket. Under admin panel go to settings - users - settings. Under Authentication settings make sure registration required is unchecked. This allows anyone to create a ticket from the portal (part 4).
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232944022-4d6c4ada-5a80-4b01-a2b2-f98134d35270.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://user-images.githubusercontent.com/128980344/232944060-efd81c4e-5fe1-451a-a830-c1079278d7f1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we will add our agents. Agents are the employees who will work the tickets. Under the admin panel go to agents and add new agents. We will make two agents, Jessica and David.
  
For Jessica we will fill out as follows. 

Name: Jessica Vaner

Email: JessV<span>@</span>osTicket.com

Usernamne: Jess_Vaner

Password: Password12321

</p>  
<p>
<img src="https://user-images.githubusercontent.com/128980344/232944095-f17f7227-e48d-4288-b995-eeec162e8b29.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<img src="https://user-images.githubusercontent.com/128980344/232944303-bac6fe37-141c-4d6b-8847-33cbda25f3d5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For the password click set password and uncheck set agent password. This allows us to set the password for the agent. Also uncheck require password change at the next login.

Then under access we can change the agents department and role. We will make jessica a Systems Administrator and be a head Admin for the role. Then under teams we can change her to be level 2 support. 
Click add and then create to make the agent Jessica Vaner. Do the same with David using the following details. 

Name: David Bale 

Email: DavidB<span>@</span>osTicket.com

Username: David_Bale

Password: Password12321 

Department: Network department

Role: Head admin  
  
Team: Level 2 support

</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232944406-918432bd-6d6b-42d1-a19b-3d4f5c32eb9d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://user-images.githubusercontent.com/128980344/232944526-f1f0a7a3-dac6-4c6a-bd46-2ba8a71f3a6c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next is to set up a user. We need to be in the agent panel which can be changed on the top right by clicking agent panel. Then we go to users and add a user.
For this lab I will have the user be Greg Dosto with the email adress GregD<span>@</span>osTicket.com. We will also add another user Pele Toll with email PeleT<span>@</span>osTicket.com.
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232944592-19dd649e-21f1-4551-8af5-41c5d91574cb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://user-images.githubusercontent.com/128980344/232944649-9004a251-6c26-4a4e-bb77-58a69cdfa3ed.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next we are going to set up our SLA's. SLA or Service Level Agreements is an expectation of a service to a client provided by the service provider. In osTicket SLA's are used to set time limits on tickets for completion. They are used to help prioritize tickets based on severity for better service. For example an SLA that is set up with SEV-C being a computer not working or Sev-A a cloud server being down, would make clear what ticket should be worked on next.

To set up our SLA's in osTicket we have to go back to the admin panel on the top right. Then under manage we can click SLA and add new SLA plan. We will make 3 severitys for our plan. Fill in the plans one by one hitting add plan at the bottom when done.  

Name: Sev-A (Server down / High Severity)        

Schedule: 24/7 

Grace period: 1 hour


Name: Sev-B (Long loading time / Medium Severity)        

Schedule: 24/7

Grace period: 5 hours


Name: Sev-C (Employee computer running slow / Low Severity)

Schedule: Mon-Fri 8am-5pm

Grace period: 8 hours
</p>
<br />


<p>
<img src="https://user-images.githubusercontent.com/128980344/232944690-75867d4b-3907-4e89-85c4-f5043872f81d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://user-images.githubusercontent.com/128980344/232944699-bc0e55c1-7d57-4964-a0ac-c1360605b86d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next is to configure help topics. These are for the users to streamline their helpdesk experience. Go to the admin panel - manage and help topics. We will make 3 topics, Severe outage, Connection issue and password reset. We dont have to change any settings just add the name and add topic. Thats all we have to do for the post installation setup of osTicket. Next we will run through 3 "examples" of osTicket in use. Part <a href="https://github.com/TimjMerida/osTicket-Pt4-Ticket-lifecycle">four - Ticket lifecycle  
</p>
<br />





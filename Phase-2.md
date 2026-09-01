# Phase 2 - Design the OU Hierarchy
Now that the initial setup is complete, I wanted to create an easy, manageable, structure. This is important because it keeps the business well aligned and efficient. New users or clients will be able to adapt quickly to the environment without confusion. I decided to design one that is business department and group policy object oriented.
* <img width="237" height="255" alt="OU Structure" src="https://github.com/user-attachments/assets/19cadfe8-d308-4717-8008-a9b17fb95171" />

# How it was Built
Starting from the DC VM, open Active Directory Users and Computers, right click the domain name "TechCorp.local" select new then select Organizational Units name it "TechCorp_Objects". This is the property that will store all of the Computers, Departments, Groups, and Service Accounts categories. 
        
  - **Note**: I wanted to prevent accidental deletion to this OU, so I saw a feature that gave me the option to enable accidental deletion protection and checked the box.
  - <img width="415" height="447" alt="Accidental protection enabled" src="https://github.com/user-attachments/assets/2447c7cf-2b53-489c-9180-2feb58e93a0e" />

  Now that we have the main OU created, I now can create the sub OUs (That would be Departments, Groups, Computers, Service Accounts stored under the main OU). To do this I right click "TechCorp_Objects", then "new", and "Organizational Unit". The screenshot below shows the result of that process. 
  - <img width="197" height="100" alt="Sub OUs created" src="https://github.com/user-attachments/assets/01ba2069-4d0c-4d5e-b05f-64acf572c6cc" />

  Lastly, I wanted to create the actual departments inside of the Department OU. To do this is the same process as before. Right click "Departments", click "new", then "Organizational Unit". The screenshot below shows the result of the different departments created.
  - <img width="216" height="112" alt="created departments in the department OU" src="https://github.com/user-attachments/assets/e6409367-a1d7-473f-88d3-73407aa51414" />


 

Next Phase > [Phase-3.md](Phase-3.md)

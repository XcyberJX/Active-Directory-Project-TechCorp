# Phase 3 - Create Users and Security Groups
Now that the OU structure is created, we will now create the users belonging to their designated department and assign specific Security Groups(RBACs) to each department. Creating groups will make assigning permissions to users much easier and faster rather than giving them permissions individually. This is important because this sets boundaries to groups with least privilege access making the environment more secure and manageable. 
- <img width="237" height="255" alt="created a security group OU" src="https://github.com/user-attachments/assets/bea2c6b3-11e3-4054-a0c6-7bf4f6dbf8b0" />

Begin by creating an OU called "Groups" then inside create another OU called "Security Groups". Inside of "Security Groups" I will create a group for the IT, Finance, and HR departments. Each with their own purpose and their own set of permissions to resources within the environment. The screenshot below provides what it should look like.
- <img width="530" height="342" alt="GRPs created" src="https://github.com/user-attachments/assets/9102f5d9-ed25-458e-b9f9-f6d9864cb2fd" />
Now that the groups are created, I can now create my first set of users. The users I will create will be Jane Doe for the HR department, John Smith for the Finance department, and Alex Rivera for the IT department. To create users simply right click the designated department OU, then click new, then select user. It will then bring up a window named "New Object - User" asking for a firstname, lastname, and the username. Entering in the following credentials then hitting next will take you to a password section that show password creation and account requirements. For this task, I gave the users a simple password and set the accounts to have to change their password at next login. This was to ensure that the actual account holder is the account holder. This will be a security practice that 


<img width="512" height="457" alt="User Jane Doe" src="https://github.com/user-attachments/assets/371c64ac-de4a-470e-b2fe-3d24335be8e4" />
<img width="492" height="430" alt="User John Smith" src="https://github.com/user-attachments/assets/e0192c00-6942-40ec-a508-5494fe680092" />
<img width="512" height="428" alt="User Alexa Rivera" src="https://github.com/user-attachments/assets/bd7cbb46-3c45-451d-a316-e230d436099d" />





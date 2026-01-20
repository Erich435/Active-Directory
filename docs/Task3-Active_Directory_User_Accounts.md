# Task 3 - Configure Active Directory User Accounts
Accounts to be created:
  * **ITadmin**
  * **John**
  * **ServiceDesk**

# Steps performed

1. Entered Active Directory Users and Computers from the domain controller Server Manager

2. In the Users container, the following users were created:
  *  **ITadmin**
  *  **John**
  *  **ServiceDesk**
 
All three users were also generated with passwords to be changed after first time log on

3. Signed into each user account individually to verify that the user will be prompted to create a new password before signing in 

# Problems encountered
  * I had accidentally created a new Organizational Unit (OU) within the **Domain Controllers** OU, not only was this out of scope with the current task, it would have also caused issues when applying Group Policy Objects (GPOs) to the Users.
  * I also could not delete the OU due to **Accidental deletion prevention** option

To fix this I first enabled **Advanced Features** in the **View** drop down menu, this allowed me to now uncheck the **Accidental deletion prevention** option in the properties menu. After doing this I was able to remove the OU and created each user within the **Users** container.

# Verification
  * The client virtual machine was able to log into domain users accounts
  * Each user was prompted to create a new password upon signing in

![Active Directory User Creation](/docs/images/ADusers.png)
![Users in AD](/docs/images/Users.png)
![Change Password](/docs/images/ChangePW.png)

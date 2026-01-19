# Task 2 - Deploy a Windows 11 Pro virtual machine configured with the following parameters:
* Hostname: **Workstation1**
* Static IP Address: **192.168.50.50/24**
* DNS Server: **192.168.50.5**
* **Successfully joined to the Active Directory domain and verified using command-line tools**

# Steps Performed
1. Created a new Virtual Machine in VMware Workstation Pro
  * Default settings used
  * Windows 11 ISO image used

2. Installed Windows 11 to the Virtual Machine
  * Windows 11 Pro edition selected
  * Local Admin and hostname configured during initial setup (Workstation1)

3. Static IP addresses configured as follows:
  * IP Address: 192.168.50.50
  * Subnet Mask: 255.255.255.0
  * DNS Server: 192.168.50.5
  * Additionally, the default gateway has been configured with: 192.168.50.2 - The Virtual Default Gateway address

4. Tested client machine has network connectivity to Windows Server machine with ping
  * 4/4 Pings succeeded - 100% Success rate

5. Joined client machine to **lab.local** domain
  * Client machine restarted in order for changes to take effect

# Problems encountered:
  * I did not have any active Active Directory user accounts to login with on the client machine, in order to verify the client machine was now successfully a member of the domain, I used Windows Key + R to bring up the RUN dialog then entered **sysdm.cpl**. This brought up system properties and I could see that the client machine had sucessfully joined the domain **lab.local**.

# Verification
  * Ipconfig shows correct addressing scheme
  * Pings succeeded to domain controller
  * Hostname shows as Workstation1
  * System properties shows that this client machine is connected to **lab.local** domain

![Static IP Addressing Scheme](/docs/images/W11IP.png) 
![Ping to DC](/docs/images/Ping.png)
![Ipconfig Command Prompt](/docs/images/IPconfig2.png)
![System Properties](/docs/images/Sysproperties.png)
![About](/docs/images/About.png)

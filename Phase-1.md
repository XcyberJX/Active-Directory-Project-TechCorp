# Phase 1 - Lab Environment Setup
To begin I install Oracle Virtualbox, which will be the hypervisor used to create 2 virtual machines. One will be used for a 2022 Windows Server which will then be promoted to a Domain Controller (Named TechCorp DC). The other will be the client workstation with the Operating System being Windows 11 (Named TechCorp ClientWorkstation). 

<img width="440" height="175" alt="2 virtual machines" src="https://github.com/user-attachments/assets/f8ef7277-d3e4-448c-a974-7289b2a20895" />

The screenshots below provide setup details for each designated category. The setup for each virtual machine you create is crucial because it allows you to be flexible without risk.
 # TechCorp DC Setup:
<img width="920" height="982" alt="Domain Controller Setup" src="https://github.com/user-attachments/assets/f7d14ffa-0154-4a51-8812-ce022e3900db" />
When you reach the startup be sure to login in as the administrator to ensure full access. Then, you will need to set a static IP address. (In this case 192.168.1.10) This will make the DC easy to reach and keep connectivity consistent. After that you will need to change the Domain Name to "TechCorp.local". Finally, you will now promote the server to a Domain Controller.

* <img width="255" height="125" alt="Domain Names Changed" src="https://github.com/user-attachments/assets/eb449a53-e026-4b28-b4e5-ad83cfa26fae" /> 
* <img width="992" height="340" alt="DC properties" src="https://github.com/user-attachments/assets/59829cc9-f295-4863-9eb3-2ae06b70c939" />

# TechCorp Client Setup:
<img width="1017" height="897" alt="Client Setup" src="https://github.com/user-attachments/assets/27fb02e9-e5d0-4e59-9f91-fd2ee0244f74" />
When you reach the login screen you want to make sure you login as an administrator and have the client join the Domain. You will also need to change the IP address as well as with the DNS server address. (In this case IP: 192.168.1.20 | DNS: 192.168.1.10). This ensures that you are able to communicate with the Domain Controller. To verify, you can open the command prompt on the client VM and run the command "nslookup TechCorp.local".

* <img width="580" height="242" alt="dns look up command" src="https://github.com/user-attachments/assets/d0437384-9b72-4cac-8c49-d2c144881928" />

The result should give me the IP address of the DC. (I was unable to come to a conclusion as to why it shows "DNS request timed out" at the moment, however, it still gave me the result needed for verification.) Lastly, I would now have the client join the Domain. The screenshot below should be the result you get for successfully joining.

* <img width="493" height="347" alt="successfully joined the domain" src="https://github.com/user-attachments/assets/b15b2de1-6d56-4d87-8720-0c2764a9ef4e" />






Next Phase > [Phase-2.md](Phase-2.md)

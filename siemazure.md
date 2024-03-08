# **Azure SIEM (Security Information Event Management) (Microsoft Sentinel)**

![alt text](image.png)

The image is a graphic representation of this laboratory, basically, a **Windows 10 Virtual Machine** in **Azure** is our honeypot, logs of attacks gonna be stored in **Log Analytics Workspace** and if want to see or query log information we uses **Azure Sentinel**.


 # [This laboratory is inspired in this YouTube video.](https://www.youtube.com/watch?v=RoZeVbbZ0o0)




# Azure resources deploy

# 1. VM Windows 10

![alt text](image-3.png) 
![alt text](image-2.png)
![alt text](image-4.png)

- When we creates the VM honeypot, in network settings, the option of security group, select create new, and add the next parameters, to allow inbound network traffic.

- After that configuration, we can use default parameters, to click in review and create to deploy VM.

# 2. Logs Analytics peering to Microsoft Defender for Cloud


![alt text](image-6.png)

- In **Log AnaLytics workspace** we need to peer the **Windows VM** 



 ![alt text](image-5.png)

 - In **Microsoft Defender for Cloud**, enable a plan for Servers, don't forget save.
# 3. Microsoft Azure Sentinel

 ![alt text](image-7.png)

 - Peer **Microsoft Azure Sentinel** to **Log AnaLytics workspace**
# 4. Login VM
![alt text](image-8.png)
![alt text](image-9.png)
![alt text](image-10.png)

- After login in our VM honeypot, we disable the Firewall, Domain, Private and Public Domains need to be in Off status.

# 5. Run a script in PowerShell

![alt text](image-11.png)
![alt text](image-12.png)

- This scrip uses a API from ipgeolocation.io, basically, creates a file with info about ip and location of attacks

# 6. Querys in Sentinel

![alt text](image-13.png)

- When ask to Sentinel about information, it provides geolocation and IP
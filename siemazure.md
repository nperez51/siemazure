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




# Week 3: Compute & Security Hardening 

## 🎯 Objective: Deploy secure Windows EC2 instance with proper network isolation 

*🏗️ Architecture*
```mermaid
graph LR  
    A[My Local Machine ] --> B[Internet];  
    B --> C{VPC Public Subnet};  
    C --> D[Security Group Inbound Port 3389];  
    D --> E[Windows Server 2019 EC2 Instance];  
    E -- Logs --> F[CloudWatch Logs];
``` 

### 🔧 Technologies: EC2, VPC, Security Groups, Systems Manager 

#### Windows EC2 Instance in the AWS Management Console  - Indicating the instance’s Name tag CSN-Bootcamp-week3 
![week3 - EC2 instance - CSN Bootcamp-week3](https://github.com/user-attachments/assets/96b6503c-f91e-4c80-b9c5-af48fc30459c)

#### Security Group: inbound rules allowing RDP (port 3389) only from your public IP address 
![week3 - security Group Inbound rules  allowing RDP port 3389](https://github.com/user-attachments/assets/a87da2bb-e0f7-43f9-9d93-6e26f22885ee)

#### Successful Remote Desktop (RDP) connection to the instance. 
![week3 - Remote Desktop RDP connection to the Windows EC2 Instance](https://github.com/user-attachments/assets/c5c49761-65e6-4812-8a43-9d3589aeb991)

### 📊 Key Learnings: 

* Defense in depth security 
* Network micro-segmentation 

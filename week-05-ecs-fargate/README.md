## Week 5: Container Orchestration 

**🎯 Objective: Deploy containerized applications using ECS Fargate** 

### 🏗️ Architecture: 
```mermaid
graph LR  
    A[Docker Image: nginx] --> B[ECS Task Definition];  
    B --> C[ECS Service];  
    C --> D[ECS Fargate Cluster];  
    D --> E[Public Subnet VPC];  
    E --> F[Security Group Inbound Port 80];  
    F -- Exposes Application --> G[Internet Access];
```

### 🔧 Technologies: ECS, Fargate, Docker, Application Load Balancer 

 #### ECS Cluster and Running Service (Initial Cluster View) 
![week5 - ECS Cluster and Running Service (Initial Cluster View)](https://github.com/user-attachments/assets/a629ec24-d9af-4fa8-80bb-8cb95efa34bd)

#### Task Definition with grafana/grafana Image and Port 3000 
![week5 - Task Definition with grafanagrafana Image and Port 3000](https://github.com/user-attachments/assets/3e61ba39-2500-48a3-99f6-94e5b642032f)

#### Security Group for Grafana access Port 3000 
![week5 - Security Group for Grafana access Port 3000](https://github.com/user-attachments/assets/899cc5f2-286f-48f5-94a0-9546a7ee6241)

#### ECS Cluster and Running Service 
![week5 - ECS Cluster and Running Service Health](https://github.com/user-attachments/assets/b76bafbb-40cf-4730-9767-fa5f4bb2451e)

#### Grafana Login Page 
![week5 - Grafana Login Page](https://github.com/user-attachments/assets/d7e0079f-8b0b-4a71-a932-e4a1e72ed456)

#### Grafana Welcome Page (successful logging) 
![week5 - Grafana Welcome Page](https://github.com/user-attachments/assets/98517d69-5343-4c3a-9c13-713a20fc2f02)

#### 📊 Key Learnings: 

  * Serverless container orchestration
  * Service discovery patterns
  * Container security best practices 

 

# Week 6: Database Integration & Data Management 

### 🎯 Objective: Deploy Metabase on Amazon ECS using Fargate and connect it to a PostgreSQL database hosted on Amazon RDS. This involves configuring database connectivity via environment variables and ensuring proper security group rules for communication. 

### 🏗️ Architecture: 
```mermaid
flowchart LR  
    subgraph VPC Default  
        ECS_SG[Metabase ECS Security Group]  
        RDS_SG[RDS PostgreSQL Security Group]

        ECS_Task[ECS Fargate Task Metabase] --> ECS_SG;  
        RDS_DB[RDS PostgreSQL Instance] --> RDS_SG;

        ECS_Task -- Private IP Access Port 3000 --> Internet;  
        ECS_Task -- Database Connection Port 5432 --> RDS_DB;

        ECS_SG -- Allow Inbound Port 3000 from Anywhere --> ECS_Task;  
        RDS_SG -- Allow Inbound Port 5432 from ECS_SG CIDR --> RDS_DB;  
    end

    style ECS_Task fill:#f9f,stroke:#333,stroke-width:2px  
    style RDS_DB fill:#9cf,stroke:#333,stroke-width:2px
```
### 🔧 Technologies: RDS PostgreSQL, ECS, Parameter Store, VPC Endpoints 

#### Meta RDS PostgreSQL Instance Details 
![week6 - Meta RDS PostgreSQL Instance Details](https://github.com/user-attachments/assets/335a4b78-4150-4cc1-b180-8aa35a8c6587)

#### Security Group Rules Allowing Traffic from ECS to RDS 
![week6 - Security Group Rules Allowing Traffic from ECS to RDS](https://github.com/user-attachments/assets/53ec3cc2-566a-493d-ae61-3c765f7a179f)

#### Metabase-Fargate-Cluster ECS Cluster and Running Service (Initial Cluster View) 
![week6 - Metabase-Fargate-Cluster ECS Cluster and Running Service (Initial Cluster View)](https://github.com/user-attachments/assets/a016319d-ca09-4e7b-9d21-7f313878c86f)

#### ECS Task Definition with metabase/metabase Image and Environment Variables 
![week6 - ECS Task Definition with metabasemetabase Image and Environment Variables](https://github.com/user-attachments/assets/11593030-4384-4414-b0fd-4cb6550d4930)
![week6 - ECS Task Definition with metabasemetabase Image and Environment Variables - 2](https://github.com/user-attachments/assets/687278ec-af87-42cf-b930-0446b5c6c9c1)
![week6 - ECS Task Definition with metabasemetabase Image and Environment Variables - 3](https://github.com/user-attachments/assets/df3ce3eb-9e11-42ce-abb4-7b1955e494d1)

#### Security Group Rules Allowing Traffic to ECS (Port 3000) 
![week6 - Security Group Rules Allowing Traffic to ECS (Port 3000)](https://github.com/user-attachments/assets/b146d84a-3478-46f9-a000-f4d44ad44905)

#### ECS Cluster and Running Service MetaBase
![week6 - ECS Cluster and Running Service MetaBase](https://github.com/user-attachments/assets/bc6e2ab7-9725-4fd1-be7c-4defe3c43e1a)

#### Metabase Setup Screen Confirming Successful Connection to the Database 
![week6 - Metabase Setup Screen Confirming Successful Connection to the Database](https://github.com/user-attachments/assets/6939f345-b8f4-45e7-89bc-9fb046e84b36)
![week6 - Metabase Setup Screen Confirming Successful Connection to the Database - 1](https://github.com/user-attachments/assets/3ebaf4b8-3245-4d14-ab7c-c5ae2944dabb)

### 📊 Key Learnings: 
  * Database security and encryption
  * Connection pooling optimization 

 

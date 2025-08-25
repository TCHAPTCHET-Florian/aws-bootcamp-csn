# Week 7: Observability & Performance Monitoring 

**🎯 Objective: Implement comprehensive monitoring with CloudWatch** 

**🏗️ Architecture:** 
```mermaid
graph LR  
    ECS_Service[ECS Service Nginx Fargate Task] --> Metrics[CloudWatch Metrics CPU, Memory];  
    ECS_Service -- Container Logs --> Logs[CloudWatch Logs];

    Metrics --> Dashboard[CloudWatch Dashboard];  
    Metrics --> Alarm[CloudWatch Alarm High CPU];  
    Alarm --> SNS[Amazon SNS Topic];  
    SNS --> Email[Email Notifications];
```
**🔧 Technologies**: CloudWatch, CloudWatch Dashboards, CloudWatch Alarms, CloudWatch Logs, ECS Nginx

#### ECS cluster and running service – Nginx container 
![week7 - ECS Cluster and Running Service - NGINX](https://github.com/user-attachments/assets/735bdb24-33fe-49ec-8e08-61406bbf4749)

#### CloudWatch dashboard displaying the CPU and Memory utilization widgets for your Nginx service. 
![week7 - CloudWatch dashboard displaying the CPU and Memory utilization widgets for your Nginx service](https://github.com/user-attachments/assets/dd6d7aec-528f-47b8-ade2-76bf4da0ebdb)

#### Load Nginx page... 
![week7 - Loading Nginx page](https://github.com/user-attachments/assets/618077f0-0982-4c70-86d6-094b05a1eb60)

#### CloudWatch Dashboard with metrics changed after loading Nginx page 
![week7 - CloudWatch Dashboard after loading Nginx page](https://github.com/user-attachments/assets/4ebc1e5c-380a-4f50-8202-cc5c8269ac88)

### 📊 Key Learnings: 
  * Proactive monitoring strategies
  * Cost-optimized scaling patterns 

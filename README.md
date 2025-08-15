# **AWS Cloud Bootcamp 2025 \- DevSecOps Journey**

*Sponsored by CloudSec Network (CSN)*

## **🚀 Overview**

This repository showcases my 10-week intensive AWS Cloud Bootcamp journey, demonstrating hands-on expertise in **cloud architecture, DevSecOps practices, and AI/ML integration**. Each week builds upon previous knowledge, culminating in a comprehensive understanding of enterprise-grade AWS solutions.

**Author**: Florian TCHAPTCHET NJOKWA

**Role**: DevSecOps Engineer & AI Enthusiast

**Certification Goal**: AWS Solutions Architect Professional

## **🎯 Learning Objectives Achieved**

* **Cloud Infrastructure**: Multi-VPC architectures, containerization, and serverless computing  
* **DevSecOps Integration**: Security-first approach with automated monitoring, compliance, and CI/CD  
* **AI/ML Enhancement**: Intelligent automation and data-driven insights across cloud operations  
* **Enterprise Architecture**: Scalable, resilient, and cost-optimized solutions adhering to best practices

## **📋 Weekly Project Structure**

| Week | Focus Area | Core Technologies | AI Enhancement (Bonus Task) |
| :---- | :---- | :---- | :---- |
| [Week 1](./week-1-foundation--governance/README.md) | Account Setup & Governance | AWS Organizations, IAM | AWS Config AI Compliance |
| [Week 2](./week-2-identity--access-management/README.md) | Identity & Access Management | AWS Identity Center, SSO | Intelligent IAM Policy Generator |
| [Week 3](./week-3-compute--security-hardening/README.md) | Compute & Security Hardening | EC2, Security Groups, RDP | CloudWatch AI Anomaly Detection |
| [Week 4](./week-4-multi-vpc-network-architecture/README.md) | Multi-VPC Network Architecture | VPC, Subnets, Peering | Network Insights & AI Analysis |
| [Week 5](./week-5-container-orchestration/README.md) | Container Orchestration | ECS Fargate, Docker | Container Image Vulnerability Scanning |
| [Week 6](./week-6-database-integration--data-management/README.md) | Database Integration & Data Management | RDS PostgreSQL, ECS | Amazon Comprehend Data Analysis |
| [Week 7](./week-7-observability--performance-monitoring/README.md) | Observability & Performance Monitoring | CloudWatch, Dashboards | Predictive Scaling with ML |
| [Week 8](./week-8-global-content-delivery/README.md) | Global Content Delivery | S3, CloudFront | Image Recognition with Rekognition |
| [Week 9](./week-9-dns-management--ssl-automation/README.md) | DNS Management & SSL Automation | Route 53, ACM | Automated SSL Renewal Bot |
| [Week 10](./week-10-serverless-event-driven-architecture/README.md/README.md) | Serverless Event-Driven Architecture | Lambda, S3 Events | Document Processing with Textract |
| [Capstone](./capstone-project-intelligent-devsecops-platform/README.md) | Full-Stack AI Platform | Multi-service Integration | End-to-End ML & DevSecOps | 🚧 |

## **📚 Detailed Weekly Breakdown**

### **Week 1: Foundation & Governance**

**🎯 Objective**: Establish a secure AWS account with proper governance for multi-account strategy.

**📁 Project**: [/week-01-account-setup](./week-01-account-setup/README.md)

**🏗️ Architecture**:

graph TD  
    A\[User/Learner\] \--\> B{Access AWS Console};  
    B \--\> C\[AWS Account Setup/Verification\];  
    C \--\> D\[Active AWS Account in AWS Cloud\];  
    D \--\> E\[Ready for Cloud Deployments\];

**🔧 Technologies**: AWS Account Management, AWS Management Console

**🤖 AI Enhancement (Bonus Task)**: Explored potential for **AWS Config AI Compliance** using Amazon Bedrock to analyze configuration drift and suggest intelligent remediation steps, moving towards proactive governance.

**📊 Key Learnings**:

* Understanding the importance of account setup as the cloud foundation.  
* Initial familiarity with the AWS Management Console.  
* Early considerations for cost management within the AWS Free Tier.

### **Week 2: Identity & Access Management**

**🎯 Objective**: Configure centralized identity management using AWS Identity Center for secure, least privilege access.

**📁 Project**: [/week-02-identity-center](./week-02-identity-center/README.md)

**🏗️ Architecture**:

graph TD  
    A\[User/Admin\] \--\> B\[AWS Identity Center (SSO)\];  
    B \--\> C\[Create User (e.g., security-auditor)\];  
    B \--\> D\[Assign Predefined Permission Set (SecurityAudit)\];  
    D \--\> E\[Access AWS Resources with Least Privilege\];

graph TD
    A[User/Admin] --> B[AWS Identity Center (SSO)];
    B --> C[Create User (e.g., security-auditor)];
    B --> D[Assign Predefined Permission Set (SecurityAudit)];
    D --> E[Access AWS Resources with Least Privilege];

**🔧 Technologies**: AWS Identity Center (formerly SSO), Permission Sets, IAM Policies

**🤖 AI Enhancement (Bonus Task)**: Researched integrating with **Amazon Bedrock** to create an intelligent IAM policy generator that analyzes user behavior patterns and suggests optimal permission boundaries, enhancing a zero-trust model.

**📊 Key Learnings**:

* Implementing centralized identity management for streamlined access.  
* Applying the principle of least privilege through permission sets.  
* Understanding the security benefits of single sign-on (SSO).

### **Week 3: Compute & Security Hardening**

**🎯 Objective**: Deploy a secure Windows EC2 instance with proper network isolation and controlled access.

**📁 Project**: [/week-03-ec2-security](./week-03-ec2-security/README.md)

**🏗️ Architecture**:

graph TD  
    A\[My Local Machine\] \--\> B\[Internet\];  
    B \--\> C{VPC (Public Subnet)};  
    C \--\> D\[Security Group (Inbound Port 3389)\];  
    D \--\> E\[Windows Server 2019 EC2 Instance\];  
    E \-- Logs \--\> F\[CloudWatch Logs\];

**🔧 Technologies**: EC2, VPC, Security Groups, Remote Desktop Protocol (RDP), Key Pairs

**🤖 AI Enhancement (Bonus Task)**: Investigated **CloudWatch Anomaly Detection** using machine learning to identify unusual RDP connection patterns and automatically trigger security responses, enhancing real-time threat posture.

**📊 Key Learnings**:

* Securely deploying virtual machines in the cloud.  
* Configuring security groups as virtual firewalls for granular access control.  
* Importance of SSH keys/RDP access management and troubleshooting connectivity issues.

### **Week 4: Multi-VPC Network Architecture**

**🎯 Objective**: Create an interconnected network architecture by peering two isolated VPCs with proper routing.

**📁 Project**: [/week-04-vpc-peering](./week-04-vpc-peering/README.md)

**🏗️ Architecture**:

graph TD  
    subgraph VPC-A (10.10.0.0/16)  
        A\_Pub\[Public Subnet\]  
        A\_Priv\[Private Subnet\]  
        A\_RT\[Route Table A\]  
        A\_Pub \--\> A\_RT  
        A\_Priv \--\> A\_RT  
    end

    subgraph VPC-B (10.20.0.0/16)  
        B\_Pub\[Public Subnet\]  
        B\_Priv\[Private Subnet\]  
        B\_RT\[Route Table B\]  
        B\_Pub \--\> B\_RT  
        B\_Priv \--\> B\_RT  
    end

    A\_RT \-- Traffic for 10.20.0.0/16 \--\> PC\[VPC Peering Connection\];  
    PC \-- Traffic for 10.10.0.0/16 \--\> B\_RT;

**🔧 Technologies**: VPC, Subnets, VPC Peering, Route Tables, Security Groups

**🤖 AI Enhancement (Bonus Task)**: Explored **Network Traffic Analysis** using Amazon VPC Flow Logs combined with AI-powered insights to optimize routing, detect anomalies, and identify security threats across peered networks.

😰 Challenge Overcome:  
Initially struggled with VPC peering connectivity. The frustration was real when I couldn't get the instances in different VPCs to communicate\! The key insight came from methodically debugging the route tables – I realized I hadn't added return routes in both VPCs pointing to the peering connection. After implementing bidirectional routes and ensuring security group rules allowed inter-VPC traffic, communication flowed smoothly. It highlighted the critical importance of symmetric routing and detailed network troubleshooting in complex cloud environments.  
**📊 Key Learnings**:

* Designing segmented and isolated network environments with VPCs.  
* Establishing private, high-bandwidth communication between VPCs using peering.  
* Mastering route table configurations for effective traffic flow and troubleshooting network issues.

### **Week 5: Container Orchestration**

**🎯 Objective**: Deploy a simple containerized application (Nginx) using Amazon ECS with Fargate for serverless container management.

**📁 Project**: [/week-05-ecs-fargate](./week-05-ecs-fargate/README.md)

**🏗️ Architecture**:

graph TD  
    A\[Docker Image: nginx\] \--\> B\[ECS Task Definition\];  
    B \--\> C\[ECS Service\];  
    C \--\> D\[ECS Fargate Cluster\];  
    D \--\> E\[Public Subnet (VPC)\];  
    E \--\> F\[Security Group (Inbound Port 80)\];  
    F \-- Exposes Application \--\> G\[Internet Access\];

**🔧 Technologies**: ECS, Fargate, Docker, Task Definitions, ECS Services, Security Groups

**🤖 AI Enhancement (Bonus Task)**: Integrated a conceptual **Container Vulnerability Scanning** pipeline using Amazon Inspector and AI-powered risk assessment to prioritize security patches, demonstrating DevSecOps principles in container deployments.

**📊 Key Learnings**:

* Deploying and managing containers without managing servers using Fargate.  
* Defining container configurations and resource allocations in Task Definitions.  
* Exposing containerized applications to the internet via public subnets and security groups.

### **Week 6: Database Integration & Data Management**

**🎯 Objective**: Deploy a containerized application (Metabase) on ECS Fargate and securely connect it to a PostgreSQL database hosted on Amazon RDS.

**📁 Project**: [/week-06-rds-integration](./week-06-rds-integration/README.md)

**🏗️ Architecture**:

graph TD  
    subgraph VPC (Default)  
        ECS\_SG\[Metabase ECS Security Group\]  
        RDS\_SG\[RDS PostgreSQL Security Group\]

        ECS\_Task\[ECS Fargate Task (Metabase)\] \--\> ECS\_SG;  
        RDS\_DB\[RDS PostgreSQL Instance\] \--\> RDS\_SG;

        ECS\_Task \-- Private IP Access (Port 3000\) \--\> Internet;  
        ECS\_Task \-- Database Connection (Port 5432\) \--\> RDS\_DB;

        ECS\_SG \-- Allow Inbound Port 3000 from Anywhere \--\> ECS\_Task;  
        RDS\_SG \-- Allow Inbound Port 5432 from ECS\_SG CIDR \--\> RDS\_DB;  
    end

    style ECS\_Task fill:\#f9f,stroke:\#333,stroke-width:2px  
    style RDS\_DB fill:\#9cf,stroke:\#333,stroke-width:2px

**🔧 Technologies**: RDS PostgreSQL, ECS Fargate, Docker, Environment Variables, VPC Security Groups

**🤖 AI Enhancement (Bonus Task)**: Explored **Amazon Comprehend Data Analysis** to analyze database query patterns and provide intelligent insights about data usage and optimization opportunities, moving towards data-driven application tuning.

**📊 Key Learnings**:

* Integrating containerized applications with managed database services.  
* Securely connecting application tasks to databases within a VPC using private IPs.  
* Configuring environment variables for sensitive database credentials.

### **Week 7: Observability & Performance Monitoring**

**🎯 Objective**: Implement comprehensive monitoring for an ECS service using AWS CloudWatch, including custom dashboards and alarms.

**📁 Project**: [/week-07-monitoring](./week-07-monitoring/README.md)

**🏗️ Architecture**:

graph TD  
    ECS\_Service\[ECS Service (Nginx Fargate Task)\] \--\> Metrics\[CloudWatch Metrics (CPU, Memory)\];  
    ECS\_Service \-- Container Logs \--\> Logs\[CloudWatch Logs\];

    Metrics \--\> Dashboard\[CloudWatch Dashboard\];  
    Metrics \--\> Alarm\[CloudWatch Alarm (High CPU)\];  
    Alarm \--\> SNS\[Amazon SNS Topic\];  
    SNS \--\> Email\[Email Notifications\];

**🔧 Technologies**: CloudWatch, CloudWatch Dashboards, CloudWatch Alarms, CloudWatch Logs, Amazon SNS, ECS Fargate

**🤖 AI Enhancement (Bonus Task)**: Researched **Machine Learning-powered Predictive Scaling** using Amazon Forecast to anticipate traffic patterns and automatically adjust container capacity, moving towards intelligent infrastructure scaling.

**📊 Key Learnings**:

* Establishing robust monitoring for containerized applications.  
* Visualizing application performance with custom CloudWatch Dashboards.  
* Setting up proactive alerts using CloudWatch Alarms to respond to operational events.  
* Centralizing container logs for effective troubleshooting.

### **Week 8: Global Content Delivery**

**🎯 Objective**: Deploy a globally distributed static website using Amazon S3 for storage and CloudFront for content delivery.

**📁 Project**: [/week-08-cdn-deployment](./week-08-cdn-deployment/README.md)

**🏗️ Architecture**:

graph TD  
    A\[User (Global)\] \--\> B\[CloudFront Edge Location\];  
    B \-- Cache Hit \--\> A;  
    B \-- Cache Miss \--\> C\[CloudFront Origin (S3 Bucket)\];  
    C \--\> B;  
    S3\[S3 Bucket \- Static Website Hosting\] \--\> C;  
    S3 \-- Public Access via OAC Policy \--\> B;

**🔧 Technologies**: S3, CloudFront, Static Website Hosting, Origin Access Control (OAC), S3 Bucket Policies

**🤖 AI Enhancement (Bonus Task)**: Explored **Amazon Rekognition integration** to automatically analyze and tag images uploaded to the S3 bucket, demonstrating an intelligent content management system.

😰 Challenge Overcome:  
Initially faced the dreaded "Access Denied" error when trying to load the website via CloudFront\! This was a classic permissions issue. I learned that simply enabling "public access" on the S3 bucket isn't enough when using CloudFront's recommended Origin Access Control (OAC). The fix involved replacing my S3 bucket policy with the precise policy generated by CloudFront's OAC. This experience highlighted the importance of specific IAM permissions for service-to-service communication and the propagation time for CloudFront distributions. It's frustrating when you're stuck, but overcoming these specific access issues really cemented my understanding of AWS security models.  
**📊 Key Learnings**:

* Hosting static content efficiently and cost-effectively on S3.  
* Accelerating content delivery and enhancing security with CloudFront.  
* Understanding and correctly configuring S3 bucket policies with CloudFront Origin Access Control.

### **Week 9: DNS Management & SSL Automation**

**🎯 Objective**: Implement a custom domain and secure it with HTTPS using Route 53, ACM, and CloudFront.

**📁 Project**: [/week-09-dns-ssl](./week-09-dns-ssl/)

**🏗️ Architecture**:

graph TD  
    A\[User Browser\] \-- HTTPS Request (Custom Domain) \--\> B\[CloudFront Edge Location\];  
    B \-- Uses \--\> C\[ACM SSL Certificate (Issued)\];  
    C \-- Validated via \--\> D\[Route 53 DNS Records (CNAME)\];  
    B \-- For Content \--\> E\[S3 Origin\];  
    E \--\> B;  
    B \--\> A;

**🔧 Technologies**: Route 53, Amazon Certificate Manager (ACM), DNS Validation, Custom Domains, HTTPS

**🤖 AI Enhancement (Bonus Task)**: Investigated an **Intelligent SSL Certificate Monitoring Bot** using Lambda and Amazon Bedrock to predict certificate expiration patterns and proactively manage renewals with natural language notifications, demonstrating automated security governance.

**📊 Key Learnings**:

* Registering and managing custom domains with Route 53\.  
* Obtaining and validating free SSL/TLS certificates using ACM.  
* Integrating SSL certificates with CloudFront to enable HTTPS for custom domains.  
* Understanding DNS propagation and certificate validation processes.

### **Week 10: Serverless Event-Driven Architecture**

**🎯 Objective**: Build a serverless document processing pipeline where an S3 upload triggers a Lambda function for automated processing.

**📁 Project**: [/week-10-serverless-pipeline](./week-10-serverless-pipeline/README.md)

**🏗️ Architecture**:

graph TD  
    A\[User\] \--\> B\[S3 Bucket: Upload File\];  
    B \-- Object Created Event \--\> C\[Lambda Function: S3FileUploadLogger\];  
    C \-- Write Logs \--\> D\[CloudWatch Logs\];

**🔧 Technologies**: AWS Lambda, Amazon S3 Event Notifications, CloudWatch Logs, Python

**🤖 AI Integration**: Proposed a full AI pipeline using **Amazon Textract** for document OCR, **Amazon Comprehend** for sentiment analysis/entity extraction, and intelligent document classification with automatic routing based on content analysis, showcasing real-world AI applications.

**📊 Key Learnings**:

* Designing and implementing event-driven serverless architectures.  
* Configuring S3 bucket events to automatically invoke Lambda functions.  
* Writing Lambda functions to process S3 event payloads and log output to CloudWatch Logs.  
* Understanding the power of serverless for automated workflows.

## **🎓 Capstone Project: Intelligent DevSecOps Platform**

**🎯 Objective**: To build a comprehensive, AI-enhanced DevSecOps platform that integrates and demonstrates key concepts from across the bootcamp, focusing on security, automation, and intelligent operations.

**📁 Project**: [/capstone-devsecops-platform](./capstone-devsecops-platform/README.md)

**💡 Project Vision**: This capstone aims to create a fully operational framework where applications are deployed securely, monitored intelligently, and managed with automation driven by AI insights. It bridges the gap between traditional DevSecOps practices and the cutting-edge capabilities of AI/ML in cloud environments.

**🏗️ Full Architecture**:

graph TD  
    subgraph Multi-Account AWS Organization  
        subgraph Development Account  
            DevApp\[Application Development\]  
            DevCI\[CI/CD Pipeline\]  
            DevDB\[RDS Dev DB\]  
            DevLogs\[CloudWatch Logs\]  
            DevApp \--\> DevLogs;  
            DevCI \--\> DevApp;  
            DevApp \--\> DevDB;  
        end

        subgraph Security Account  
            SecHub\[AWS Security Hub\]  
            GuardDuty\[Amazon GuardDuty\]  
            Config\[AWS Config\]  
            AI\_Sec\_Analysis\[AI Security Analysis (SageMaker/Bedrock)\]  
            GuardDuty \--\> AI\_Sec\_Analysis;  
            Config \--\> AI\_Sec\_Analysis;  
            SecurityHub \--\> AI\_Sec\_Analysis;  
            SecHub \-- Alerts \--\> Lambda\_Sec\[Security Remediation Lambda\];  
        end

        subgraph Production Account  
            ProdApp\[Production Application (ECS Fargate)\]  
            ProdDB\[RDS Production DB (Multi-AZ)\]  
            ProdCDN\[CloudFront \+ WAF\]  
            ProdDNS\[Route 53 DNS\]  
            ProdApp \--\> ProdDB;  
            ProdCDN \--\> ProdApp;  
            ProdDNS \--\> ProdCDN;  
            ProdLogs\[CloudWatch Logs\];  
            ProdApp \--\> ProdLogs;  
            DR\[Disaster Recovery (Cross-Region/Backup)\];  
            ProdDB \--\> DR;  
        end

        subgraph Shared Services / AI Platform  
            SageMaker\[Amazon SageMaker: Custom ML Models\]  
            Bedrock\[Amazon Bedrock: GenAI Insights\]  
            Comprehend\[Amazon Comprehend: Log/Text Analysis\]  
            Lambda\_Ops\[Lambda for Operational Automation\]  
            SQS\[Amazon SQS/SNS\];  
            API\_GW\[API Gateway\];  
        end  
    end

    DevCI \-- Deploy to Prod \--\> ProdApp;  
    ProdLogs \--\> Comprehend;  
    Comprehend \-- Insights \--\> SQS;  
    SQS \--\> Lambda\_Ops;  
    Lambda\_Ops \-- Automate/Notify \--\> ProdApp;  
    AI\_Sec\_Analysis \-- Alerts \--\> SQS;  
    SQS \--\> Lambda\_Sec;  
    Lambda\_Sec \-- Remediate \--\> DevApp;  
    API\_GW \--\> SageMaker;  
    SageMaker \-- Predictive Analytics \--\> Lambda\_Ops;

**🔧 Technologies**: All services from Weeks 1-10, plus:

* **Compute:** AWS Lambda, ECS Fargate, EC2  
* **Networking:** VPC, Subnets, Peering, Route 53, CloudFront  
* **Databases:** Amazon RDS (PostgreSQL), DynamoDB  
* **Security:** AWS Security Hub, Amazon GuardDuty, AWS Config, AWS WAF, IAM, AWS Identity Center, AWS Key Management Service (KMS)  
* **Monitoring & Logging:** Amazon CloudWatch (Logs, Metrics, Alarms, Dashboards), Amazon SNS  
* **Automation & CI/CD:** AWS CodePipeline, AWS CodeBuild, AWS CodeDeploy (conceptual), S3 Events  
* **AI/ML Services:** Amazon SageMaker, Amazon Bedrock, Amazon Comprehend, Amazon Textract, Amazon Forecast, Amazon Rekognition (integrating bonus tasks)

**🤖 AI Innovation Highlights**:

* **Intelligent Threat Detection & Remediation:** Leverage SageMaker to train custom ML models on security logs (GuardDuty, CloudTrail, VPC Flow Logs) to identify sophisticated threats. Use Bedrock to generate natural language explanations for detected anomalies and suggest automated remediation actions via Lambda.  
* **Predictive Resource Optimization:** Apply Amazon Forecast to analyze historical resource utilization data (from CloudWatch) for applications and databases, enabling proactive scaling and cost optimization.  
* **Automated Security Compliance:** Utilize AWS Config with AI-powered analysis (Bedrock) to continuously monitor resource configurations against compliance baselines, automatically flagging deviations and recommending fixes.  
* **Intelligent Incident Response:** Implement a system where CloudWatch Alarms or GuardDuty findings trigger Lambda functions that use Bedrock to summarize incidents and propose initial diagnostic steps or automated fixes.  
* **AI-Enhanced Observability:** Use Amazon Comprehend to perform sentiment analysis or entity extraction on application logs, identifying trends in user feedback or critical error patterns. Incorporate Rekognition for image/video content analysis in specific use cases.

**📊 Key Learnings & Skills Demonstrated (Capstone)**:

* **End-to-End Cloud Solution Design:** Architecting a complex, multi-service, multi-account solution.  
* **Advanced DevSecOps Practices:** Implementing automated security, CI/CD, and governance at scale.  
* **Practical AI/ML Integration:** Applying various AWS AI services to enhance operational efficiency, security, and decision-making.  
* **Cross-Service Communication & Integration:** Orchestrating complex workflows between diverse AWS services.  
* **Cost Optimization & Resilience:** Designing for efficiency, high availability, and disaster recovery.

## **🛠️ DevSecOps Best Practices Implemented (Overall)**

### **Security First**

* ✅ Least privilege access patterns (IAM, Identity Center)  
* ✅ Network isolation and micro-segmentation (VPC, Security Groups, NACLs)  
* ✅ Encryption in transit and at rest (RDS, S3, SSL with ACM)  
* ✅ Automated compliance monitoring (Config \- conceptual)  
* ✅ Vulnerability scanning and remediation (Inspector \- conceptual)

### **Operational Excellence**

* ✅ Infrastructure as Code (Conceptual for the overall structure)  
* ✅ Automated deployment pipelines (ECS, S3 Triggers)  
* ✅ Comprehensive monitoring and alerting (CloudWatch)  
* ✅ Disaster recovery and business continuity (RDS Multi-AZ, CloudFront)  
* ✅ Cost optimization and governance (Monitoring, Fargate)

### **AI/ML Integration**

* ✅ Intelligent automation and decision-making  
* ✅ Predictive analytics for infrastructure planning  
* ✅ Natural language interfaces for complex operations  
* ✅ Automated threat detection and response  
* ✅ Data-driven insights and optimization

## **📈 Skills Demonstrated**

**Cloud Architecture**: Multi-account strategies, VPC design, hybrid connectivity, global distribution, high availability, disaster recovery.

**DevSecOps**: CI/CD automation, security scanning, compliance monitoring, incident response, automated governance, infrastructure as code principles.

**AI/ML Engineering**: Service integration, model deployment, data pipeline orchestration, intelligent automation, natural language processing, computer vision.

**Leadership & Problem-Solving**: Problem-solving under pressure, systematic troubleshooting, knowledge sharing, continuous learning, innovation mindset, critical thinking.

## **🎯 Certification Journey**

This bootcamp directly prepares for:

* **AWS Solutions Architect Professional**  
* **AWS DevOps Engineer Professional**  
* **AWS Security Specialty**

## **📞 Connect With Me**

**Florian TCHAPTCHET NJOKWA** 📧 floriantchaptchet@gmail.com

🔗 [LinkedIn](https://linkedin.com/in/florian-tchaptchet)

🐙 [GitHub](https://github.com/florian-tchaptchet)

*"Bridging the gap between traditional infrastructure and intelligent, AI-enhanced cloud solutions."*

## **📄 License**

This project is licensed under the MIT License \- see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

**⭐ If you find this repository helpful for your AWS journey, please consider giving it a star\!**

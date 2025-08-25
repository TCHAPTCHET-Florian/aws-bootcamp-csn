### **Week 2: Identity & Access Management**

**🎯 Objective: Configure centralized identity management with least privilege access** 

### 🏗️ Architecture: 

```mermaid
graph LR  
    A[User/Admin] --> B[AWS Identity Center SSO];  
    B --> C[Create User e.g., security-auditor];  
    B --> D[Assign Predefined Permission Set SecurityAudit];  
    D --> E[Access AWS Resources with Least Privilege];
```

### 🔧 Technologies: AWS Identity Center, Permission Sets

 
![week2 - ASW IAM - Identity Center](https://github.com/user-attachments/assets/fd1be9e1-6987-45dd-8e7a-569b7fc12c2d)

 
### 📊 Key Learnings: 

* Zero-trust security model 

* Federation best practices 

- Least privilege access patterns 


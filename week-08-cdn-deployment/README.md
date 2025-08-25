# Week 8: Global Content Delivery 

**🎯 Objective: Deploy globally distributed static website with cloud front** 

**🏗️ Architecture:** 
```mermaid
flowchart LR  
    A[User Global] --> B[CloudFront Edge Location];  
    B -- Cache Hit --> A;  
    B -- Cache Miss --> C[CloudFront Origin S3 Bucket];  
    C --> B;  
    S3[S3 Bucket - Static Website Hosting] --> C;  
    S3 -- Public Access via OAC Policy --> B;
```
#### Static Website Hosting for my chapy-personal-portfolio 
![week8 - Static Website Hosting for my chapy-personal-portfolio](https://github.com/user-attachments/assets/c9f77e45-a366-4ee9-be57-8e4f95754ddc)

#### Bucket Policy 
![week8 - Bucket Policy](https://github.com/user-attachments/assets/68b2439f-451a-4f89-96b3-1ea16e283767)

#### CloudFront distribution setting 
![week8 - CloudFront distribution setting](https://github.com/user-attachments/assets/5fceeaa4-f414-4b55-aa19-0a73fd91d169)

#### CloudFront demo 
![week8 - CloudFront demo link](https://github.com/user-attachments/assets/913101bc-9b65-4880-b456-6f5339e48f07)

😰 *Challenge Overcome:* Encountered caching issues where updates weren't reflecting immediately. Learned about CloudFront invalidation strategies and implemented cache-control headers properly to balance performance and content freshness. 

### 📊 Key Learnings: 
  * content delivery network (CDN)
  * Global edge computing patterns
  * Cache optimization strategies 

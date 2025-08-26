# Week 9: DNS Management & SSL Automation 

**🎯 Objective: Implement automated certificate management with custom domain** 

**🏗️ Architecture:** 
```mermaid
graph LR  
    A[User Browser] -- HTTPS Request Custom Domain --> B[CloudFront Edge Location];  
    B -- Uses --> C[ACM SSL Certificate Issued];  
    C -- Validated via --> D[Route 53 DNS Records CNAME];  
    B -- For Content --> E[S3 Origin];  
    E --> B;  
    B --> A;
``` 

 #### Domain Registration and Route 53 - Giving My Site a Home 
 ![week9 - Domain Registration and Route 53 - Giving My Site a Home](https://github.com/user-attachments/assets/452b0ff5-7acc-4fd7-bca0-34e72b1a8980)


_'This was my first time registering a domain and connecting it to AWS Route 53. It felt like a fundamental step in making my website truly mine. Porkbun was a straightforward way to get a domain without hidden fees, and then updating the nameservers in Route 53 was the critical link. It's like telling the internet, "Hey, for this domain, come to AWS for directions!" This step really solidified my understanding of how DNS works in the cloud.'_ 

 #### SSL Certificate - The Padlock of Trust 
![week9 - SSL Certificate - The Padlock of Trust](https://github.com/user-attachments/assets/ae6b2c99-47a5-4b9b-9f78-0a2e209b3889)

Securing my website with HTTPS was a non-negotiable. Users expect it, and search engines prefer it. AWS Certificate Manager (ACM) made getting a free SSL certificate incredibly easy. The DNS validation method in Route 53 was a neat trick – it automatically added the necessary CNAME records, proving I owned the domain without me having to manually mess with DNS. This step was crucial for building trust and ensuring encrypted communication for my website visitors. 

#### CloudFront Integration and HTTPS - The Final Polish 

This was the grand finale! Attaching the newly issued SSL certificate to my CloudFront distribution was the last piece of the puzzle. It meant that all traffic to my custom domain would now be served securely over HTTPS, leveraging CloudFront's global network. It was incredibly satisfying to type my custom domain into the browser and see the website load with the secure padlock, knowing that all the pieces of my AWS architecture were now working together seamlessly. 
![week9 - CloudFront Integration and HTTPS - The Final Polish](https://github.com/user-attachments/assets/25ccfa4e-607c-4e9d-a4b7-eadfa044ce24)

#### On Chrome browser 
![week9 - CloudFront Integration and HTTPS - On Chrome browser](https://github.com/user-attachments/assets/672601f1-7d91-487f-b688-3d84d933e9ef)

#### On Microsoft Edge 
![week9 - CloudFront Integration and HTTPS - On Microsoft Edge](https://github.com/user-attachments/assets/15db4fca-953a-4114-8e62-7c1451a43366)

 

 

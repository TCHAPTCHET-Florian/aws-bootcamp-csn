## Week 4: Multi-VPC Network Architecture 

**🎯 Objective: Create interconnected VPC architecture with proper routing** 

**🏗️ Architecture**:

```mermaid
graph RL  
    subgraph VPC-A 10.10.0.0/16  
        A_Pub[Public Subnet]  
        A_Priv[Private Subnet]  
        A_RT[Route Table A]  
        A_Pub --> A_RT  
        A_Priv --> A_RT  
    end
    subgraph VPC-B 10.20.0.0/16  
        B_Pub[Public Subnet]  
        B_Priv[Private Subnet]  
        B_RT[Route Table B]  
        B_Pub --> B_RT  
        B_Priv --> B_RT  
    end

    A_RT -- Traffic for 10.20.0.0/16 --> PC[VPC Peering Connection];  
    PC -- Traffic for 10.10.0.0/16 --> B_RT;
```

**🔧 Technologies**: VPC, Subnets, VPC Peering, Route Tables, Security Groups

#### The two VPCs and their CIDR blocks: VPC-CSN-A and VPC-CSN-B 
![week4 - Virtual Private Cloud A and B with their CIDR block](https://github.com/user-attachments/assets/aa7718dc-68ca-4612-87af-2bf56f67b081)

#### VPC-CSN-A        10.10.0.0/16 
![week4 - Virtual Private Cloud A + Public and Private Subnets](https://github.com/user-attachments/assets/cca76228-f3f2-4736-9b9d-4371ea5c31f6)

#### VPC-CSN-A        Subnets 
![week4 - Virtual Private Cloud A and Private and Public Network](https://github.com/user-attachments/assets/02f1478e-d850-46aa-9393-759264ec018d)

#### VPC-CSN-B        10.20.0.0/16 
![week4 - Virtual Private Cloud B + Public and Private Subnets](https://github.com/user-attachments/assets/1e69ec11-7b31-4bf4-8f63-0815028d5f04)

#### VPC-CSN-B    - Subnets 
![week4 - Virtual Private Cloud B and Private and Public Subnets](https://github.com/user-attachments/assets/3c192678-f1ca-4f78-bf9f-421614cee767)

#### The VPC-A-to-B-Peering, peering connection in Active status 
![week4 - Virtual Private Cloud Peering connection with Active status](https://github.com/user-attachments/assets/20c41662-9872-4d42-8389-0bc8456a6a62)

#### The route tables for the VPC-CSN-A with routes pointing to the VPC-CSN-B CIDR block through the peering connection. 
![week4 - VPC A Route Table to VPC B](https://github.com/user-attachments/assets/72e55028-9da5-4037-991e-593af287b50f)

#### The route tables for the VPC-CSN-B with routes pointing to the VPC-CSN-A CIDR block through the peering connection. 
![week4 - VPC B Route Table to VPC A](https://github.com/user-attachments/assets/e28585d9-4bdd-4b27-970a-fac3157bf485)

#### 📊 Key Learnings: 

  * Network troubleshooting methodology 
  * Symmetric routing importance 

VPC design patterns 

 

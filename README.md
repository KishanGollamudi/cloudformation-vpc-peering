# 🛠️ Fully Automated AWS VPC Peering + EC2 Setup via CloudFormation

## 📌 Project Overview

This project automates the setup of a **complete multi-VPC network architecture** using **AWS CloudFormation**. It includes VPC creation, subnets, route tables, internet gateways, EC2 instances with Ubuntu OS, and VPC peering — all deployed end-to-end with Infrastructure as Code (**IaC**) and zero manual configuration.

---

## 🧱 What’s Built via CloudFormation

✅ **Two VPCs (A and B)**  
- VPC A CIDR: `10.0.0.0/16`  
- VPC B CIDR: `192.168.0.0/16`  
- Created using CloudFormation templates

✅ **Components Automatically Provisioned in Each VPC**  
- Public and Private Subnets  
- Route Tables and Associations  
- Internet Gateways and NAT Gateways (if used)  
- Security Groups  
- Elastic IPs (for public EC2)  

✅ **EC2 Instances (Ubuntu OS)**  
- 1 Public EC2 Instance in each VPC  
- 1 Private EC2 Instance in each VPC  
- Ubuntu AMI (Amazon Linux replaced with Ubuntu)  
- Connected to respective subnets  
- Key pair setup for secure SSH access

✅ **VPC Peering Setup**  
- Peering connection created between VPC A and VPC B  
- Route tables modified to enable cross-VPC private communication  

✅ **Secure Access Flow**  
- SSH into Public EC2 (Bastion) → Reach Private EC2  
- Test private subnet connectivity and file transfers  



### 🔧 Manual VPC Peering

While this project leverages **AWS CloudFormation** for full automation, it's important to understand how **VPC Peering** is configured manually in the AWS Console or via CLI. Manually setting up VPC peering involves creating a peering connection between two VPCs, accepting the request from the requester/acceptor side, and updating the **route tables** in each VPC to enable private IP communication. Additionally, **security groups** must be configured to allow traffic between peered subnets. This hands-on understanding is valuable for troubleshooting or hybrid scenarios where IaC is not yet implemented. However, in this project, all these steps are declaratively handled by CloudFormation templates to ensure reproducibility and scalability.

## Screenshots
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/86b59092-d3d5-4ea6-b76d-2bc80ca12500" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/71379f89-b87c-474a-b792-9699f9cd4ba1" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/08e8a6e0-8503-4e9d-96e5-5a2c376ebd79" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/f7fab2a6-25e4-4927-9077-dc94ac6dff7c" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/2f595493-982f-4a4d-abda-c5ae8dfc7f8a" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/3d6e52f6-dc0e-4d89-b53c-d80ae09fcc6c" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/d99e6b72-508f-40c9-aa53-ff70df3d7bbc" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/93f74f6a-8857-43c2-b0a4-cd3600e47e44" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/0d569c1d-e0df-4d20-835a-2b988db8bf23" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/ce8395b1-b113-47a1-9324-ba7bb95ea785" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/7a25d225-c5a9-4b75-8753-e217913d84fa" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/13c71870-ea48-4280-8801-dc4cbd71adcc" />

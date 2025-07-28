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

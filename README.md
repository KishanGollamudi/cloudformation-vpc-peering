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

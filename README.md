# 🛠️ AWS VPC Peering and EC2 Setup using CloudFormation (Fully Automated)

## 📌 Project Overview

This project demonstrates a **production-like AWS network setup** fully automated using **Infrastructure as Code (IaC)** via **AWS CloudFormation**. It provisions two isolated VPCs, deploys EC2 instances, establishes secure VPC peering, and enables private communication across subnets — all without any manual intervention.

---

## 🧱 What We’ll Build

✅ **Two VPCs**  
- VPC A (e.g., `10.0.0.0/16`)  
- VPC B (e.g., `10.1.0.0/16`)  

✅ **Public and Private Subnets** in Each VPC  
- Spread across different **Availability Zones**

✅ **EC2 Instances**  
- One **public** and one **private** instance in each VPC  
- Amazon Linux AMI used

✅ **VPC Peering Connection**  
- Enables communication between **private instances** in both VPCs

✅ **Route Table Configuration**  
- Route tables updated to support **cross-VPC traffic** securely

✅ **Test Connectivity**  
- Use **Bastion Host (Jumpbox)** in public subnet to SSH into private instances  
- Validate **file transfer** via `scp` or `rsync`

---

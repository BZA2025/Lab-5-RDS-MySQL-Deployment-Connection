# AWS / Johns Hopkins Labs  

## ⚡ Lab 5 – RDS MySQL Deployment & Connection  

### 🎯 Overview  
This lab focused on deploying an **Amazon RDS MySQL instance** in a secure, network-isolated environment and connecting to it from an **EC2 instance** using the MySQL CLI.  

### 🛠️ Architecture  
- **VPC:** Existing lab VPC (public + private subnets).  
- **RDS:** MySQL engine (db.t3.micro) deployed in private subnets.  
- **EC2 Instance:** Deployed in public subnet (used as bastion/DB client).  
- **Security Groups:**  
  - RDS SG → Allowed inbound `3306` only from EC2 SG.  
  - EC2 SG → Allowed inbound `22` (SSH) from my IP.  

### 🔧 Steps  
1. Provisioned RDS MySQL (private subnet, no public access).  
2. Configured Security Groups (least privilege).  
3. Connected from EC2 via MySQL CLI.  

### ✅ Key Skills  
- Secure database provisioning in AWS  
- Private subnet RDS deployment  
- Security group design (least privilege)  
- CLI-based DB connectivity & testing  

### ⏰ Time to Complete  
~2 – 2.5 hours  

### 📌 Notes  
- Real-world pattern: **DB private + jump-host EC2 access**  
- Reinforces **principle of least privilege**  

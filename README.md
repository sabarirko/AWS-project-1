# 🚀 AWS High Availability Web Application with EC2, RDS & Auto Scaling

## 📌 Project Overview
This project demonstrates how to deploy a **PHP + MySQL application** on AWS with high availability.  
The solution uses **EC2 Auto Scaling** for the web tier and **Amazon RDS** for the database tier, ensuring fault tolerance and scalability.  

---

## 🛠️ Tools & Technologies
- **Cloud Services:** AWS EC2, Auto Scaling, RDS (MySQL), Security Groups  
- **Database:** MySQL  
- **Web Server:** PHP, Apache  
- **Networking:** VPC, Security Groups, Load Balancer  

---

## ⚙️ Architecture
![Architecture Diagram](screenshots/architecture.png)  
*(Replace with your AWS High Availability architecture diagram)*  

---

## 🚀 Implementation Steps
1. **EC2 Instances**
   - Launched **multiple EC2 instances** to host the PHP website.  
   - Configured Apache + PHP runtime environment.  

2. **Auto Scaling**
   - Created an **Auto Scaling Group (ASG)** with minimum 2 instances.  
   - Ensured new EC2 instances launch automatically in case of failure or load increase.  

3. **Amazon RDS**
   - Provisioned **MySQL RDS instance** with the following:  
     - Database name: `intel`  
     - Table name: `data`  
     - Password: `intel123`  
   - Configured database security groups to allow access from EC2 instances only.  

4. **Application Configuration**
   - Updated PHP website config to point to the **RDS endpoint**.  
   - Verified secure connection between EC2 web servers and RDS.  

5. **Security Groups**
   - Allowed HTTP/HTTPS traffic to EC2 instances.  
   - Allowed only internal EC2 → RDS communication.

---

## ✅ Outcomes
- Highly available **web application** using EC2 Auto Scaling.  
- **Database decoupling** with Amazon RDS.  
- **Scalable and fault-tolerant** architecture using AWS native services.


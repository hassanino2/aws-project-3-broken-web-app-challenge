# AWS Project 3: Broken Web App Challenge

## 📌 Overview
In this challenge, I deployed a web application using a CloudFormation template that provisioned EC2 instances behind an Application Load Balancer (ALB). The app was intentionally broken. My task was to identify and fix four issues preventing it from being accessed through the ALB.

## 🛠️ Technologies Used
- AWS EC2
- Application Load Balancer (ALB)
- Target Groups
- Security Groups
- Route Tables & Internet Gateway (IGW)
- CloudFormation

## ✅ Issues Identified & Fixed

1. **No Registered Targets**  
   → Registered both EC2 instances manually to the target group.

2. **Incorrect Health Check Path**  
   → Corrected `/healthcheck.hmtl` to `/healthcheck.html` in target group health settings.

3. **EC2 Security Group Blocked HTTP**  
   → Added inbound rule to allow HTTP (port 80) traffic from the ALB.

4. **Route Table Missing Internet Gateway**  
   → Added route to IGW in the subnet’s route table to enable ALB to return responses.

## 🔍 Screenshots
- ALB DNS success in browser
<img width="1106" alt="Screenshot 2025-04-22 at 2 50 34 AM" src="https://github.com/user-attachments/assets/f2b5b485-ccd9-472d-ab8f-8e3e257c76f3" />
- Healthy targets in Target Group
<img width="1201" alt="healthytargets" src="https://github.com/user-attachments/assets/4397b9fb-096c-47bb-b0aa-9c764a6c0af5" />
- Route Table with IGW  
<img width="1191" alt="routetable" src="https://github.com/user-attachments/assets/dd0d68f8-78a6-4abe-9139-017c16057bc0" />
- Security Groups showing HTTP access
<img width="1171" alt="Screenshot 2025-04-22 at 2 51 51 AM" src="https://github.com/user-attachments/assets/80e4c930-9d28-4b95-910d-0c8e3408dfcc" />

## ✅ Outcome
The application successfully loaded through the ALB DNS name after fixing all issues. This challenge helped me practice real-world troubleshooting in a cloud environment.

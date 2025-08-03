# NGINX on AWS EC2 Deployment

This project demonstrates how I deployed a fully functional **NGINX web server** on an **AWS EC2 instance** and made it accessible via a custom domain using **Route 53**.

---

## 🚀 Project Overview
- Launch an EC2 instance running **Amazon Linux 2023**.
- Install and configure **NGINX** to serve a default webpage.
- Configure **Security Groups** to allow inbound traffic on **Port 80 (HTTP)**.
- Link a **custom domain** via **Route 53 A record** to the EC2 instance.
- Access the webpage using **nginx.hassanweb.net**.

---

## 🔹 Steps I Followed

### 1. EC2 Instance Setup
1. Created an **EC2 instance** in AWS.
2. Configured **Security Group** to allow:
   - **Port 22 (SSH)** for remote access.
   - **Port 80 (HTTP)** for web traffic.
3. Connected to the instance using SSH:
   ```bash
   ssh -i my-key.pem ec2-user@<public-ip>
2. Install and Start NGINX

sudo yum update -y
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
Verified by visiting the EC2 Public IP in the browser.

3. Configure Route 53
Registered a domain Abdirahmanweb.net.

Created an A record:

Name: nginx.Abdirahmanweb.net

Type: A

Value: EC2 Public IP

Waited for DNS propagation.

4. Test the Setup
Accessed the site via: http://nginx.Abdirahmanweb.net

Verified NGINX Welcome Page loads successfully.

📸 Project Outcome
Successfully hosted a web page on AWS using NGINX, accessible via a custom domain.

🛠️ Technologies Used
AWS EC2

Amazon Linux 2023

NGINX

Route 53

SSH
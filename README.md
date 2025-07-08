# Static Website Deployment on EC2 using HTTPD

This repository is created for deploying a **static website** on an **Amazon EC2 instance** using the **HTTPD (Apache)** web server.

## 📦 Project Overview

- Launch an EC2 instance (Amazon Linux 2 or Redhart )
- Install and configure `httpd` (Apache)
- Deploy static website files (HTML, CSS, JS)
- Configure security group to allow HTTP (port 80) access

## 🚀 Deployment Steps

1. **Launch EC2 Instance**
   - Use Amazon Linux 2
   - Attach a security group that allows HTTP (port 80)

2. **Connect to EC2 via SSH**
   ```bash
   ssh -i your-key.pem ec2-user@your-ec2-public-ip
   
3. **Install HTTPD**  
   ```bash
   sudo yum update -y
   sudo yum install httpd -y
   ```
4. **Clone the Repository**  
   ```bash
   git clone "repo url"
   ```

5. **Copy your files to the right path**
    ```bash
   sudo cp -r * /var/www/html/
   ```
    
7. **Start httpd**
    ```bash
    sudo systemctl start httpd
    ```
8. **Configure the security group to allow traffic from http and https.**
  
9. **Access the website using the public ip address**

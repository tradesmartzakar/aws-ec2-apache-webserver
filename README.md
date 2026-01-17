# aws-ec2-apache-webserver
Creating and Launching my first EC2 Instance
# AWS EC2 Apache Web Server Deployment

This project documents my first successful deployment of a live web server
on AWS using an EC2 instance and a bash User Data script.

## 🚀 Project Overview
I launched an Amazon EC2 instance, configured its public IP address to
serve a webpage, and automated the installation of an Apache web server.
I also connected directly to the instance via SSH to modify the web
content in real time.

## 🛠️ Technologies Used
- AWS EC2
- Amazon Linux
- Apache (httpd)
- Bash (User Data)
- SSH
- HTML

## ⚙️ Deployment Steps
1. Launched an EC2 instance in a public subnet
2. Configured the instance’s **public IP address** to display a webpage
3. Allowed HTTP traffic through **Security Group rules**
4. Used EC2 User Data to:
   - Update the system
   - Install Apache
   - Start and enable Apache on boot
   - Create an initial `index.html` file
5. Connected to the EC2 instance via **SSH**
6. Edited the live `index.html` file in `/var/www/html`
7. Verified changes by refreshing the public IP in a browser

## 🧪 Verification
The web server successfully served a custom webpage displaying:

> “Welcome to LUIT Academy  
> Your cloud journey starts here… Let’s Gooo!!!”

## 📸 Screenshots

### Live Webpage via EC2 Public IP
![Live EC2 Webpage](screenshots/01-live-ec2-webpage.png)

### Security Group Inbound Rules (HTTP / SSH / HTTPS)
![Security Group Inbound Rules](screenshots/03-security-group-inbound-rules.png)

### SSH Session Editing index.html on the Server
![Editing index.html](screenshots/04-ssh-edit-index-html.png)



## 📚 Key Learnings
- How to configure a public IP to serve web traffic
- How Security Groups control inbound access
- How Apache serves content from `/var/www/html`
- How to connect to and manage EC2 instances via SSH
- How to update production web content on a live server

## 🔜 Next Steps
- Add HTTPS with SSL
- Implement IAM roles
- Convert deployment to Infrastructure as Code (Terraform)
- Add Load Balancer and Auto Scaling

# AWS EC2 Web Server Deployment

## Project Overview

Successfully deployed and hosted a static website on an Amazon EC2 Linux instance using Apache HTTP Server.

This project demonstrates practical implementation of AWS cloud infrastructure, Linux server administration, networking, security configuration and web server deployment.

## Technologies & Services Used

- **Cloud Provider:** Amazon Web Services (AWS)
- **Compute Service:** Amazon EC2
- **Operating System:** Amazon Linux 2023
- **Web Server:** Apache HTTP Server (httpd)
- **Web Technologies:** HTML5 and CSS3
- **Remote Access:** SSH using PuTTY
- **Networking:** Public IPv4, Security Groups and HTTP

## Architecture

User Browser → Internet → AWS Security Group → EC2 Instance → Apache HTTP Server → HTML Website

## Implementation

### 1. EC2 Infrastructure Setup
- Provisioned an Amazon EC2 instance.
- Selected Amazon Linux 2023 as the operating system.
- Configured instance type and storage.
- Enabled public IPv4 connectivity.

### 2. Network & Security Configuration
Configured AWS Security Group inbound rules:

| Protocol | Port | Source | Purpose |
|---|---|---|---|
| SSH | 22 | My IP | Secure remote server access |
| HTTP | 80 | 0.0.0.0/0 | Public website access |

### 3. Linux Server Administration
- Established SSH connectivity using PuTTY.
- Authenticated using an SSH private key.
- Accessed the server using the `ec2-user` account.

### 4. Apache Web Server Installation

Installed and configured Apache HTTP Server.

Commands used:

```bash
sudo dnf update -y
sudo dnf install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
sudo systemctl status httpd
```

### 5. Website Development & Deployment
- Created a static webpage using HTML and CSS.
- Deployed the webpage inside Apache's document root: `/var/www/html/`.
- Configured appropriate file permissions.
- Restarted Apache to serve the deployed webpage.

### 6. Deployment Verification
- Verified Apache service status.
- Accessed the website using the EC2 instance's public IPv4 address.
- Successfully displayed the hosted webpage through a web browser using HTTP.

## Project Screenshots

### EC2 Instance
![EC2 Instance](screenshots/ec2-instance.png)

### Security Group Configuration
![Security Group](screenshots/security-group.png)

### Apache Service Status
![Apache Running](screenshots/apache-running.png)

### Deployed Website
![Deployed Website](screenshots/deployed-website.png)

## Skills Demonstrated

- AWS EC2 provisioning and management
- Linux command-line administration
- Apache web server installation and configuration
- SSH remote server connectivity
- AWS Security Group configuration
- Basic networking and HTTP communication
- Static website deployment
- Cloud infrastructure troubleshooting

## Future Enhancements

- Configure HTTPS using SSL/TLS.
- Implement domain name configuration.
- Explore Amazon CloudWatch monitoring.
- Automate deployment using scripts.
- Explore AWS S3 and CloudFront integration.

## Author

**Jewel Gabriel**

B.Tech Electronics and Communication Engineering




# AWS Static Website Hosting using EC2 and S3

## Minor Project – 1

**Static Website Hosting Using EC2 and S3 (Nginx)**

**Student:** Dalia Mahata  
**Project:** Static Website Hosting Using EC2 and S3  
**Platform:** Amazon Web Services  
**Server:** Nginx  
**Operating System:** Amazon Linux 2023  
**Submission Date:** 04 September 2026

## 1. Introduction

Amazon EC2 provides virtual servers that can be used to host web applications and websites.

In this project, an EC2 instance running Amazon Linux 2023 was configured with the Nginx web server to host a static website.

Amazon S3 was used as backup storage for the website files. The website was accessed through the public IPv4 address of the EC2 instance.

## 2. Objectives

- Launch and configure an Amazon EC2 instance.
- Install and configure the Nginx web server.
- Create and host a static HTML website.
- Configure Security Group rules for web access.
- Create an Amazon S3 bucket.
- Upload the website backup file to S3.
- Verify the website through the EC2 public IP.
- Understand the basic use of EC2, Nginx and S3.

## 3. Project Architecture

**User → EC2 Instance → Nginx Web Server**

**EC2 Instance → Amazon S3 Bucket (Backup Storage)**

| Component | Purpose |
|---|---|
| Amazon EC2 | Hosts the website |
| Amazon Linux 2023 | Operating system |
| Nginx | Web server |
| Security Group | Controls network access |
| Amazon S3 | Stores website backup |
| HTML | Website content |

## 4. EC2 Instance Configuration

An EC2 instance was launched using Amazon Linux 2023.

| Setting | Configured Value |
|---|---|
| Operating System | Amazon Linux 2023 |
| Instance Type | t3.micro |
| Instance State | Running |
| Availability Zone | ap-south-1b |
| Web Server | Nginx |

## 5. Security Group Configuration

The Security Group was configured to allow incoming traffic required for the website and remote administration.

| Type | Protocol | Port | Source |
|---|---|---|---|
| HTTP | TCP | 80 | 0.0.0.0/0 |
| SSH | TCP | 22 | 0.0.0.0/0 |

Port 80 allows HTTP access to the website, while port 22 allows SSH access to the EC2 instance.

## 6. Nginx Web Server Installation

Nginx was installed on the Amazon Linux 2023 EC2 instance using the following commands:

```bash
sudo dnf update -y
sudo dnf install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
sudo systemctl status nginx
```
The Nginx service status showed **Active: active (running)**, confirming that the Nginx web server is running successfully.

## 7. Static Website Creation

The website was created as an HTML file named:

`index.html`

It was placed in the Nginx web root:

`/usr/share/nginx/html/index.html`

The website contains the project heading, AWS EC2 + Nginx + S3 information, project description, server information and operating system information.

The website was verified through the EC2 public IPv4 address. The displayed page confirms that the static website is being served by Nginx.

## 8. Amazon S3 Backup

An Amazon S3 bucket was created to store a backup copy of the website.

**Bucket name:**

`dalia-static-website-backup-2026-170638969506-ap-south-1-an`

The website file `index.html` was uploaded to the bucket.

| Object | Type | Storage Class |
|---|---|---|
| index.html | HTML | Standard |

## 9. IAM Role Configuration

An IAM role named:

`StaticWebsiteS3Role`

was associated with the EC2 instance.

The role provides permissions required for the EC2 instance to interact with AWS services.

## 10. Verification Results

| Component | Verification Result |
|---|---|
| EC2 Instance | Successful |
| Security Group HTTP/SSH rules | Successful |
| Nginx | Active / Running |
| Website | Accessed through public IP successfully |
| S3 index.html | Uploaded successfully |
| IAM Role | Configured |

## 11. Project Deliverables

The following screenshots were collected as project evidence:

- EC2 Instance Configuration screenshot
- Security Group Configuration screenshot
- Nginx Service Status screenshot
- Hosted Static Website screenshot
- S3 Bucket screenshot
- Uploaded `index.html` screenshot
- IAM Role Configuration screenshot

## 12. Learning Outcomes

- Basic AWS EC2 instance management
- Amazon Linux 2023
- Nginx web server installation
- Static website hosting
- Security Group configuration
- HTTP and SSH ports
- Amazon S3 storage
- Website backup using S3
- IAM roles and permissions
- Accessing an EC2-hosted website using a public IP

## 13. Conclusion

The project demonstrates static website hosting using Amazon EC2 and Nginx, with Amazon S3 used for storing a backup copy of the website.

An EC2 instance running Amazon Linux 2023 was configured with Nginx, the HTML website was created and accessed through the EC2 public IP, and the `index.html` file was uploaded to an S3 bucket for backup storage.

The collected screenshots provide evidence of the EC2 configuration, Security Group, Nginx service, working website, S3 bucket and uploaded website file.

## 14. Project Report

The complete project report is available here:

[**Minor Project 1 – Static Website Hosting PDF**](minor%20project%201.pdf)

## 15. References

- Amazon Web Services – EC2
- Amazon Web Services – S3
- Amazon Web Services – IAM
- Nginx

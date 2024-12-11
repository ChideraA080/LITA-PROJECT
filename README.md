
# Project Title

BUILDING A SCALABLE WEB INFRASTRUCTURE FOR SMARTSHOP USING AWS

The purpose of the project is to develop a solution that meets SmartShop's requirements by leveraging AWS services such as EC2, 
Virtual Private Cloud (VPC), and Identity and Access Management (IAM) and using APache as Webserver


## Introduction

The project provides a step-by-step process to build a scalable and secure web infrastructure for SmartShop using AWS services.

 Prerequisites

An active AWS account.

Basic understanding of AWS services (EC2, VPC, IAM, etc.).

Installed SSH client for managing instances.

Gitbash (for command execution).
## Launch an EC2 Instance

In my AWS console, I launched an EC2 instance using Amazon Linux 2. 

![Lunch Instance](https://github.com/ChideraA080/LITA-PROJECT/blob/main/LITA%20IMAGE/Lita%20EC2%20Running.png)





## Create Security Group

I configured the security group with:

1. SSH (Port 22) for remote access.

2. HTTP (Port 80) for web access.

![Security Grroup](https://github.com/ChideraA080/LITA-PROJECT/blob/main/LITA%20IMAGE/Lita%20Security%20Group.png)
## Establish SSH Client for remote Connection

I established SSH client by connecting it for remote access

![SSH Client](https://github.com/ChideraA080/LITA-PROJECT/blob/main/LITA%20IMAGE/Lita%20Showing%20EC2%20connect%20via%20SSH%20client.png)
## Connect to the EC2 Instance via SSH Client

To connect to the EC2 instance I used Git Bash.I launched Git Bash and run this command to connect to the EC2:

```ssh -i "your-key.pem" ec2-user@<public-ip>```

![Connect to instance](https://github.com/ChideraA080/LITA-PROJECT/blob/main/LITA%20IMAGE/Lita%20gitbash%20establishment.png)
## Installing the Apache Web Server

The first step is to update the server's package index and install the Apache web server.

Purpose: To updates the package lists for the server and upgrades any outdated packages, Start the Apache service and 
Enable the service to run on startup.

Commands to use on the gitbash:

```
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```
![Apache Installation](https://github.com/ChideraA080/LITA-PROJECT/blob/main/LITA%20IMAGE/Lita%20gitbash%20showing%20commands%20run.png)
## To Test Apache with Public IP address After Installation

Go to your browser, navigate and paste this command:

```
http://<ec2-instance-public-ip>
```
You should see the Apache Test page like this below:

![Apache Test Page](https://github.com/ChideraA080/LITA-PROJECT/blob/main/LITA%20IMAGE/Lita%20Showing%20Apache%20Page%20Installed.png)
## Summary Of Learnings From the Project

What I Learned
AWS Service Utilization:

I gained hands-on experience in deploying scalable web infrastructure using AWS services like EC2, VPC, IAM.
Learned how to configure and manage security groups, subnets, and route tables for a secure and isolated network environment.

Web Server Configuration:

Installed and configured Apache on Amazon Linux 2.
Deployed a basic web application and verified its accessibility via a web browser.

This project provided me a comprehensive understanding of building scalable, secure, web infrastructure using AWS.
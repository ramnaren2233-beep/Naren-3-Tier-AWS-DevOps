# Task 2 - Deploy the Web Tier

## Objective

Deploy the Presentation Layer using AWS EC2 instances in the Public Subnets.

## 1. AWS Deployment Details

| No. | Component | What I Did | Status |
|---:|---|---|---|
| 1 | EC2 Instance | Launched an EC2 instance in **Naren-Web-Public-A** | Completed |
| 2 | Security Group | Configured **Naren-Web-SG** with the required inbound rules | Completed |
| 3 | EC2 Connection | Successfully connected to the EC2 instance using EC2 Instance Connect | Completed |
| 4 | Nginx | Installed Nginx and verified that it is running successfully | Completed |
| 5 | HTML Files | Copied the HTML files to the Nginx web directory | Completed |
| 6 | Web Page | Successfully accessed the website using the EC2 Public IP | Completed |

## 2. AWS Services Used

| No. | Service | Purpose |
|---:|---|---|
| 1 | Amazon EC2 | Used to run and host the web server |
| 2 | Amazon VPC | Used to provide the AWS network |
| 3 | Public Subnet | Used to place the EC2 instance in the public network |
| 4 | Security Group | Used to allow or block network traffic |
| 5 | Nginx | Used to run and serve the website |
| 6 | HTML | Used to create and display the website content |

## 3. My Task 2 Work

| Step | Task | My Answer |
|---:|---|---|
| 1 | EC2 Instance | I launched an EC2 instance in **Naren-Web-Public-A**. |
| 2 | Security Group | I configured the **Naren-Web-SG** Security Group with the required inbound rules. |
| 3 | EC2 Connection | I successfully connected to the EC2 instance using EC2 Instance Connect. |
| 4 | Nginx Installation | I installed Nginx and started the Nginx service on the EC2 instance. |
| 5 | HTML Files | I copied the provided HTML files to the Nginx web directory. |
| 6 | Web Page Verification | I successfully accessed and verified the website using the EC2 Public IP address. |

## 4. Deployment Summary

| No. | Step | My Result |
|---:|---|---|
| 1 | EC2 | EC2 instance launched in **Naren-Web-Public-A** |
| 2 | Security Group | **Naren-Web-SG** configured with required inbound rules |
| 3 | EC2 Connection | Successfully connected |
| 4 | Nginx | Installed and running |
| 5 | HTML Deployment | HTML files copied to Nginx web directory |
| 6 | Website Verification | Website successfully accessed |

## 5. Screenshots

| No. | Screenshot | My Proof |
|---:|---|---|
| 1 | EC2 | `01-EC2.png` |
| 2 | Security Group | `02-Security-Group.png` |
| 3 | Connection | `03-Connection.png` |
| 4 | Nginx | `04-Nginx.png` |
| 5 | Web Page | `05-Webpage.png` |

## 6. Result

The Web Tier / Presentation Layer was successfully deployed using AWS EC2 and Nginx.

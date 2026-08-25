# Task 5 - Implement Network and Instance Security

| S.No | Task | Answer / Implementation |
|---:|---|---|
| 1 | Create Security Groups | Security Groups were created for the Web, Application, Database, and Load Balancer tiers. |
| 2 | Configure Web Tier Security Group | Required HTTP traffic was allowed for the Web Tier. **Security Group:** `Naren-Web-SG` |
| 3 | Configure Application Tier Security Group | Application traffic was allowed on port **5000** from the Internal Load Balancer. **Security Group:** `Naren-App-SG` |
| 4 | Configure Database Tier Security Group | MySQL traffic on port **3306** was allowed only from the Application Tier. **Security Group:** `Naren-DB-SG` |
| 5 | Configure Load Balancer Security Group | HTTP traffic was allowed for the Load Balancer. HTTPS was not configured. **Security Group:** `Naren-LB-SG` |
| 6 | Verify Security Rules | Inbound and outbound rules were verified to ensure only the required ports were allowed. |

## Security Group Configuration

| Tier | Security Group | Port | Protocol | Source | Purpose |
|---|---|---:|---|---|---|
| Web Tier | `Naren-Web-SG` | 80 | TCP | `0.0.0.0/0` | HTTP Web Traffic |
| Application Tier | `Naren-App-SG` | 5000 | TCP | `Naren-Internal-ALB-SG` (`sg-0396152261f787a7b`) | Flask Application Traffic |
| Database Tier | `Naren-DB-SG` | 3306 | TCP | `Naren-App-SG` (`sg-02fe92f97309d3a86`) | MySQL Database Connection |
| Load Balancer | `Naren-LB-SG` | 80 | TCP | `0.0.0.0/0` | HTTP Traffic |

## AWS Security Group Details

| Tier | Security Group Name | Security Group ID |
|---|---|---|
| Web Tier | `Naren-Web-SG` | `sg-0b328da160bfcb5cc` |
| Application Tier | `Naren-App-SG` | `sg-02fe92f97309d3a86` |
| Database Tier | `Naren-DB-SG` | `sg-05d6353c5980219a3` |
| Load Balancer | `Naren-LB-SG` | `sg-0c906be99400fb414` |
| Internal Load Balancer | `Naren-Internal-ALB-SG` | `sg-0396152261f787a7b` |

## Screenshots

### 1. Load Balancer Security Group
Shows the inbound HTTP rule on port **80** with source `0.0.0.0/0`.

### 2. Web Tier Security Group
Shows the Web Tier Security Group and its configured inbound/outbound rules.

### 3. Application Tier Security Group
Shows port **5000** allowed from the `Naren-Internal-ALB-SG` security group.

### 4. Database Tier Security Group
Shows MySQL port **3306** allowed only from the `Naren-App-SG` security group.

### 5. RDS Connectivity & Security
Shows the RDS database network configuration, VPC, port **3306**, and associated security group.

## Task 5 Status

**Network and Instance Security configuration completed successfully.**

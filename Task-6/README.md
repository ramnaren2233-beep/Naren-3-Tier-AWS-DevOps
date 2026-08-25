# Task 6 – Configure the Internet-Facing Application Load Balancer

| S.No | Task / Requirement                                  | Answer / Implementation                                                                                                          |
| ---: | --------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
|    1 | Create an Internet-Facing Application Load Balancer | An **Internet-Facing Application Load Balancer (ALB)** was created to distribute incoming traffic to the Web Tier EC2 instances. |
|    2 | Create a Target Group                               | A target group was created for the Web Tier EC2 instances.                                                                       |
|    3 | Target Group Name                                   | **Naren-Web-TG**                                                                                                                 |
|    4 | Target Group Protocol                               | **HTTP**                                                                                                                         |
|    5 | Target Group Port                                   | **80**                                                                                                                           |
|    6 | Register Web EC2 Instances                          | The Web Tier EC2 instances were registered as targets in the target group.                                                       |
|    7 | Registered Web EC2 Instances                        | **Instance ID:** `i-05a9b8d01bd7ddb74`<br>**Name:** `Naren-Web-EC2-A`                                                            |
|    8 | Configure Health Checks                             | Health checks were configured to verify the availability of the Web Tier instances.                                              |
|    9 | Health Check Protocol                               | **HTTP**                                                                                                                         |
|   10 | Health Check Port                                   | **Traffic Port / 80**                                                                                                            |
|   11 | Health Check Path                                   | **/**                                                                                                                            |
|   12 | Health Check Interval                               | **30 seconds**                                                                                                                   |
|   13 | Healthy Threshold                                   | **5 consecutive health check successes**                                                                                         |
|   14 | Unhealthy Threshold                                 | **2 consecutive health check failures**                                                                                          |
|   15 | Load Balancer Name                                  | **Naren-Internet-ALB**                                                                                                           |
|   16 | Load Balancer Type                                  | **Application Load Balancer (ALB)**                                                                                              |
|   17 | Scheme                                              | **Internet-facing**                                                                                                              |
|   18 | Load Balancer Security Group                        | **Naren-LB-SG**                                                                                                                  |
|   19 | Listener                                            | **HTTP : 80**                                                                                                                    |
|   20 | Public Subnet 1                                     | **subnet-07bbbd0d216953858 / Naren-Web-Public-A**                                                                                |
|   21 | Public Subnet 2                                     | **subnet-0eebe5631588cc0d4 / Naren-Public-B**                                                                                    |
|   22 | VPC                                                 | **Naren-3Tier-VPC**                                                                                                              |
|   23 | Load Balancer DNS Name                              | `Naren-Internet-ALB-2004691733.ap-south-1.elb.amazonaws.com`                                                                     |
|   24 | Attach Load Balancer to Public Subnets              | The Internet-Facing ALB was attached to the two Public Web Subnets.                                                              |
|   25 | Configure Listener                                  | An HTTP listener on port **80** was configured to forward requests to the Web Tier target group.                                 |
|   26 | Verify Target Health                                | The registered Web EC2 instances were checked to ensure their target health status was **Healthy**.                              |
|   27 | Verify Application Access                           | The application was accessed using the ALB DNS name.                                                                             |
|   28 | Application URL                                     | `http://Naren-Internet-ALB-2004691733.ap-south-1.elb.amazonaws.com`                                                              |
|   29 | Final Verification                                  | The application was successfully verified through the Internet-Facing 
Application Load Balancer.


| S.No | Screenshot Name                   |
| ---: | --------------------------------- |
|    1 | Target Group Details              |
|    2 | Registered Web EC2 Instances      |
|    3 | Target Health Status              |
|    4 | Application Load Balancer Details |
|    5 | ALB Listener – HTTP 80            |
|    6 | ALB Public Subnets                |
|    7 | ALB Security Group                |
|    8 | ALB DNS Application Verification  |

# Task 6 Status

Internet-Facing Application Load Balancer configuration completed successfully.

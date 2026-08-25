# Task 7 - Configure Internal Application Load Balancer

| S.No | Task / Requirement                                | Answer / Implementation                                                                                                     |
| ---: | ------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
|    1 | Create an Internal Application Load Balancer      | An **Internal Application Load Balancer (ALB)** was created for the Application Tier to handle private application traffic. |
|    2 | Load Balancer Name                                | **Naren-Internal-ALB**                                                                                                      |
|    3 | Load Balancer Type                                | **Application Load Balancer (ALB)**                                                                                         |
|    4 | Scheme                                            | **Internal**                                                                                                                |
|    5 | VPC                                               | **Naren-3Tier-VPC**                                                                                                         |
|    6 | Load Balancer Security Group                      | **Naren-Internal-ALB-SG**                                                                                                   |
|    7 | Create a Target Group                             | A target group was created for the Application Tier Flask EC2 instance.                                                     |
|    8 | Target Group Name                                 | **Naren-App-TG**                                                                                                            |
|    9 | Target Group Protocol                             | **HTTP**                                                                                                                    |
|   10 | Target Group Port                                 | **5000**                                                                                                                    |
|   11 | Register Flask EC2 Instances                      | The Flask Application EC2 instance was registered as a target in the target group.                                          |
|   12 | Flask EC2 Instance ID                             | **i-019f6acc6f76e792b**                                                                                                     |
|   13 | Flask EC2 Instance Name                           | **Naren-App-Server**                                                                                                        |
|   14 | Application Subnet 1                              | **subnet-0bb4dc4133e76a9c1**                                                                                                |
|   15 | Application Subnet 2                              | **subnet-08e7db9cea295b3a4**                                                                                                |
|   16 | Configure Health Checks                           | Health checks were configured to verify the availability of the Flask Application EC2 instance.                             |
|   17 | Health Check Protocol                             | **HTTP**                                                                                                                    |
|   18 | Health Check Port                                 | **Traffic Port / 5000**                                                                                                     |
|   19 | Health Check Path                                 | **/**                                                                                                                       |
|   20 | Health Check Interval                             | **30 seconds**                                                                                                              |
|   21 | Healthy Threshold                                 | **5 consecutive health check successes**                                                                                    |
|   22 | Unhealthy Threshold                               | **2 consecutive health check failures**                                                                                     |
|   23 | Listener                                          | **HTTP : 5000**                                                                                                             |
|   24 | Listener Action                                   | The listener was configured to forward application traffic to the Application Tier target group.                            |
|   25 | Registered Target Health                          | The registered Flask EC2 instance was verified to have a **Healthy** target status.                                         |
|   26 | Internal ALB DNS Name                             | `internal-Naren-Internal-ALB-435335926.ap-south-1.elb.amazonaws.com`                                                        |
|   27 | Verify Web Tier to Application Tier Communication | Communication between the Web Tier and Application Tier was verified through the Internal Application Load Balancer.        |
|   28 | Application Tier Target Group                     | **Naren-App-TG**                                                                                                            |
|   29 | Final Verification                                | The Internal Application Load Balancer was successfully configured to route private traffic to the Flask Application Tier.  |

| S.No | Screenshot Name                            |
| ---: | ------------------------------------------ |
|    1 | Internal Application Load Balancer Details |
|    2 | Internal ALB Network Mapping               |
|    3 | Internal ALB Security Group                |
|    4 | Application Target Group Details           |
|    5 | Registered Flask EC2 Instance              |
|    6 | Application Target Health Status           |
|    7 | Internal ALB Listener – HTTP 5000          |
|    8 | Internal ALB DNS Name                      |
|    9 | Web Tier to Application Tier Communication |
|   10 | Final Application Tier Verification        |

Task 7 Status

Internal Application Load Balancer configuration completed successfully.

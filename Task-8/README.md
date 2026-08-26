# Task 8 - Configure Nginx Reverse Proxy for API Routing
S.No	Task / Requirement	Answer / Implementation
1	Replace Default Nginx Configuration	Default Nginx configuration was replaced successfully.
2	Copy nginx.conf File	nginx.conf was copied to the Web Tier EC2 instance.
3	Check proxy.md	Nginx configuration was configured using proxy.md.
4	Configure Reverse Proxy	Nginx was configured to forward /api/ requests to the Internal ALB.
5	Internal ALB DNS Name	internal-Naren-Internal-ALB-435335926.ap-south-1.elb.amazonaws.com
6	API Route	/api/
7	Nginx Configuration File	/etc/nginx/nginx.conf
8	Replace Configuration	Project-specific Nginx reverse proxy configuration was applied.
9	Test Nginx Configuration	sudo nginx -t — Syntax is OK and test is successful.
10	Restart Nginx	sudo systemctl restart nginx
11	Verify Nginx Status	Nginx service is active and running.
12	Web → Application Communication	Web Tier successfully communicates with the Application Tier.
13	API Request Through Nginx	/api/ request was successfully verified through Nginx.
14	Final Verification	Nginx reverse proxy and API routing were successfully verified.

# Nginx Configuration Details
S.No	Configuration	Answer
1	Configuration File	/etc/nginx/nginx.conf
2	Reverse Proxy	/api/ requests are forwarded through Nginx.
3	Internal ALB DNS	internal-Naren-Internal-ALB-435335926.ap-south-1.elb.amazonaws.com
4	API Port	5000
5	Proxy Pass	http://internal-Naren-Internal-ALB-435335926.ap-south-1.elb.amazonaws.com:5000
6	Nginx Service	Active and running

# Verification Details
S.No	Verification	Result
1	Nginx Configuration Test	Passed
2	Nginx Service Status	Active and Running
3	API Request Test	Passed
4	Web Tier → Nginx	Successful
5	Nginx → Internal ALB	Successful
6	Internal ALB → Application Tier	Successful
7	Final API Response	Successful

# Screenshot Names
S.No	Screenshot Name
1	Nginx Configuration
2	Reverse Proxy Configuration
3	Internal ALB DNS
4	Nginx Configuration Test
5	Nginx Service Status
6	API Request Verification
7	Web to Application Communication
8	Final Verification
Task 8 Status

Nginx Reverse Proxy and API Routing completed successfully.


![Screenshot 2024-09-10 210939](https://github.com/user-attachments/assets/9032be5c-8e60-4e1e-bd81-2027ba404ae9)
Architecture Diagram



CloudScale 3-Tier Architecture on AWS
This project demonstrates the deployment of a scalable and highly available 3-tier architecture on AWS, leveraging various AWS services like EC2, ALB, CloudFront, RDS, Auto Scaling Groups, and more. The architecture is designed to ensure availability, security, and performance across multiple availability zones.


Project Architecture Overview
Web Tier: Includes EC2 instances running behind an external Application Load Balancer (ALB) for distributing incoming traffic. CloudFront is used as a CDN for improved performance and security.

--> App Tier: Hosts application servers in private subnets, accessible only through internal communication from the web tier. Auto Scaling is configured for handling varying workloads.

--> Database Tier: Consists of primary and backup RDS instances in private subnets across different availability zones, ensuring data redundancy and high availability.

Key Features
--> High Availability & Fault Tolerance: Multi-AZ deployment across two availability zones using Auto Scaling Groups and ALB to handle traffic and server health checks.

--> Security: Web servers are placed in public subnets while application and database servers are secured in private subnets. IAM roles and security groups provide granular control over access.

--> Monitoring & Logging: Integrated CloudWatch for monitoring system metrics, CloudTrail for API activity logging, and VPC Flow Logs stored in S3 for detailed traffic analysis. Real-time alerts are set up via SNS.

Technologies Used
AWS Services: EC2, RDS, ALB, CloudFront, CloudWatch, CloudTrail, SNS, S3, VPC
Networking: VPC, Public/Private Subnets, Route Tables, NAT Gateways, Internet Gateway
Security: IAM Roles, Security Groups, VPC Flow Logs

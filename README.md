# The GoodGreets Company

## Company Profile
Established in 2023, The GoodGreets Company was set up to bring joy to the hearts of family, friends and colleagues with the simple act of sending a card.

## Team Members
- Low Chee Meng 
- Lim Tuang Yong Justin
- Tang Kwong Hoong
- Stephanie Wong

## Topic
[TODO]
## Website and Core Features
| URL |
| ----------- |
| https://goodgreets.sctp-sandbox.com |

![Image 1: Website Homepage](image-website-frontend.png)
Image 1: Website Homepage

### Feature 1: Card Image Upload
[TODO]
### Feature 2: Scheduled Sending of Card
[TODO]

## Solution Architecture
![Image 2: Solution Architecture](image-solution-architecture.png)
Image 2: Solution Architecture

## Repository and Technology Stack
To implement our architecture, we have logically grouped various infrastructure components into its own code repository. This is to allow decoupling of the infrastructure components to enable efficient development of each component by various developers. In addition, each group of infrastructure components could be deployed or teardowned without impacting other parts of the infrastructure. 

**Github** is the version control system used for our code repositiory and **Terraform** is the Infrastructure as Code (IaC) tool used to deploy our AWS infrastructure components via **Github Actions**.

| Repository | AWS Stack | Others |
| ---------- | --------- | --------- |
| https://github.com/friends-ce-3-group/capstone-cloudfront | CloudFront, WACL/WAF |
| https://github.com/friends-ce-3-group/capstone-s3-website | - | ReactJS |
| https://github.com/friends-ce-3-group/capstone-s3-buckets | S3, API Gateway, EventBridge | - |
| https://github.com/friends-ce-3-group/terraform-aws-network | VPC, NetGW, Subnets | - |
| https://github.com/friends-ce-3-group/capstone-ecs | ECS (Fargate), ALB, EventBridge | Prometheus |
| https://github.com/friends-ce-3-group/capstone-ecr | ECR | - |
| https://github.com/friends-ce-3-group/capstone-pydbcapstone | - | Python |
| https://github.com/friends-ce-3-group/capstone-pythumbnailscapstone | - | Python |
| https://github.com/friends-ce-3-group/capstone-rds | RDS MySQL, KMS | - |
| https://github.com/friends-ce-3-group/capstone-cards-delivery | EventBridge, Lambda, SNS, SES | Python |
| https://github.com/friends-ce-3-group/capstone-monitoring | CloudWatch | Grafana | 
| https://github.com/friends-ce-3-group/capstone-alarm | CW Alarms, SNS | Slack |

## SRE Aspect 1: Security
### Security Groups and Origin Access Control
[TODO]
### AWS
[TODO]
### RDS Proxy
[TODO]
## SRE Aspect 2: Availability
[TODO]
## SRE Aspect 3: Monitoring (Cloudwatch & Grafana)
[TODO]
## SRE Aspect 4: Alarms (Emails & Slack)
[TODO]
## SRE Aspect 5: Improving Resiliency (AWS Resiliency Hub)
[TODO]
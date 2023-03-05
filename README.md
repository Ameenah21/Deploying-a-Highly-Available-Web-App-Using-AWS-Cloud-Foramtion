# Deploying-a-Highly-Available-Web-App-Using-AWS-Cloud-Formation
In this project, I configured infrastructure to deploy a highly available web App using AWS Infrastructure as Code Service - AWS Cloud Formation.\ The Infrastructure stack in this repository consists of a VPC and a server stack.
Technologies:
- [AWS Cloud](https://aws.amazon.com/)
- [AWS Cloud Formation](https://aws.amazon.com/cloudformation/)
- [AWS CLI](https://aws.amazon.com/cli/)\
- 
The VPC template deploys a VPC, with a pair of public and private subnets spread across two Availabilty Zones. It deploys an Internet Gateway, with a default route on the public subnets. It deploys a pair of NAT Gateways (one in each AZ), and default routes for them in the private subnets.

The Server template deploys 3 Ec2 servers, with one in the private subnet and an autoscaling group.
![alt text](https://github.com/Ameenah21/Deploying-a-Highly-Available-Web-App-Using-AWS-Cloud-Foramtion/blob/main/Architecture%20diagram.png)

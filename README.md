# Deploying-a-Highly-Available-Web-App-Using-AWS-Cloud-Formation
In this project, I configured infrastructure to deploy a highly available web App using AWS Infrastructure as Code Service - AWS Cloud Formation.The deployment includes setting up a VPC (Virtual Private Cloud) with public and private subnets spread across multiple Availability Zones, as well as launching a server stack for the web application.

# Technologies:
- [AWS Cloud](https://aws.amazon.com/)
- [AWS Cloud Formation](https://aws.amazon.com/cloudformation/)
- [AWS CLI](https://aws.amazon.com/cli/)
  
# Architecture
The architecture consists of the following components:

- VPC: A virtual network that provides isolation and security for your resources.
- Public Subnets: Subnets that have access to the internet and are used for hosting publicly accessible resources.
- Private Subnets: Subnets that do not have internet access and are used for hosting private resources.
- Internet Gateway: Provides internet connectivity to the public subnets.
- NAT Gateways: Allow private subnets to access the internet while keeping resources within them private.
- Load Balancer: Distributes incoming traffic across multiple instances to improve availability and scalability.
- Auto Scaling Group: Automatically adjusts the number of instances based on demand to ensure high availability and fault tolerance.
The Server template deploys 3 Ec2 servers, with one in the private subnet and an autoscaling group.
![alt text](https://github.com/Ameenah21/Deploying-a-Highly-Available-Web-App-Using-AWS-Cloud-Foramtion/blob/main/Architecture%20diagram.png)

# Prerequisites
Before deploying the application, make sure you have the following prerequisites:

- An AWS account
- AWS CLI installed and configured
- Git installed
# Deployment Steps
To deploy the highly available application on AWS, follow these steps:

1. Clone the repository:
2. Navigate to the cloned repository:
3. Update the necessary parameters in the network_parameters.json and servers_parameters.json files to match your requirements.
4. Create the network stack by executing the create_stack.sh script:
5. Wait for the network stack creation to complete.
6. Create the server stack by executing the create_stack.sh script again passing the server.yml as argument
7. Wait for the server stack creation to complete.
8. Access the deployed application by opening the DNS name of the Load Balancer provided in the stack outputs.

# Updating the Stack
If you need to update the stack with new configurations, follow these steps:

1. Modify the necessary parameters in the respective parameter files (network_parameters.json or servers_parameters.json).
2. Update the network stack by executing the update_stack.sh script
3. Wait for the network stack update to complete.

Update the server stack by executing the update_stack.sh script again:

Wait for the server stack update to complete.

# Cleaning Up
To delete the deployed stacks and remove all resources from your AWS account, follow these steps:

1. Delete the server stack by executing the delete_stack.sh script
2. Wait for the server stack deletion to complete.
3. Delete the network stack by executing the delete_stack.sh script again
4. Wait for the network stack deletion to complete.


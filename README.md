# AWS Three-Tier Infrastructure Deployment with Terraform
![Terraform Architecture] (screenshots/36-terraform-architecture-diagram.png)

## Project Overview

This project demonstrates how to deploy a production-style three-tier AWS infrastructure using Terraform Infrastructure as Code (IaC)
Instead of manually provisioning resources through the AWS Management Console, the entire infrastructure was deployed from code, making the deployment repeatable, scaleable, version-controlled, and easy to maintain.
The architecture includes:

- Amazon VPC
- Two Public Subnets
- Two private Subnets
- Internet Gateway
- Route Tables
- Security Groups
- Two Amazon EC2 instances running (Apache Web Server installed)
- Application Load Balancer (ALB)
- Amazon RDS MySQL Database
- DB Subnet Group
After successfully testing the deployment, the infrastructure was safely removed using 'terraform destroy', demonstrating proper cloud cost management and infrastructure lifecycle management.

## Prerequisites
Before deploying this project, ensure you have the following:
- An active AWS account
- Terraform installed
- AWS CLI installed and configured
- An IAM user with programmatic access
- AWS Access Key ID, ans Secret Access key configured
- Basic knowledge of Terraform and AWS Networking

## Deployment Steps
1. Clone the repository
2. Navigate to the project directory
3. Initialize Terraform:
   '''bash
   terraform init
   '''
4. Validate the Terraform configuration:
   '''bash
   terraform validate
   '''
5. Preview the execution plan:
   '''bash
   terraform plan
   '''
6. Deploy the infrastructure:
   '''bash
   terraform apply
   '''
7. Verify the deployed resources in the AWS Management Console.
8. Test the Application Load Balancer by accessing its DNS name in a web browser.
9. When finished, remove all resources to avoid AWS charges:
    '''bash
   terraform destroy
    

# AWS EC2 Instance Terraform Module

This Terraform configuration creates an EC2 instance in AWS with the following components:
- VPC with Internet Gateway
- Public Subnet
- Route Table with Internet access
- Security Group allowing SSH access
- EC2 instance running Amazon Linux 2

## Prerequisites
- AWS Account
- Terraform installed
- AWS CLI configured

## Usage
1. Clone the repository
2. Navigate to the module directory
3. Run `terraform init`
4. Run `terraform apply` to create the resources
5. Run `terraform destroy` to delete the resources


## Variables
| Name | Description | Type | Default |
|------|-------------|------|---------|
| aws_region | AWS region | string | us-east-1 |
| instance_type | EC2 instance type | string | t2.micro |
| instance_name | Name tag for EC2 instance | string | my-ec2-instance |
| vpc_cidr | CIDR block for VPC | string | 10.0.0.0/16 |
| subnet_cidr | CIDR block for subnet | string | 10.0.1.0/24 |

## Outputs
| Name | Description |
|------|-------------|
| instance_id | ID of the EC2 instance |
| instance_public_ip | Public IP of the EC2 instance |
| vpc_id | ID of the VPC |
| subnet_id | ID of the subnet |
# Terraform Configuration for AWS VPC, EC2 and RDS

### This project contains terraform configuration files on creating EC2 and RDS instances inside a Custom VPC on AWS. Here is the architecture of what will be created:

![Custom VPC architecture for AWS](https://miro.medium.com/max/700/1*Oxp7FZT4Z9RWqpnJn-hHqw.png)

## Set Up
### Prerequisites
- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) installed and configuration
- [Terraform](https://www.terraform.io/downloads) installed

### Create the Secrets file
Create a secrets file called ***secrets.tfvars*** and populate it with the follow secrets:
  - **db_username** <-- this is going to be the master user for RDS
  - **db_password** <-- this is going to be the RDS master user's password
  - **my_ip** <-- this is going to be your public IP

## Running the Configuration
### Initializing the Terraform directory
Run the command: `terraform init`

### Apply the Terraform Config to AWS
Run the command: `terraform apply -var-file="secrets.tfvars"`

### To destroy everything that was created by the Terraform Config
Run the command: `terraform destroy -var-file="secrets.tfvars"`

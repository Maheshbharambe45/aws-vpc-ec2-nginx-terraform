## Terraform AWS VPC + EC2 + Nginx Deployment

This repository contains Terraform configuration files to deploy a complete AWS infrastructure including:

- A custom VPC
- Public and private subnets
- Internet Gateway and route tables
- Security Group (SSH + HTTP)
- A public EC2 instance with Nginx auto-installed using user data

Once deployed, you can access the Nginx web server using the EC2 public IP address.


##  Prerequisites

Make sure the following are installed and configured:

- **Terraform v1.0+**
- **AWS CLI** (`aws configure` must be completed)
- **AWS Key Pair** for SSH access
- IAM permissions to create:
  - VPC
  - Subnets
  - Internet Gateway
  - Route Tables
  - EC2
  - Security Groups


---

## 1. Initialize Terraform

Initialize providers and modules:

```bash
terraform init

```

## 2. Validate Configuration

```bash
terraform validate

```

## 3. Preview Resources Before Creation

```bash
terraform plan

```

## 4. Apply Terraform Configuration

```bash
terraform apply --auto-approve

```
 ![Website Screenshot](assets/Screenshot%202025-11-21%20203342.png)


 See All Resources

 Ec2 instance

 ![Website Screenshot](assets/Screenshot%202025-11-21%20203416.png)


 Security groups

![Website Screenshot](assets/Screenshot%202025-11-21%20203445.png)

Vpc

 ![Website Screenshot](assets/Screenshot%202025-11-21%20203507.png)

Resource Map

 ![Website Screenshot](assets/Screenshot%202025-11-21%20203554.png)

## 5. Access the Nginx Web Server

```bash

http://<EC2_PUBLIC_IP>

http://13.234.33.45

```
 ![Website Screenshot](assets/Screenshot%202025-11-21%20221134.png)


## 6. Destroy All Resources

```bash
terraform destroy --auto-approve

```
 ![Website Screenshot](assets/Screenshot%202025-11-21%20221747.png)

👨‍💻 Author

Mahesh Bharambe — AWS | Terraform | DevOps

Terraform S3 and DynamoDB State Locking
This repository contains Terraform code to create an S3 bucket and DynamoDB table. These resources are used for locking the state file to ensure safe, concurrent operations when applying Terraform configurations.

Table of Contents
Prerequisites
Directory Structure
Setup
Usage
Contributing
Prerequisites
Terraform installed
AWS credentials configured with sufficient permissions to create S3 buckets and DynamoDB tables.
Directory Structure
text
Copy code
.
├── dynamo.tf           # DynamoDB table configuration for state file locking
├── provider.tf         # AWS provider configuration
├── s3.tf               # S3 bucket configuration for storing state files
├── terraform.tfvars    # Variable values for the configuration
└── variable.tf         # Variable definitions
Setup
Clone the repository:

bash
Copy code
git clone https://github.com/pankaj957/Terraform-Code.git
cd Terraform-Code
Customize terraform.tfvars with your desired S3 bucket and DynamoDB table configurations.

Initialize the Terraform working directory:

bash
Copy code
terraform init
Usage
To apply the configuration and create the resources, run:

bash
Copy code
terraform apply
Review the plan and confirm with yes to create the resources.

To destroy the created resources, run:

bash
Copy code
terraform destroy
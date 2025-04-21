# 📁 Terraform Folder Layout – AWS E-Commerce Capstone
👨‍💻 *By: Punna Rao Kommineni*

---

## 📦 Root Folder: `capstone-ecommerce-aws/`
Contains service-specific Terraform modules and a central `terraform/` deployment layer.

---

### 🔹 networking/
Terraform modules for:
- VPC and Subnet Creation
- Route Tables, IGW, NAT Gateway
- ALB Setup

**Files:**
- `vpc.tf`
- `subnets.tf`
- `routing.tf`
- `alb.tf`
- `variables.tf`, `outputs.tf`

---

### 🔹 compute/
Terraform for:
- EC2 Launch Template
- Auto Scaling Group
- Lambda Functions

**Files:**
- `ec2.tf`
- `asg.tf`
- `lambda.tf`
- `variables.tf`, `outputs.tf`

---

### 🔹 storage/
Terraform for:
- S3 Bucket for media, invoices
- EBS volumes attached to EC2

**Files:**
- `s3.tf`
- `ebs.tf`
- `variables.tf`, `outputs.tf`

---

### 🔹 database/
Terraform for:
- RDS MySQL
- DynamoDB table for carts/session

**Files:**
- `rds.tf`
- `dynamodb.tf`
- `variables.tf`, `outputs.tf`

---

### 🔹 integration/
Terraform for:
- SQS for order queue
- SNS for user notifications
- EventBridge for triggers

**Files:**
- `sqs.tf`
- `sns.tf`
- `eventbridge.tf`
- `variables.tf`, `outputs.tf`

---

### 🔹 security/
Terraform for:
- IAM Roles, Policies for EC2, Lambda, RDS
- Cognito User Pool
- WAF Web ACLs

**Files:**
- `iam.tf`
- `cognito.tf`
- `waf.tf`
- `variables.tf`, `outputs.tf`

---

### 🔹 observability/
Terraform for:
- CloudWatch Logs, Metrics, Dashboards
- AWS X-Ray setup

**Files:**
- `cloudwatch.tf`
- `xray.tf`
- `variables.tf`, `outputs.tf`

---

### 🔹 terraform/
Root execution layer to bring everything together.

**Files:**
- `main.tf` → Includes modules from subfolders
- `providers.tf` → AWS provider config
- `variables.tf`, `outputs.tf`
- `backend.tf` (optional – S3 + DynamoDB for state)

---

## 💡 Notes
- Each subfolder is a self-contained reusable module
- Use `terraform init`, `plan`, and `apply` in the `terraform/` folder
- Variables can be loaded via `terraform.tfvars`

This structure allows clean separation, modular code, and environment-specific overrides later.


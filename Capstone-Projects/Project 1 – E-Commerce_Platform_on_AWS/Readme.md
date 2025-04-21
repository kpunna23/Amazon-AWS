# 🛒 Capstone Project 1 – E-Commerce Platform on AWS
👨‍💻 *Cloud Architect: Punna Rao Kommineni*

---

## 📘 Project Overview
This project simulates a scalable, secure, and fully monitored **E-Commerce Platform** built on Amazon Web Services. It includes components for customer-facing UI, product catalog, secure ordering, cart management, payment integration, and admin reporting.

---

## 🧩 Architecture Layers

| Layer | AWS Services |
|-------|--------------|
| **Networking** | VPC, Subnets, IGW, NAT, Route Tables, ALB |
| **Compute** | EC2 (Web/API), Auto Scaling Group, Launch Templates, Lambda |
| **Storage** | S3 (images, invoices), EBS |
| **Database** | Amazon RDS (MySQL), DynamoDB (shopping cart/sessions) |
| **Security** | IAM, Security Groups, WAF, Cognito for auth |
| **App Integration** | SQS (Order Queue), SNS (Confirmation), EventBridge (Triggers) |
| **Monitoring & Logs** | CloudWatch Logs, Metrics, Dashboards, Alarms, AWS X-Ray |
| **Cost Optimization** | AWS Budgets, Cost Explorer |
| **Infra as Code** | Terraform Modules by Layer |

---

## 📂 Project Folder Structure

```
capstone-ecommerce-aws/
├── networking/        --> VPC, Subnets, NAT, IGW
├── compute/           --> EC2, Launch Template, Auto Scaling
├── storage/           --> S3 Buckets, EBS Volumes
├── database/          --> RDS MySQL, DynamoDB for cart/session
├── integration/       --> SQS, SNS, EventBridge
├── security/          --> IAM Roles, WAF Rules, Cognito Pools
├── observability/     --> CloudWatch, Logs, Dashboards, X-Ray
├── terraform/         --> main.tf, variables.tf, outputs.tf
├── diagrams/          --> architecture.png
└── README.md          --> This file
```

---

## ✅ Key Implementation Goals
- ✅ Design Highly Available Architecture across AZs
- ✅ Use both SQL and NoSQL storage for flexibility
- ✅ Secure app using IAM, WAF, and Cognito
- ✅ Decouple order processing using SQS
- ✅ Automate infra deployment using Terraform
- ✅ Enable monitoring + alerting with CloudWatch

---

## 📈 Architecture Diagram
_📍Located in `diagrams/architecture.png`_

---

## 🧪 Use Case Scenarios
1. **User Registration + Login** (via Cognito)
2. **View Product Catalog** (stored in RDS)
3. **Add to Cart** (DynamoDB + sessions)
4. **Place Order** (Triggers SQS)
5. **Order Processed by Lambda**
6. **Notifications sent via SNS**
7. **Admin views order logs and dashboards**

---

## 🔐 Security Measures
- IAM Role Segmentation (EC2, Lambda, DB)
- S3 Bucket Policies + KMS Encryption
- RDS Encryption + VPC Private Subnet
- WAF for Web Layer Protection
- Cognito for secure user management

---

## 🧠 Future Enhancements
- Enable CI/CD Pipeline with CodePipeline & CodeDeploy
- Integrate with Stripe/PayPal in test mode
- Add CloudTrail for governance
- Add Shield Advanced for DDoS

---

## 🏁 Final Goal
You will deploy and validate:
- Secure and scalable cloud infrastructure
- Full-stack e-commerce use case
- Monitoring, automation, and cost-awareness

_Designed to reflect real-world enterprise experience for interviews and client demos._


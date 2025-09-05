
---


# Terraform + GitHub Actions Automation

This project provisions core AWS resources using **Terraform** and automates infrastructure management with **GitHub Actions**. The repository demonstrates best practices for Infrastructure as Code (IaC) and CI/CD automation.

---


## 🚀 Project Purpose

- Provision AWS resources with **Terraform**
- Automate infrastructure management using **GitHub Actions** workflows
- Enforce CI/CD best practices for IaC

---


## 📦 AWS Resources Provisioned

The Terraform code provisions the following AWS resources:

- **VPC**
- **Subnet**
- **Route Table**
- **Internet Gateway**
- **Security Group**
- **S3 Bucket**
- **DynamoDB Table**

---


## 🤖 GitHub Actions Workflows

Three workflows automate the Terraform process:

- **build.yml**: Runs `terraform validate` to check syntax and formatting on every push or pull request to `dev`.
- **terraform-plan.yml**: Runs `terraform init` and `terraform plan` on pull requests to preview infrastructure changes.
- **terraform-apply.yml**: Runs `terraform apply -auto-approve` (manual trigger) to deploy infrastructure automatically.

---

## ✅ Outcome

Once all steps are completed:

- Terraform will provision AWS infrastructure automatically.
- GitHub Actions will handle validation, planning, and deployment through CI/CD pipelines.

---

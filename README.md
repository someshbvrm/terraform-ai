
---

# Terraform + GitHub Actions Automation

This project demonstrates **Infrastructure as Code (IaC)** using Terraform, combined with **GitHub Actions** for automation.
It provisions core AWS resources and automates the validation, planning, and applying of Terraform code using CI/CD workflows.

---

## 🚀 Project Purpose

* Provision AWS resources with **Terraform**.
* Automate infrastructure management using **GitHub Actions** workflows.
* Enforce CI/CD best practices for IaC.

---

## 📦 AWS Resources Provisioned

Terraform code in this repository provisions the following resources:

* **VPC**
* **Subnet**
* **Route Table**
* **Internet Gateway**
* **Security Group**
* **S3 Bucket**
* **DynamoDB Table**

---

## ⚙️ Steps to Set Up

Follow these steps strictly in order (1 → 7). Do not skip or merge steps.

### 1. Clone the Repository

```bash
git clone https://github.com/venkatkukatla/Terraform-ai.git
cd Terraform-ai
```

---

### 2. Create and Switch to a New Branch

```bash
git checkout -b dev
```

---

### 3. Create Terraform Files in Project Root

Create the following files:

* **main.tf**
* **variables.tf**
* **terraform.tfvars**

These must define the AWS resources listed above (VPC, subnet, route table, IGW, security group, S3, DynamoDB).

---

### 4. Configure GitHub Workflows

Create the folder `/.github/workflows/` and add these workflows:

* **build.yml** → runs `terraform validate`
* **terraform-plan.yml** → runs `terraform init` and `terraform plan`
* **terraform-apply.yml** → runs `terraform apply -auto-approve`

---

### 5. Add `.gitignore`

Create a `.gitignore` file to exclude:

```
.terraform/
*.tfstate
*.tfstate.backup
crash.log
.DS_Store
```

---

### 6. Update README.md

Update this README with:

* Project purpose
* AWS resources being provisioned
* Workflows explanation

---

### 7. Commit and Push Changes

```bash
git add .
git commit -m "Terraform setup with GitHub Actions workflows"
git push origin dev
```

---

## 🤖 GitHub Actions Workflows

* **Build Workflow (`build.yml`)**
  Runs `terraform validate` to check syntax and formatting.

* **Terraform Plan Workflow (`terraform-plan.yml`)**
  Runs `terraform init` and `terraform plan` to preview infrastructure changes.

* **Terraform Apply Workflow (`terraform-apply.yml`)**
  Runs `terraform apply -auto-approve` to deploy infrastructure automatically.

---

## ✅ Outcome

Once all steps are completed:

* Terraform will provision AWS infrastructure automatically.
* GitHub Actions will handle validation, planning, and deployment through CI/CD pipelines.

---

Would you like me to also include **example workflow YAML files (build.yml, plan, apply)** in the README so contributors can copy them directly, or keep README only as a guide?

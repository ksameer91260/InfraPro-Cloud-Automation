# InfraPro - AWS Cloud Infrastructure Automation 🚀

An end-to-end cloud automation project designed to provision scalable cloud resources on Amazon Web Services (AWS) using Infrastructure as Code (IaC) and configure them automatically using Configuration Management.

---

## 🛠️ Tech Stack & Tools
- **Cloud Provider:** Amazon Web Services (AWS)
- **Infrastructure as Code (IaC):** Terraform (v1.x)
- **Configuration Management:** Ansible
- **Operating System:** Ubuntu LTS (EC2)
- **Web Server:** Nginx

---

## 📐 Architecture & Flow
1. **Infrastructure Provisioning (Terraform):**
   - Creates a custom VPC (`10.0.0.0/16`) for network isolation.
   - Sets up a Security Group allowing SSH (Port 22) and HTTP (Port 80) traffic.
   - Deploys an AWS EC2 instance running Ubuntu LTS.
2. **Configuration & Deployment (Ansible):**
   - Connects to the EC2 instance via SSH.
   - Installs and enables the Nginx Web Server.
   - Deploys a custom, responsive HTML landing page.

---

## 📁 Repository Structure
- `main.tf` - Declarative Terraform configuration file to spin up AWS resources.
- `playbook.yml` - Ansible playbook for installing Nginx and deploying the web application.
- `README.md` - Project documentation and setup guide.

---

## 🚀 How to Run This Project

### 1. Prerequisites
- AWS Account with IAM credentials configured locally.
- Terraform and Ansible installed on your control node (local machine or bastion host).

### 2. Provision Infrastructure
Initialize Terraform and apply the configuration:
```bash
terraform init
terraform plan
terraform apply -auto-approve

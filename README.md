# Terraform Docker Setup

## 📌 Objective
Provision a local Docker container using Terraform to demonstrate Infrastructure as Code (IaC).

## 🚀 Tools Used
- Terraform
- Docker

## 🛠️ Files Included
- `main.tf`: Terraform configuration file
- Terraform state files (`.terraform`, `terraform.tfstate`)
- `README.md`

## 🧱 What It Does
- Pulls the latest Nginx Docker image
- Provisions a Docker container named `nginx_container`
- Exposes port `8080` (localhost) to access the container

## ✅ Steps to Run

### 1. Install Terraform and Docker
- [Install Terraform](https://developer.hashicorp.com/terraform/downloads)
- [Install Docker](https://docs.docker.com/get-docker/)

### 2. Clone the Repository
```bash
git clone https://github.com/YOUR-USERNAME/terraform-docker-setup.git
cd terraform-docker-setup

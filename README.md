
# 🚀 Task 3: Infrastructure as Code with Terraform (Docker Setup)

## 📌 Objective  
Provision a local Docker container using **Terraform**, showcasing the power of Infrastructure as Code (IaC).

---

## 🛠 Tools Used  
- Terraform  
- Docker  
- Git & GitHub  

---

## ✅ Outcome  
You will learn how to use Terraform to automate the provisioning of a Docker container on your local system.

---

## 🧾 Prerequisites  
Make sure you have the following installed:
- Docker
- Terraform
- Git

---

## 📂 Project Setup Steps

### 🔹 Step 1: Create a New Project Directory  
Open your terminal and run:

    mkdir terraform-docker-setup
    cd terraform-docker-setup

### 🔹 Step 2: Initialize a Git Repository  

    git init

### 🔹 Step 3: Create `main.tf` File  
Create a file named `main.tf` and paste the following Terraform configuration:

    provider "docker" {}

    resource "docker_image" "nginx" {
      name = "nginx:latest"
    }

    resource "docker_container" "nginx" {
      name  = "nginx-container"
      image = docker_image.nginx.latest
      ports {
        internal = 80
        external = 8080
      }
    }

### 🔹 Step 4: Initialize Terraform  

    terraform init

This command downloads the necessary provider (Docker) and sets up the environment.

### 🔹 Step 5: Validate Configuration  

    terraform validate

Expected output:  
**Success! The configuration is valid.**

### 🔹 Step 6: Apply Configuration  

    terraform apply

Type `yes` when prompted.

Terraform will:
- Pull the nginx image
- Create a container named `nginx-container`
- Map port 80 inside the container to port 8080 on your machine

---

## 🌐 Test the Setup  
Visit this in your browser:

    http://localhost:8080

You should see the default **nginx welcome page**.

---

## 🔄 To Destroy the Setup  

    terraform destroy

Type `yes` to confirm. This will remove the container and free up resources.

---

## 🧼 Optional: .gitignore  

To keep your repo clean, create a `.gitignore` file and add:

    .terraform/
    terraform.tfstate
    terraform.tfstate.backup

---

## 🧑‍💻 Author  
**Yash Kachale**  

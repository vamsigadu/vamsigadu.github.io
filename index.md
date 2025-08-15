# 👋 Hi, I'm Vamsi

Welcome to my DevOps portfolio!  

Here’s one of my key projects:

## End to End Node.js Application Deployment with AWS, Terraform, Jenkins, Kubernetes & ArgoCD

### 📌 Overview
This project demonstrates a complete DevOps pipeline to:
- Provision AWS infrastructure using **Terraform**  
- Deploy an **EKS cluster**  
- Automate builds and deployments via **Jenkins**  
- Manage continuous delivery with **ArgoCD**  

---

### 🛠 Technologies Used
- **Cloud**: AWS (VPC, EC2, RDS, EKS, Route53, IAM, ELB)
- **IaC**: Terraform
- **CI/CD**: Jenkins
- **GitOps**: ArgoCD
- **Containerization**: Docker, AWS ECR
- **Orchestration**: Kubernetes
- **Languages/Tools**: Shell scripting, kubectl, Git

---

## 🚀 Workflow

### **1️⃣ Infrastructure Provisioning (Terraform)**
- Cloned the repository containing the `terraform-main-ec2` module.
- Ran `terraform apply` to provision:
  - **Networking**: VPC, subnets, route tables, internet gateway, NAT gateway, security groups.
  - **Compute**: EC2 jumphost with CLI tools installed via `tools.sh`.
  - **Database**: Amazon RDS instance.

**Screenshot:**  
<img src="/Screenshots/terraform output.png" width="700" alt="Terraform Output">

---

### **2️⃣ CI/CD Pipelines in Jenkins**

#### **Pipeline 1 – EKS Cluster Setup**
- Used Terraform to create the EKS cluster and configure kubectl.

#### **Pipeline 2 – Frontend Build & Deploy**
- Built Docker image for frontend, pushed to AWS ECR, updated Kubernetes manifests.

#### **Pipeline 3 – Backend Build & Deploy**
- Built backend image, pushed to ECR, updated manifests with DB credentials from Kubernetes Secrets/ConfigMaps.

**Screenshot:**  
<img src="/Screenshots/Jenkins screenshot.png" width="700" alt="Backend Deployment Pipeline">

---

### **3️⃣ GitOps with ArgoCD**
- Installed and configured ArgoCD on EKS.
- Created a project pointing to the GitHub repo path with Kubernetes manifests.
- Enabled **Auto Sync** for continuous delivery.

**Screenshot:**  
<img src="/Screenshots/Argo cd screenshot.png" width="700" alt="ArgoCD Dashboard">
<img src="/Screenshots/Argo cd screenshot 2.png" width="700" alt="ArgoCD Dashboard">

---

## ✅ Outcome
- Fully automated from infrastructure provisioning to production deployment.
- Clear separation between IaC, CI/CD, and GitOps stages.
- Scalable & repeatable in new AWS accounts.

**Screenshot:**  
<img src="/Screenshots/Project 1 output.png" width="700" alt="ArgoCD Dashboard">


---

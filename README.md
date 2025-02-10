# GitOps CI/CD Pipeline with GitHub Actions, Terraform, AWS EKS, Docker, and SonarCloud

## **Project Overview**
This GitOps-based CI/CD pipeline automates infrastructure provisioning and application deployment using **GitHub Actions, Terraform, AWS EKS, Docker, Helm, Maven, and SonarCloud**. The pipeline ensures **continuous integration, security scanning, and automated deployment** of containerized applications into a highly available Kubernetes cluster (EKS). 

It integrates **Terraform** for infrastructure management, **SonarCloud** for code quality analysis, and **Helm** for Kubernetes deployment.

## **Architecture Diagram**
![GitOps CI/CD Pipeline](terraform%20and%20app%20code%20workflow%20devops%20gitops.jpeg)

---

## **Flow of Execution**
### **1. Code Development and Version Control**
- Developers use **Visual Studio Code (VS Code)** for coding.
- Code is pushed to **GitHub**, which acts as the **central version control system**.
- **GitHub Actions** are triggered for two separate workflows:
  - **Terraform Workflow**: Infrastructure provisioning.
  - **Build, Test, and Deploy Workflow**: Application build, security scanning, and deployment.

### **2. Infrastructure Provisioning with Terraform**
- Developers work on a feature branch and push **Terraform** infrastructure changes.
- **GitHub Actions** fetch the latest **stage branch**.
- **Terraform Plan** is executed to validate infrastructure changes.
- A **Pull Request (PR)** is created for review.
- Upon approval, the **PR is merged** into the main branch.
- **Terraform Apply** executes to provision AWS resources, including:
  - **Amazon EKS (Elastic Kubernetes Service) Cluster**
  - **Amazon ECR (Elastic Container Registry) for storing container images**
  - **VPC subnet for secure ne

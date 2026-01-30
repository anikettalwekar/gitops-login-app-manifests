# GitOps Deployment using Argo CD on AWS EKS

## Project Overview
This project demonstrates a production-style GitOps workflow using Argo CD to deploy a containerized web application on Amazon EKS.  
The application is developed on an EC2 instance, containerized using Docker, pushed to Amazon ECR, and deployed to EKS using Git as the single source of truth.

---

## Architecture Overview
- Custom AWS VPC with public and private subnets
- Windows Bastion host for secure access
- Web EC2 for application development and Docker image creation
- Amazon ECR for container image storage
- Amazon EKS with private worker nodes
- Argo CD for GitOps-based continuous deployment

---

## AWS Services Used
- Amazon VPC
- Amazon EC2 (Windows Bastion, Web Server, EKS Bastion)
- Amazon ECR
- Amazon EKS
- IAM
- Argo CD
- GitHub

---

## Application Details
- Simple HTML-based login application
- Login credentials:
  - Username: admin
  - Password: admin123
- After successful login, the user is redirected to a "Welcome to Project" page

---

## GitOps Workflow
1. Application is developed on Web EC2
2. Docker image is built and pushed to Amazon ECR
3. Kubernetes manifests are stored in GitHub
4. Argo CD continuously monitors the GitHub repository
5. Argo CD syncs the desired state to the EKS cluster automatically
6. Application is exposed using a Kubernetes LoadBalancer service

---

## Repository Structure
gitops-login-app-manifests/
├── app-manifests/
│ ├── deployment.yaml
│ └── service.yaml
├── screenshots/
│ ├── 01-vpc
│ ├── 02-ec2
│ ├── 03-ecr
│ ├── 04-eks
│ ├── 05-argocd
│ └── 06-application
└── README.md



---

## Screenshots
All project-related screenshots are available inside the `screenshots/` directory, including:
- VPC and networking setup
- EC2 instances
- ECR repository and image
- EKS cluster and node groups
- Argo CD application status
- Final application output in browser

---

## Key Learnings
- End-to-end GitOps implementation using Argo CD
- Secure EKS setup with private worker nodes
- Docker image lifecycle from build to deployment
- Troubleshooting Argo CD sync and repository issues
- Real-world DevOps workflow and best practices

---

## Author
Aniket Talwekar  
AWS / DevOps Engineer

---

## Project Status
Application successfully deployed on Amazon EKS using Argo CD with automated GitOps workflow.

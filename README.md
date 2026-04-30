# 🚀 CI/CD Pipeline using GitHub Actions & ArgoCD (Java Application)

This project demonstrates a modern CI/CD pipeline using GitHub Actions (CI) and ArgoCD (CD) to deploy a Java application into Kubernetes.

---

## 📌 Overview

The pipeline automates:
- Building a Java application  
- Creating Docker images  
- Pushing images to Docker Hub  
- Deploying applications using GitOps with ArgoCD  

---

## 🏗️ Architecture Diagram

```mermaid
flowchart LR
    A[GitHub Repo] -->|Code Push| B[GitHub Actions]
    B --> C[Build Java App]
    C --> D[Build Docker Images]
    D --> E[Push to Docker Hub]
    E --> F[Update K8s Manifests]
    F --> G[ArgoCD]
    G --> H[Kubernetes Cluster]
    H --> I[Application Running]

# GitOps Crossplane - AWS Infrastructure as Code

> Complete AWS infrastructure GitOps: ArgoCD automatically provisions all resources via Crossplane

## 🎯 About

This project implements **GitOps for AWS infrastructure**, where:

- ✅ **Git is the source of truth**: All infrastructure is versioned as code
- ✅ **ArgoCD provisions automatically**: Changes in Git are automatically applied to AWS
- ✅ **Crossplane creates resources**: Translates Kubernetes manifests into real AWS resources
- ✅ **IRSA for security**: Authentication without hardcoded credentials

## 🏗️ Architecture

![GitOps Crossplane Architecture](images/crossplane.drawio.svg)

### How it works?

```
1. You commit YAML to GitHub
   ↓
2. ArgoCD detects changes
   ↓
3. ArgoCD applies to cluster
   ↓
4. Crossplane creates AWS resources
   ↓
5. Infrastructure automatically provisioned!
```

## 🏗️ Provisioned Infrastructure

- VPC with public and private subnets
- Internet Gateway and Route Tables
- EKS Cluster with Node Groups
- IAM Roles and Policies

## 📁 Structure

```
crossplane/
├── aws/          # AWS Resources (VPC, IAM, EKS)
├── config/       # Crossplane Configuration (Providers, DRCs)
└── argocd/       # ArgoCD Applications (GitOps)
```

## 📚 Technologies

- Kubernetes
- Crossplane
- ArgoCD
- AWS (VPC, EKS, IAM)


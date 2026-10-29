# Purpose:
The GitOps-ArgoCD repository stores the Kubernetes deployment configuration for the LocalHelp application. Argo CD uses this repository as the source of truth for deploying and maintaining the application in Amazon EKS.

```
 argocd/ — defines Argo CD Applications and their deployment sources.
 apps/frontend/helm/ — frontend Kubernetes resources and configuration.
 apps/backend/helm/ — backend Kubernetes resources and configuration.
```
# Responsibilities
- Jenkins: Builds and tests application code and publishes Docker images.
- Amazon ECR: Stores frontend and backend images.
- GitOps Repository: Stores Helm charts and desired deployment configuration.
- Argo CD: Synchronizes Git configuration with the EKS cluster.
- Helm: Templates Kubernetes resources for each application.
- External Secrets Operator: Retrieves database credentials from AWS Secrets Manager and creates Kubernetes Secrets.

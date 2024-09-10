# kustomization-with-argo-demo

## Description

This project is a demo lab designed to showcase the use of Kubernetes, Kustomize, and ArgoCD for managing deployments across different environments. It includes:

- **Two Web Servers**: Configured for different environments, specifically `dev` and `stg` (staging).
- **Base and Overlay Environments**: The project uses Kustomize to manage different configurations for each environment through a base configuration and environment-specific overlays.
- **ArgoCD Integration**: ArgoCD is used to deploy and manage these configurations, providing a GitOps approach to continuous deployment.

## Requirements

- **Local Kubernetes Cluster**: You need a local Kubernetes cluster to run the demo. For Mac users, you can use [Orbstack](https://orbstack.dev/) or another local Kubernetes solution.
- **Kustomize** 
  - Install with Homebrew: 
    ```bash
    brew install kustomize
    ```
- **ArgoCD CLI**
  - Install with Homebrew:
    ```bash
    brew install argocd
    ```

## Installation

1. **Start Your Local Kubernetes Cluster**

   Ensure that your local Kubernetes cluster is running. You can use [Orbstack](https://orbstack.dev/) or another local Kubernetes solution.

2. **Install ArgoCD**

    Apply the ArgoCD configuration:
    ```kubectl apply -k . -n argocd```

    Retrieve the initial password for the admin user:
    ```argocd admin initial-password -n argocd```
    For more information on setting up ArgoCD, visit the ArgoCD Getting Started Guide.

    Log In to the ArgoCD UI

    Access the ArgoCD web UI and log in with the credentials retrieved in the previous step.

    Connect Your Repository to ArgoCD

    Go to Settings in the ArgoCD UI.
    Navigate to Repositories.
    Click Connect Repo.
    Enter the Repository URL: https://github.com/dimitristoumpanos/kustomization-with-argo-demo
    Click CONNECT.


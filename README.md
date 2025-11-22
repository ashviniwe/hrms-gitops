# HRMS GitOps

This repository contains a GitOps setup for two microservices:
- user-service
- employee-service

## Deploying with Argo CD

1. Install Argo CD:
``kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml``

2. Apply the root application:

``kubectl apply -n argocd -f argo-app.yaml``

Argo CD will automatically deploy both microservices.








hrms-gitops/
 ├── argo-app.yaml
 ├── apps/
 │    ├── Chart.yaml
 │    ├── values.yaml
 │    └── templates/
 │         └── NOTES.txt
 ├── charts/
 │    ├── user-service/
 │    │     ├── Chart.yaml
 │    │     ├── values.yaml
 │    │     └── templates/
 │    │           ├── deployment.yaml
 │    │           └── service.yaml
 │    └── employee-service/
 │          ├── Chart.yaml
 │          ├── values.yaml
 │          └── templates/
 │                ├── deployment.yaml
 │                └── service.yaml
 └── README.md

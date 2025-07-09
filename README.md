# DotNetModularMonolith-k8s

## Project Overview

This repository contains Kubernetes manifests for deploying and managing the DotNetModularMonolith application and its supporting infrastructure. It provides configuration files for various components, including application deployments, services, ingress, secrets, monitoring, and infrastructure resources such as databases and metrics servers.

The aim of this repository is to contain the Kubernetes manifests for the DotNetModularMonolith applications contained in the main repository: [ilroberts/DotNetModularMonolith](https://github.com/ilroberts/DotNetModularMonolith)

### Structure

- **ECommerce.AdminUI/k8s/**: Manifests for the Admin UI, with base and overlay configurations for different environments (dev, prod).
- **ECommerceApp/k8s/**: Manifests for the main application, including deployment, service, ingress, and monitoring.
- **Infrastructure/k8s/**: Supporting infrastructure manifests, such as PostgreSQL and metrics server.

### Usage

1. Review and customize the manifests as needed for your environment.
2. Apply the manifests using `kubectl apply -k <path>` for kustomize overlays or `kubectl apply -f <file>` for individual files.
3. Monitor the deployment and ensure all resources are running as expected.

### Requirements

- Kubernetes cluster (local or cloud)
- kubectl
- kustomize (for overlays)

### Notes

- Secrets are managed using sealed secrets for security.
- Monitoring is enabled via ServiceMonitor resources.

For more details, refer to the individual manifest files and directories.

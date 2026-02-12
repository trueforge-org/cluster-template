# Kubernetes Cluster Template

WIP repository intended to one-day store the embeded cluster structure for forgetool

This repository contains the kubernetes cluster template from TrueForge ForgeTool.

## Overview

This template provides a complete, production-ready Kubernetes cluster configuration with:

- **Base Configuration**: Cluster environment variables and Talos Linux configuration
- **Kubernetes Manifests**: Pre-configured applications and system components
- **Flux GitOps**: Automated cluster management through GitOps principles
- **Patches**: Customizable patches for different node types (control plane, worker, nvidia)
- **Root Configuration**: Repository structure, workflows, and development environment setup

## Directory Structure

```
├── base/              # Cluster base configuration
│   ├── clusterenv.yaml    # Environment variables
│   └── talos/             # Talos Linux configuration
├── kubernetes/        # Kubernetes manifests
│   ├── apps/             # Application deployments
│   ├── core/             # Core cluster services
│   ├── flux-system/      # Flux CD configuration
│   ├── kube-system/      # System components
│   ├── networking/       # Network services
│   └── system/           # System applications
├── patches/           # Node-specific patches
│   ├── all.yaml          # Patches for all nodes
│   ├── controlplane.yaml # Control plane specific
│   ├── nvidia.yaml       # NVIDIA GPU support
│   └── worker.yaml       # Worker node specific
└── root/             # Repository root structure
    ├── repositories/     # Flux repositories
    ├── .github/          # GitHub workflows
    ├── .devcontainer/    # Development environment
    └── .vscode/          # VSCode settings
```

## Key Components

### Core Services
- **Cilium**: CNI and network policy enforcement
- **MetalLB**: Load balancer for bare metal
- **Cert-Manager**: Certificate management
- **Flux**: GitOps continuous delivery

### Monitoring & Observability
- **Kube-Prometheus-Stack**: Prometheus, Grafana, AlertManager
- **Metrics Server**: Resource metrics

### Storage
- **Longhorn**: Distributed block storage
- **OpenEBS**: Container attached storage
- **CloudNative-PG**: PostgreSQL operator

### Networking
- **Blocky**: DNS proxy and ad blocker
- **NGINX Ingress**: Internal and external ingress
- **System Upgrade Controller**: Automated upgrades

## Usage

This template is designed to be used with TrueForge ForgeTool for cluster bootstrapping.

1. Configure cluster parameters in `base/clusterenv.yaml`
2. Customize patches in `patches/` for your node types
3. Add or modify applications in `kubernetes/`
4. Use ForgeTool to bootstrap the cluster

## License

See [LICENSE](LICENSE) for details.


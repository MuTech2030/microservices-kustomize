# Rhesis Worker Service

## Overview

This directory contains the Kubernetes manifests for deploying the Rhesis Worker microservice using Kustomize. The worker service is responsible for processing background tasks and jobs for the Rhesis platform.

## Structure

- `base/`: Base configuration for the microservice
  - `deployment.yaml`: Defines the worker deployment
  - `service.yaml`: Defines the worker service
  - `configmap.yaml`: Contains configuration data
  - `secret.yaml`: Contains sensitive data
  - `hpa.yaml`: Horizontal Pod Autoscaler configuration
  - `serviceaccount.yaml`: Service account for the worker
  - `kustomization.yaml`: Kustomize configuration for the base
- `overlay/`: Environment-specific overlays
  - `dev/`: Development environment configuration
  - `qa/`: QA environment configuration
  - `stage/`: Staging environment configuration
  - `prod/`: Production environment configuration
  - `dr/`: Disaster Recovery environment configuration

## Usage

To build the configuration for a specific environment:

```bash
# Development environment
kustomize build overlay/dev

# QA environment
kustomize build overlay/qa

# Staging environment
kustomize build overlay/stage

# Production environment
kustomize build overlay/prod

# Disaster Recovery environment
kustomize build overlay/dr
```

## Configuration

### Base Configuration

The base configuration includes:
- Deployment with 2 replicas
- Service exposing port 80
- ConfigMap with worker configuration
- Secret with sensitive data
- Horizontal Pod Autoscaler
- ServiceAccount

### Environment-Specific Configurations

Each environment overlay customizes the base configuration:

#### Development
- 1 replica
- Development-specific environment variables
- Reduced resource limits

#### QA
- 2 replicas
- QA-specific environment variables
- Moderate resource limits

#### Staging
- 3 replicas
- Staging-specific environment variables
- Higher resource limits

#### Production
- 5 replicas
- Production-specific environment variables
- High resource limits
- Zone-based topology spread constraints for high availability

#### Disaster Recovery
- 2 replicas
- DR-specific environment variables
- Moderate resource limits

## Security Considerations

- The worker service runs as a non-root user
- Privilege escalation is disabled
- All capabilities are dropped
- A seccomp profile is applied
- Sensitive data is stored in Kubernetes secrets

## Monitoring

The worker service exposes metrics on port 9090 that can be scraped by Prometheus for monitoring.


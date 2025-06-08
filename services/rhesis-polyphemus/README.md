# Rhesis Polyphemus Service

## Overview

The Rhesis Polyphemus service is the main API gateway and orchestration layer for the Rhesis microservices platform. It provides authentication, rate limiting, and request routing capabilities.

## Architecture

- **Component Type**: API Gateway
- **Port**: 8080
- **Health Endpoints**: `/healthz`, `/readyz`
- **Metrics Port**: 9090

## Features

- API Gateway functionality
- Authentication and authorization
- Rate limiting and throttling
- Request routing and load balancing
- CORS support
- Monitoring and metrics

## Configuration

The service is configured through:
- ConfigMap: `rhesis-polyphemus-config`
- Secret: `rhesis-polyphemus-secret`

## Deployment

### Base Configuration
Located in `base/` directory with core Kubernetes resources.

### Environment Overlays
- `dev`: Development environment with reduced resources
- `qa`: Quality assurance environment
- `stage`: Staging environment
- `prod`: Production environment with high availability
- `dr`: Disaster recovery environment

## Security

- Runs as non-root user (UID: 10001)
- Read-only root filesystem
- Security contexts and capabilities properly configured
- Uses trusted container registry (gcr.io)

## Dependencies

- Backend services for API routing
- Database for session management
- Cache for performance optimization


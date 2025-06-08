# Rhesis SDK Service

## Overview

The Rhesis SDK service provides developer tools, documentation, and client libraries for integrating with the Rhesis platform. It serves as the primary interface for third-party developers and partners.

## Architecture

- **Component Type**: SDK and Developer Tools
- **Port**: 8080
- **Health Endpoints**: `/healthz`, `/readyz`
- **Metrics Port**: 9090

## Features

- Multi-language SDK support (JavaScript, Python, Go, Java, C#)
- Interactive API documentation
- Swagger/OpenAPI specifications
- Code examples and tutorials
- Developer portal and resources
- API key management
- Rate limiting and usage analytics

## Configuration

The service is configured through:
- ConfigMap: `rhesis-sdk-config`
- ConfigMap: `rhesis-sdk-docs` (documentation content)
- Secret: `rhesis-sdk-secret`

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
- CORS support for web-based integrations
- API key authentication and authorization

## Dependencies

- Polyphemus API for backend integration
- Documentation storage and rendering
- Analytics and monitoring services

## Supported Languages

- **JavaScript/Node.js**: `@rhesis/sdk`
- **Python**: `rhesis-sdk`
- **Go**: `github.com/rhesis/sdk-go`
- **Java**: `com.rhesis:rhesis-sdk`
- **C#**: `Rhesis.SDK`

## Documentation

- Getting started guides
- API reference documentation
- Code examples and tutorials
- Best practices and patterns
- Integration guides


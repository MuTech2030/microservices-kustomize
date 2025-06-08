# Rhesis Frontend Service

## Overview

The Rhesis Frontend service is the user-facing web application for the Rhesis platform. It provides a modern, responsive interface for users to interact with the Rhesis ecosystem.

## Architecture

- **Component Type**: Frontend Web Application
- **Port**: 3000
- **Health Endpoints**: `/healthz`, `/readyz`
- **Technology**: Next.js/React

## Features

- Modern React-based user interface
- Server-side rendering (SSR)
- Progressive Web App (PWA) capabilities
- Responsive design for mobile and desktop
- Real-time updates and notifications
- Analytics and error reporting integration

## Configuration

The service is configured through:
- ConfigMap: `rhesis-frontend-config`
- Secret: `rhesis-frontend-secret`

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
- Content Security Policy (CSP) enabled
- XSRF protection enabled

## Dependencies

- Polyphemus API for backend communication
- Analytics service for user tracking
- Error reporting service for monitoring

## Performance

- Optimized bundle size
- Caching strategies implemented
- CDN integration ready
- Image optimization
- Code splitting


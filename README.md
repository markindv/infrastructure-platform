# Infrastructure Platform

Infrastructure Platform is a personal DevOps project focused on building a production-style infrastructure stack step by step.

The repository is designed as a growing platform where each module represents a separate infrastructure component.

## Current Modules

### Compose

A containerized environment built with:

- Nginx
- PostgreSQL 17
- Docker Compose
- Docker Volumes
- Docker Networks
- Environment Variables

Features:

- Multi-container deployment
- Persistent PostgreSQL storage
- Service communication through Docker Network
- Configuration via .env
- Data persistence validation

Location:

```text
compose/READMI.md
```

## Planned Modules

### CI/CD

Future implementation:

- GitHub Actions
- Automated testing
- Automated deployment

### Monitoring

Future implementation:

- Prometheus
- Grafana
- Metrics collection
- Alerting

### Terraform

Future implementation:

- Infrastructure as Code
- Cloud provisioning
- Reusable modules

## Project Structure

```text
infrastructure-platform/
├── compose/
├── ci-cd/
├── monitoring/
├── terraform/
└── README.md
```

## Author

Dmitry Markin


# Azure DevOps Demo Project

This repository demonstrates comprehensive Azure DevOps capabilities including CI/CD pipelines, Infrastructure as Code, containerization, and Kubernetes orchestration. PPR

## Project Overview

This project showcases:
- **CI/CD Pipelines**: Automated builds, tests, and deployments using Azure Pipelines and GitHub Actions
- **Infrastructure as Code**: Terraform scripts for Azure resource provisioning
- **Containerization**: Docker configurations for application deployment
- **Kubernetes**: Container orchestration on Azure Kubernetes Service (AKS)
- **Testing**: Unit and integration test suites
- **Monitoring**: Application Insights integration and health checks

## Project Structure

```
DevOpsDemo/
├── .github/workflows/           # GitHub Actions workflows
├── src/                         # Source code
│   ├── api/                    # REST API application
│   ├── frontend/               # Frontend application
│   └── shared/                 # Shared libraries
├── tests/                      # Test suites
│   ├── unit/                   # Unit tests
│   └── integration/            # Integration tests
├── infrastructure/             # Infrastructure as Code
│   ├── terraform/              # Terraform configurations
│   ├── docker/                 # Docker configurations
│   └── kubernetes/             # Kubernetes manifests
├── docs/                       # Documentation
├── azure-pipelines.yml         # Azure Pipelines configuration
└── README.md                   # This file
```

## Getting Started

### Prerequisites
- .NET 6.0 SDK or higher
- Docker and Docker Compose
- Terraform 1.0+
- kubectl and Azure CLI
- Node.js 16+ (for frontend)

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/PTPAC/DevOpsDemo.git
   cd DevOpsDemo
   ```

2. **Run with Docker Compose**
   ```bash
   cd infrastructure/docker
   docker-compose up -d
   ```

3. **Access the applications**
   - API: http://localhost:5000
   - Frontend: http://localhost:3000

### Running Tests

```bash
# Unit tests
dotnet test tests/unit/

# Integration tests
dotnet test tests/integration/
```

## Azure DevOps Pipeline Stages

### 1. Build Stage
- Code compilation
- Unit test execution
- Code quality analysis

### 2. Test Stage
- Integration tests
- Security scanning
- Performance testing

### 3. Deploy to Dev
- Automatic deployment to development environment
- Smoke tests

### 4. Deploy to Staging
- Manual approval required
- Staging environment deployment
- Load testing

### 5. Deploy to Production
- Manual approval required
- Blue-Green deployment strategy
- Health checks and monitoring

## Key Features

### CI/CD Pipelines
- **Azure Pipelines**: Multi-stage YAML-based pipeline
- **GitHub Actions**: Automated workflows for CI/CD
- **Pull Request Validation**: Automated checks on PR creation

### Infrastructure
- **Terraform**: IaC for Azure resources (App Service, AKS, ACR)
- **Docker**: Containerized applications
- **Kubernetes**: Orchestration manifests for AKS

### Testing
- **Unit Tests**: xUnit framework
- **Integration Tests**: Full stack testing
- **Code Coverage**: Track test coverage metrics

### Monitoring
- **Application Insights**: Real-time monitoring
- **Health Checks**: Endpoint availability monitoring
- **Logs**: Centralized logging configuration

## Environment Variables

Create a `.env` file in the root directory:

```env
AZURE_SUBSCRIPTION_ID=your_subscription_id
AZURE_TENANT_ID=your_tenant_id
AZURE_RESOURCE_GROUP=devops-demo-rg
AZURE_CONTAINER_REGISTRY=devopsdemoregistry
```

## Documentation

- [Architecture](docs/architecture.md) - System architecture and design
- [Deployment Guide](docs/deployment.md) - Detailed deployment instructions
- [Azure DevOps Setup](docs/azure-devops-setup.md) - Setting up Azure DevOps

## CI/CD Status

- Azure Pipelines: [![Build Status](https://dev.azure.com/PTPAC/DevOpsDemo/_apis/build/status/main)]()
- GitHub Actions: [![CI](https://github.com/PTPAC/DevOpsDemo/workflows/CI/badge.svg)](https://github.com/PTPAC/DevOpsDemo/actions)

## Contributing

1. Create a feature branch
2. Make your changes
3. Push to your branch
4. Create a Pull Request
5. Automated checks will run on PR creation

## License

This project is licensed under the Apache License 2.0 - see the LICENSE file for details.

## Contact

For questions or support, please open an issue in the repository.

---

Last Updated: 2026-02-12
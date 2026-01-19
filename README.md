# 🚀 EnginEdge Platform

> *Empowering engineers and technical professionals with intelligent AI-powered tools for productivity, learning, career development, and collaboration.*

[![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-2088FF?logo=github-actions&logoColor=white)](https://github.com/Engineer-s-Edge)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-Ready-326CE5?logo=kubernetes&logoColor=white)](https://kubernetes.io/)
[![Microservices](https://img.shields.io/badge/Architecture-Microservices-success)](https://microservices.io/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Python](https://img.shields.io/badge/Python-3.11-3776AB?logo=python&logoColor=white)](https://www.python.org/)

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Platform Architecture](#-platform-architecture)
- [Technology Stack](#-technology-stack)
- [Repository Structure](#-repository-structure)
- [Getting Started](#-getting-started)
- [CI/CD Pipeline](#-cicd-pipeline)
- [Documentation](#-documentation)
- [Development](#-development)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Overview

**EnginEdge** is a comprehensive, production-ready platform that leverages cutting-edge AI technologies to provide engineers with intelligent tools across their entire workflow. From technical interviews and resume optimization to document generation, scheduling, and data analytics, EnginEdge integrates seamlessly into the modern engineering lifecycle.

### What Makes EnginEdge Unique?

- **🤖 AI-First Design**: Built with LLMs and machine learning at the core
- **🏗️ Hexagonal Architecture**: Clean separation of concerns, highly maintainable
- **☁️ Cloud-Native**: Kubernetes-ready with Helm charts and automated CI/CD
- **📊 Data-Driven**: Integrated data lake with Trino, Spark, and Airflow
- **🔒 Enterprise-Grade**: OAuth2, JWT, RBAC, and comprehensive observability
- **⚡ High Performance**: Event-driven architecture with Apache Kafka
- **🧪 Tested**: Comprehensive unit, integration, and E2E testing
- **📦 Modular**: Independent microservices that can be deployed separately

---

## ✨ Key Features

### 🎤 **Technical Interview Platform**
- AI-powered interview simulations with real-time evaluation
- Adaptive question difficulty based on candidate responses
- Comprehensive feedback and skill gap analysis
- Multi-phase interview workflows (screening, technical, behavioral)

### 📄 **Resume Intelligence**
- Automated resume parsing and skill extraction
- ATS optimization and keyword analysis
- Gap analysis and career path recommendations
- Resume scoring against job descriptions

### 🧑‍💼 **Smart Scheduling**
- ML-powered meeting optimization
- Timezone-aware scheduling with conflict detection
- Calendar integration (Google, Outlook, iCal)
- Automatic rescheduling and reminder management

### 📝 **Document Generation**
- LaTeX-powered professional document creation
- Resume templates, cover letters, technical reports
- Real-time preview and collaborative editing
- Version control and template management

### 🤖 **AI Assistant & Agents**
- Context-aware engineering assistant
- Multi-tool agent orchestration
- Code analysis, debugging suggestions
- Natural language to code generation

### 📊 **Data Analytics Platform**
- Self-service analytics with Trino query engine
- Apache Spark for big data processing
- Apache Airflow for workflow orchestration
- MinIO-backed data lake with S3-compatible API
- Great Expectations for data quality validation

### 🔐 **Identity & Access Management**
- OAuth2 and OpenID Connect integration
- JWT token management with JWKS
- Role-based access control (RBAC)
- Multi-tenant user management

---

## 🏗️ Platform Architecture

EnginEdge follows **Hexagonal Architecture** (Ports & Adapters) with **Domain-Driven Design** principles:

```
┌─────────────────────────────────────────────────────────────────┐
│                          EnginEdge Platform                      │
└─────────────────────────────────────────────────────────────────┘

         ┌─────────────┐         ┌──────────────┐
         │  Frontend   │────────▶│ API Gateway  │
         │  (React)    │◀────────│  (NestJS)    │
         └─────────────┘         └──────┬───────┘
                                        │
                                        ▼
                            ┌─────────────────────┐
                            │      Hexagon        │
                            │   (Orchestration)   │
                            └──────────┬──────────┘
                                       │
            ┌──────────────────────────┼──────────────────────────┐
            │                          │                          │
            ▼                          ▼                          ▼
     ┌─────────────┐          ┌─────────────┐          ┌─────────────┐
     │  Assistant  │          │  Interview  │          │   Resume    │
     │   Worker    │          │   Worker    │          │   Worker    │
     └─────────────┘          └─────────────┘          └─────────────┘
            │                          │                          │
            ▼                          ▼                          ▼
     ┌─────────────┐          ┌─────────────┐          ┌─────────────┐
     │  Scheduling │          │    LaTeX    │          │    Tools    │
     │   Worker    │          │   Worker    │          │   Worker    │
     └─────────────┘          └─────────────┘          └─────────────┘
            │                          │                          │
            └──────────────────────────┼──────────────────────────┘
                                       │
                                       ▼
                          ┌─────────────────────┐
                          │     Apache Kafka     │
                          │  (Event Streaming)   │
                          └─────────────────────┘
                                       │
                                       ▼
                          ┌─────────────────────┐
                          │      Data Lake       │
                          │ (Trino/Spark/MinIO) │
                          └─────────────────────┘
```

### Architecture Patterns

- **Event-Driven**: Asynchronous communication via Apache Kafka
- **CQRS**: Command Query Responsibility Segregation for scalability
- **API Gateway Pattern**: Centralized routing, authentication, and rate limiting
- **Orchestration**: Hexagon service coordinates complex workflows
- **Domain-Driven Design**: Rich domain models with clear bounded contexts
- **Repository Pattern**: Abstract data persistence layer
- **Dependency Injection**: Loose coupling and high testability

---

## 🛠️ Technology Stack

### **Backend**
- **Node.js** (v18+) with **TypeScript** (v5.x)
- **NestJS** - Progressive Node.js framework
- **Python** (v3.11) - ML models and data processing
- **Apache Kafka** - Event streaming platform
- **PostgreSQL** - Primary relational database
- **MongoDB** - Document storage for flexible schemas
- **Redis** - Caching and session management

### **Frontend**
- **React** (v18+) with **TypeScript**
- **Next.js** - Server-side rendering and routing
- **Tailwind CSS** - Utility-first styling
- **Zustand** - State management
- **React Query** - Server state management
- **Shadcn/ui** - Component library

### **Data & Analytics**
- **Trino** - Distributed SQL query engine
- **Apache Spark** - Big data processing
- **Apache Airflow** - Workflow orchestration
- **MinIO** - S3-compatible object storage
- **Great Expectations** - Data quality validation
- **PostgreSQL** - Metadata and Hive Metastore

### **Infrastructure & DevOps**
- **Kubernetes** - Container orchestration
- **Helm** - Kubernetes package manager
- **Docker** - Containerization
- **GitHub Actions** - CI/CD automation
- **GitHub Container Registry (GHCR)** - Docker image registry
- **Prometheus & Grafana** - Monitoring and alerting
- **Loki** - Log aggregation
- **Tempo** - Distributed tracing

### **AI/ML**
- **OpenAI API** - GPT models for assistants
- **LangChain** - LLM orchestration
- **Vector Databases** - Semantic search
- **spaCy** - NLP processing
- **Scikit-learn** - ML models

### **Testing**
- **Jest** - Unit and integration testing
- **Pytest** - Python testing
- **Supertest** - API testing
- **Cypress** - E2E testing
- **ESLint** - Code linting
- **Prettier** - Code formatting

---

## 📁 Repository Structure

This is a **meta-repository** containing multiple independent Git repositories organized as subdirectories. Each component is maintained separately with its own CI/CD pipeline.

### Core Services

#### 🏛️ **[enginedge-core](./enginedge-core/)**
Core platform services and infrastructure.

- **`api-gateway/`** - Centralized API gateway with authentication, rate limiting, and routing (NestJS)
- **`hexagon/`** - Orchestration service coordinating worker interactions (NestJS)
- **`platform/`** - Kubernetes manifests, Helm charts, and infrastructure configurations

**Tech**: TypeScript, NestJS, Kubernetes, Helm  
**CI**: Automated testing, linting, Docker build on tags  
**Status**: ✅ Production Ready

---

#### ⚙️ **[enginedge-workers](./enginedge-workers/)**
Specialized microservices handling specific business domains.

| Worker | Description | Tech Stack |
|--------|-------------|------------|
| **`assistant-worker`** | AI assistant with context management and agent orchestration | TypeScript, NestJS, OpenAI |
| **`agent-tool-worker`** | Tool execution engine for AI agents (API calls, file ops, etc.) | TypeScript, NestJS |
| **`identity-worker`** | User authentication, OAuth2, JWT token management | TypeScript, NestJS, PostgreSQL |
| **`interview-worker`** | Technical interview platform with real-time evaluation | TypeScript, NestJS, MongoDB |
| **`latex-worker`** | LaTeX document generation and compilation | TypeScript, NestJS, LaTeX |
| **`resume-worker`** | Resume parsing, analysis, and optimization | TypeScript, NestJS, spaCy |
| **`scheduling-worker`** | Smart scheduling with ML-powered optimization | TypeScript, NestJS, PostgreSQL |
| **`news-worker`** | News aggregation and engineering content curation | TypeScript, NestJS |

**Tech**: TypeScript, NestJS, MongoDB, PostgreSQL, Redis, Kafka  
**CI**: Independent CI per worker, automated deployment on tags  
**Status**: ✅ Production Ready

---

#### 🗄️ **[enginedge-datalake](./enginedge-datalake/)**
Enterprise data lake with analytics and processing capabilities.

- **Trino** - Distributed SQL query engine
- **Apache Spark** - Big data processing and ETL
- **Apache Airflow** - Workflow orchestration and scheduling
- **MinIO** - S3-compatible object storage
- **PostgreSQL** - Hive Metastore
- **Great Expectations** - Data quality validation
- **Observability** - Monitoring and alerting service

**Tech**: TypeScript, Python, Trino, Spark, Airflow, MinIO, Kubernetes  
**CI**: Multi-stage testing, Docker Compose validation, security scanning  
**Status**: ✅ Production Ready

---

#### 🎨 **[enginedge-frontend](./enginedge-frontend/)**
Modern web application with responsive design.

- **Pages**: Dashboard, Interviews, Resumes, Documents, Scheduling, Admin
- **Components**: Design system with reusable UI components
- **Authentication**: OAuth2 integration with PKCE flow
- **Real-time**: WebSocket connections for live updates

**Tech**: React, Next.js, TypeScript, Tailwind CSS, Zustand, React Query  
**CI**: Linting, testing, build verification  
**Status**: 🚧 Active Development

---

#### 🐍 **[enginedge-local-kernel](./enginedge-local-kernel/)**
Python execution kernel for local code execution and testing.

**Tech**: Python 3.11, FastAPI  
**CI**: Python linting, testing, Docker build  
**Status**: ✅ Production Ready

---

#### 🧠 **[enginedge-scheduling-model](./enginedge-scheduling-model/)**
Machine learning models for intelligent scheduling optimization.

**Tech**: Python 3.11, Scikit-learn, TensorFlow  
**CI**: Python testing, model validation, Docker build  
**Status**: ✅ Production Ready

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** 18+ and npm/yarn
- **Python** 3.11+
- **Docker** and Docker Compose
- **Kubernetes** cluster (for production)
- **kubectl** configured
- **Helm** 3+ (for Kubernetes deployments)

### Quick Start (Local Development)

#### 1. Clone the Repository
```bash
git clone https://github.com/Engineer-s-Edge/EnginEdge.git
cd EnginEdge
```

#### 2. Set Up Individual Components

Each component has its own README with specific setup instructions:

```bash
# Core services
cd enginedge-core
# See enginedge-core/README.md for setup

# Workers
cd enginedge-workers/assistant-worker
npm install
# See individual worker READMEs

# Data lake
cd enginedge-datalake
docker-compose up -d
# See enginedge-datalake/README.md

# Frontend
cd enginedge-frontend
npm install
npm run dev
```

#### 3. Deploy to Kubernetes (Production)

```bash
# Deploy all services
./scripts/deploy_k8s_all.sh

# Or deploy individually
cd enginedge-core/platform/helm
helm upgrade --install enginedge-core ./enginedge-core

cd enginedge-datalake/helm
helm upgrade --install enginedge-datalake ./datalake
```

#### 4. Verify Deployment

```bash
# Check all pods
kubectl get pods -A | grep enginedge

# Check services
kubectl get svc -A | grep enginedge

# Access API Gateway
kubectl port-forward svc/api-gateway 3000:3000
curl http://localhost:3000/health
```

### Environment Variables

Each service requires environment variables. See `.env.example` files in each component directory.

**Required Secrets**:
- `GITHUB_TOKEN` - For CI/CD and GHCR access (automatically provided in GitHub Actions)
- `KUBECONFIG` / `KUBECONFIG_B64` - For Kubernetes deployments
- `OPENAI_API_KEY` - For AI features
- `DATABASE_URL` - PostgreSQL connection string
- `MONGODB_URI` - MongoDB connection string
- `KAFKA_BROKERS` - Kafka broker addresses
- `REDIS_URL` - Redis connection string

---

## 🔄 CI/CD Pipeline

EnginEdge uses **GitHub Actions** for automated CI/CD across all repositories.

### Pipeline Stages

#### **On Push to `main` or `dev` Branches**
1. ✅ **Checkout** - Clone repository
2. ✅ **Lint** - ESLint (TypeScript) or Black/Flake8 (Python)
3. ✅ **Format Check** - Prettier (TypeScript) or Black/isort (Python)
4. ✅ **Unit Tests** - Jest (TypeScript) or Pytest (Python)
5. ✅ **Integration Tests** - Full test suite
6. ✅ **Build Verification** - Ensure code compiles
7. ✅ **Security Scan** - Trivy vulnerability scanning
8. ❌ **NO DEPLOYMENT** - Only testing on branch pushes

#### **On Tag Push** (e.g., `v1.0.0`, `api-gateway-v1.0.0`)
1. ✅ **Run All Tests** - Ensure quality before deployment
2. ✅ **Build Docker Image** - Multi-stage Docker build
3. ✅ **Push to GHCR** - Tag as `v1.0.0` and `latest`
4. ✅ **Deploy to Kubernetes** - Helm upgrade (if configured)
5. ✅ **Smoke Tests** - Verify deployment health
6. ✅ **Notifications** - Success/failure notifications

### Deployment Strategy

```bash
# Example: Deploy api-gateway v1.2.3
cd enginedge-core
git tag api-gateway-v1.2.3
git push origin api-gateway-v1.2.3

# CI automatically:
# 1. Runs all tests
# 2. Builds Docker image: ghcr.io/engineer-s-edge/api-gateway:1.2.3
# 3. Deploys to Kubernetes
```

### Supported Tag Patterns

- `v*.*.*` - Deploy all services with the same version
- `api-gateway-v*.*.*` - Deploy only API Gateway
- `hexagon-v*.*.*` - Deploy only Hexagon
- `*-worker-v*.*.*` - Deploy specific worker
- `datalake-v*.*.*` - Deploy Data Lake
- `local-kernel-v*.*.*` - Deploy Local Kernel
- `scheduling-model-v*.*.*` - Deploy Scheduling Model

### GitHub Actions Workflows

| Repository | Workflows | Status |
|------------|-----------|--------|
| **enginedge-core** | `api-gateway-ci.yml`, `core-hexagon-ci.yml` | ✅ Passing |
| **enginedge-workers** | `workers-ci.yml` (matrix for all 8 workers) | ✅ Passing |
| **enginedge-datalake** | `datalake-ci.yml`, `deploy.yml` | ✅ Passing |
| **enginedge-local-kernel** | `local-kernel-ci.yml` | ✅ Passing |
| **enginedge-scheduling-model** | `scheduling-model-ci.yml` | ✅ Passing |

---

## 📚 Documentation

### Architecture Decision Records (ADRs)

- **[ADR-001: API Gateway Routing Only](./docs/ADR-001-api-gateway-routing-only.md)** - Why API Gateway handles routing and auth, not business logic
- **[ADR-002: Hexagon Orchestration](./docs/ADR-002-hexagon-orchestration.md)** - How Hexagon coordinates worker interactions

### Guides

- **[Developer Onboarding](./DEVELOPER_ONBOARDING.md)** - Complete setup guide for new developers
- **[Feature Summary](./FEATURE_SUMMARY.md)** - Detailed overview of all platform features
- **[Operations Runbook](./OPERATIONS_RUNBOOK.md)** - Deployment, monitoring, and troubleshooting
- **[Testing Guide](./TESTING_GUIDE.md)** - Testing strategies and best practices
- **[Deployment Runbook](./docs/DEPLOYMENT-RUNBOOK.md)** - Step-by-step deployment instructions
- **[Observability](./docs/OBSERVABILITY.md)** - Monitoring, logging, and tracing setup
- **[Troubleshooting](./docs/TROUBLESHOOTING.md)** - Common issues and solutions
- **[Performance Optimization](./docs/PERFORMANCE-OPTIMIZATION.md)** - Performance tuning guide

### Repository-Specific Documentation

Each repository contains its own comprehensive README:

- [enginedge-core/README.md](./enginedge-core/README.md)
- [enginedge-workers/README.md](./enginedge-workers/README.md)
- [enginedge-datalake/README.md](./enginedge-datalake/README.md)
- [enginedge-frontend/README.md](./enginedge-frontend/README.md)
- [enginedge-local-kernel/README.md](./enginedge-local-kernel/README.md)
- [enginedge-scheduling-model/README.md](./enginedge-scheduling-model/README.md)

---

## 💻 Development

### Development Scripts

Utility scripts located in `scripts/`:

```bash
# Kubernetes Deployment
./scripts/deploy_k8s_all.sh       # Deploy all services (Linux/macOS)
./scripts/deploy_k8s_all.ps1      # Deploy all services (Windows)
./scripts/destroy_k8s_all.sh      # Remove all services (Linux/macOS)
./scripts/destroy_k8s_all.ps1     # Remove all services (Windows)

# Code Formatting
./scripts/format-all.sh            # Format all TypeScript and Python code (Linux/macOS)
./scripts/format-all.ps1           # Format all code (Windows)

# Individual Service Management
./scripts/build-push-one.ps1       # Build and push a single service (Windows)
```

### Code Quality

- **Linting**: ESLint (TypeScript), Flake8 (Python)
- **Formatting**: Prettier (TypeScript), Black + isort (Python)
- **Type Checking**: TypeScript strict mode
- **Testing**: Jest (TypeScript), Pytest (Python)
- **Pre-commit Hooks**: Automated linting and formatting on commit

### Running Tests Locally

```bash
# TypeScript (NestJS workers)
cd enginedge-workers/assistant-worker
npm install
npm run test              # Unit tests
npm run test:e2e          # E2E tests
npm run test:cov          # Coverage report

# Python (Data Lake, Scheduling Model)
cd enginedge-datalake
pip install -r requirements.txt
pytest tests/             # All tests
pytest tests/unit/        # Unit tests only
pytest tests/integration/ # Integration tests

# Format check
npm run lint:check        # TypeScript
npm run format:check      # TypeScript formatting
black --check .           # Python formatting
isort --check .           # Python import sorting
```

### Architecture Principles

1. **Domain-Driven Design**: Rich domain models with clear bounded contexts
2. **Hexagonal Architecture**: Ports & Adapters pattern for clean separation
3. **SOLID Principles**: Single responsibility, dependency inversion
4. **Event-Driven**: Asynchronous messaging via Kafka
5. **API-First**: OpenAPI specs for all HTTP endpoints
6. **Cloud-Native**: 12-factor app methodology
7. **Test-Driven**: Comprehensive unit and integration testing
8. **Security-First**: OAuth2, RBAC, input validation

---

## 🤝 Contributing

We welcome contributions! Here's how to get started:

### 1. Read the Documentation
- [DEVELOPER_ONBOARDING.md](./DEVELOPER_ONBOARDING.md) - Setup instructions
- [TESTING_GUIDE.md](./TESTING_GUIDE.md) - Testing requirements
- Component-specific READMEs for coding standards

### 2. Fork and Clone
```bash
git clone https://github.com/YOUR_USERNAME/EnginEdge.git
cd EnginEdge
```

### 3. Create a Feature Branch
```bash
git checkout -b feature/amazing-new-feature
```

### 4. Make Changes
- Follow existing code style and patterns
- Write tests for new functionality
- Update documentation as needed

### 5. Run Tests and Linting
```bash
# Format code
./scripts/format-all.sh

# Run tests
cd [component-directory]
npm test  # or pytest for Python
```

### 6. Commit and Push
```bash
git add .
git commit -m "feat: Add amazing new feature"
git push origin feature/amazing-new-feature
```

### 7. Open a Pull Request
- Provide a clear description of changes
- Reference any related issues
- Ensure all CI checks pass

### Contribution Guidelines

- **Code Style**: Follow ESLint/Prettier (TypeScript) or Black/Flake8 (Python)
- **Commit Messages**: Use conventional commits (feat:, fix:, docs:, etc.)
- **Testing**: Maintain or improve code coverage
- **Documentation**: Update READMEs for any new features
- **Security**: Never commit secrets or sensitive data

---

## 📄 License

Individual components may have their own licenses. See each repository for details.

---

## 🌟 Showcase

### Performance Metrics

- **API Gateway**: ~5ms median response time
- **Worker Services**: Sub-100ms processing for typical requests
- **Data Lake**: Queries across 10M+ records in seconds (Trino)
- **High Availability**: 99.9% uptime with multi-replica deployments

### Scalability

- **Horizontal Scaling**: Independent scaling per service
- **Auto-scaling**: Kubernetes HPA based on CPU/memory
- **Load Balancing**: Built-in Kubernetes service load balancing
- **Event Streaming**: Kafka handles 1000+ events/second

### Security Features

- **Authentication**: OAuth2 + OpenID Connect
- **Authorization**: JWT tokens with role-based access control
- **API Security**: Rate limiting, input validation, CORS
- **Container Security**: Regular Trivy scans, minimal base images
- **Secrets Management**: Kubernetes secrets, never committed to git
- **Network Policies**: Kubernetes network isolation

---

## 📞 Contact & Links

- **GitHub Organization**: [Engineer-s-Edge](https://github.com/Engineer-s-Edge)
- **Documentation**: This repository's `docs/` folder
- **Issues**: GitHub Issues in respective repositories
- **Discussions**: GitHub Discussions (coming soon)

---

<div align="center">

**Built with ❤️ by engineers, for engineers**

⭐ **Star this repo** if you find it useful! ⭐

</div>

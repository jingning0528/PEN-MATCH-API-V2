# PEN Match API V2

Backend and AI services for the **Personal Education Number (PEN) Match** system, developed as part of a Government of British Columbia project.

This repository contains a FastAPI-based backend that integrates machine learning, Azure AI services, search, data storage, and agent-based workflows to support PEN matching and related services.

> **Portfolio note:** This repository is based on the original [BC Government PEN Match API V2](https://github.com/bcgov/PEN-MATCH-API-V2) project. I contributed to the project as part of my work with the Government of British Columbia. This fork is maintained to document the system architecture, technical stack, and my engineering contributions.

---

## My Contributions

I independently designed and implemented **PEN Match API V2 end-to-end** for the Government of British Columbia, covering the backend architecture, machine-learning workflows, AI integration, cloud infrastructure, and deployment.

Key areas of ownership included:

- Designed the overall **system architecture** and modular backend structure.
- Built the **FastAPI backend**, including API endpoints, request/response validation, configuration, logging, and service integration.
- Developed the **PEN matching and evaluation workflows** for processing and assessing student-record matching results.
- Implemented **Azure OpenAI, Azure AI Search, LangChain, and LangGraph** components for retrieval and agent-based AI workflows.
- Integrated cloud services including **Azure Cosmos DB, Blob Storage, Key Vault, and Document Intelligence**.
- Built evaluation and model-improvement components, including prompt testing and fine-tuning-related workflows.
- Containerized the application using **Docker** and implemented Azure infrastructure using **Terraform**.
- Set up **GitHub Actions CI/CD workflows** to support automated build and deployment processes.

The project reflects end-to-end ownership of a production-oriented ML/AI system, from application and model integration to cloud infrastructure and deployment.

---

## System Overview

PEN Match supports the process of identifying and matching student records with Personal Education Numbers.

The V2 backend combines traditional backend services with machine-learning and modern AI components.

At a high level:

```text
Client / External Service
          |
          v
     FastAPI API
          |
          +--------------------+
          |                    |
          v                    v
   PEN Matching Logic     PEN Agent / AI
          |                    |
          v                    +----> Azure OpenAI
   Data Processing             |
          |                    +----> Azure AI Search
          v                    |
   Database / Storage          +----> LangGraph / LangChain
          |
          v
   Evaluation Pipeline
```

The repository also contains infrastructure-as-code and deployment configuration for Azure-based environments.

---

## Tech Stack

### Backend

- **Python 3.11+**
- **FastAPI**
- **Uvicorn**
- **Pydantic**
- **HTTPX**
- REST APIs

### Machine Learning & Data

- **scikit-learn**
- **NumPy**
- **Pandas**
- Matching and ranking workflows
- Model evaluation pipelines

### Generative AI & Agents

- **Azure OpenAI**
- **OpenAI API**
- **LangChain**
- **LangGraph**
- Retrieval and agent-based workflows
- Embedding-based search

### Azure

- **Azure AI Search**
- **Azure Cosmos DB**
- **Azure Blob Storage**
- **Azure Key Vault**
- **Azure Document Intelligence**
- **Azure Identity**

### Infrastructure & Deployment

- **Docker**
- **Terraform**
- **GitHub Actions**
- Azure infrastructure-as-code
- CI/CD workflows

### Other

- **Redis**
- **pytest / pytest-asyncio**
- Structured logging

---

## Repository Structure

```text
PEN-MATCH-API-V2/
│
├── app/
│   ├── api/                 # FastAPI endpoints and application entry points
│   ├── azure_search/        # Azure AI Search integration
│   ├── config/              # Application configuration
│   ├── core/                # Core application logic
│   ├── database/            # Data-access components
│   ├── evaluation/          # Matching/model evaluation
│   ├── fine_tune/           # Model fine-tuning components
│   ├── pen_agent/           # Agent-based AI functionality
│   ├── Dockerfile
│   ├── pyproject.toml
│   └── requirements.txt
│
├── infra/
│   ├── modules/             # Reusable Terraform modules
│   ├── main.tf
│   ├── providers.tf
│   └── variables.tf
│
├── .github/
│   └── workflows/           # CI/CD workflows
│
└── initial-azure-setup.sh   # Azure environment setup
```

---

## Architecture

The application follows a modular service architecture.

### API Layer

FastAPI exposes the backend functionality through REST endpoints. Pydantic models are used for request/response validation and structured application configuration.

### Matching & ML Layer

The application contains data-processing, matching, and evaluation components used to support PEN record matching.

The ML stack includes scikit-learn, NumPy, and Pandas, with dedicated evaluation modules for assessing matching behavior.

### AI & Retrieval Layer

The V2 system also includes modern AI components built around:

```text
User / Service Request
        |
        v
    PEN Agent
        |
        v
    LangGraph
     /     \
    v       v
Azure     Azure AI
OpenAI     Search
    \       /
     v     v
   Retrieved Context
        |
        v
   Generated Result
```

Azure OpenAI provides language-model capabilities while Azure AI Search supports retrieval and search workflows.

### Data Layer

The backend integrates with Azure services including:

- Cosmos DB
- Blob Storage
- AI Search
- Key Vault

### Infrastructure Layer

Infrastructure is defined using Terraform modules and deployed to Azure. Docker is used to containerize the backend, while GitHub Actions provides automated workflows.

---

## Running Locally

### Requirements

- Python 3.11+
- Docker (optional)
- Required Azure credentials and service configuration

### Install dependencies

```bash
cd app

python -m venv .venv
source .venv/bin/activate

pip install -r requirements.txt
```

### Run the API

```bash
python run_api.py
```

The FastAPI application runs by default on:

```text
http://localhost:8000
```

Interactive API documentation is typically available at:

```text
http://localhost:8000/docs
```

Some functionality requires access to the corresponding Azure services and environment configuration.

---

## Engineering Focus

This project is particularly relevant to my experience in:

**Machine Learning Engineering**
- ML-backed application development
- Matching and ranking systems
- Model evaluation
- Data processing

**Backend Engineering**
- Python backend development
- REST API design
- Modular service architecture
- Production-oriented application integration

**Cloud & MLOps**
- Azure AI services
- Docker
- Terraform
- CI/CD
- Cloud-based model and search services

**Enterprise AI**
- Azure OpenAI
- Retrieval
- AI search
- Agent workflows
- Integration of AI components into existing backend systems

---

## Project Context

PEN Match is part of the Government of British Columbia's education technology ecosystem.

The original project is maintained under the BC Government GitHub organization:

**Original repository:**  
https://github.com/bcgov/PEN-MATCH-API-V2

This repository is presented as a portfolio/reference version of work performed on the project. The underlying project is a collaborative government software project; sections labeled **My Contributions** describe my individual engineering work rather than the work of the entire project team.

---

## License

Please refer to the original BC Government repository and its applicable licensing terms for reuse and distribution.

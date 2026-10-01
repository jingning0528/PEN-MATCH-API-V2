## My Contributions

I independently designed and implemented **PEN Match API V2 end-to-end** for the Government of British Columbia, covering the full lifecycle from system architecture and ML/AI development to cloud infrastructure and deployment.

My work included:

- **System Architecture** — Designed the modular backend architecture integrating REST APIs, machine-learning pipelines, AI services, data storage, and cloud infrastructure.

- **Backend Development** — Built the backend service with **Python and FastAPI**, including API endpoints, request/response validation, configuration, logging, error handling, and integration between application components.

- **ML-Based PEN Matching** — Developed the data-processing and machine-learning workflows used to support automated student-record matching, including feature processing, matching logic, and model evaluation.

- **AI Agent & LLM Integration** — Designed and implemented the PEN Agent using **Azure OpenAI, LangChain, and LangGraph**, integrating LLM capabilities into the existing backend system.

- **Retrieval & Search** — Integrated **Azure AI Search** and embedding-based retrieval to provide relevant information and context to AI workflows.

- **Model Evaluation & Improvement** — Built evaluation pipelines for measuring system performance, analyzing matching results, testing prompts and AI workflows, and iteratively improving system behavior.

- **Fine-Tuning Pipeline** — Implemented components for preparing data and experimenting with model fine-tuning as part of the system's model-improvement workflow.

- **Data & Azure Services** — Integrated **Azure Cosmos DB, Blob Storage, Key Vault, Document Intelligence, and Azure Identity** for application data, document processing, credentials, and cloud-service access.

- **Infrastructure as Code** — Designed the Azure deployment infrastructure using **Terraform**, including modular infrastructure definitions for networking and backend services.

- **Containerization & Deployment** — Containerized the application with **Docker** and configured the application for deployment in an Azure environment.

- **CI/CD** — Implemented **GitHub Actions** workflows to automate build, deployment, and development processes.

### Engineering Scope

The project demonstrates end-to-end ownership of a production-oriented ML/AI system:

```text
Data
  ↓
Data Processing
  ↓
ML Matching ──────────→ Evaluation
  ↓
FastAPI Backend
  ↓
AI Agent / Retrieval
  ├── Azure OpenAI
  ├── Azure AI Search
  └── LangGraph / LangChain
  ↓
Azure Services
  ↓
Docker + Terraform + GitHub Actions
  ↓
Cloud Deployment
```

Rather than developing an isolated machine-learning model, I built the surrounding engineering system required to integrate ML and generative AI capabilities into a deployable backend application.

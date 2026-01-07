# Hi, I'm Ryan Bumstead 👋

### ☁️ Salesforce Platform Architect

**📄 Professional Materials**  
[![PDF Resume](https://img.shields.io/badge/PDF_Resume-ec1c24?logo=adobeacrobatreader&logoColor=white)](https://github.com/rdbumstead/resume-as-code/releases/latest/download/RyanBumstead_Resume.pdf) [![Resume Source](https://img.shields.io/badge/Source_Markdown-000000?logo=markdown&logoColor=white)](https://github.com/rdbumstead/resume-as-code/blob/main/markdown/RyanBumstead_Resume.md) [![Portfolio](https://img.shields.io/badge/Portfolio-ryanbumstead.com-4A90E2?logo=googlechrome&logoColor=white)](https://ryanbumstead.com)

**📫 Connect With Me**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ryan_Bumstead-0077B5?logo=linkedin&logoColor=white)](https://linkedin.com/in/ryanbumstead) [![Email](https://img.shields.io/badge/Email-ryan@ryanbumstead.com-D14836?logo=gmail&logoColor=white)](mailto:ryan@ryanbumstead.com) [![Trailhead](https://img.shields.io/badge/Trailhead-rbumstead-00A1E0?logo=salesforce&logoColor=white)](https://www.salesforce.com/trailblazer/rbumstead)

---

I bridge the gap between executive strategy and enforceable technical architecture, specializing in **architecture-first delivery**, **DevOps maturity**, and **resilience engineering** for governed, multi-cloud systems (Salesforce + AWS).

### 🛠 Tech Stack

| Domain | Stack |
| :--- | :--- |
| **☁️ Salesforce** | **Apex** · **LWC** · **Agentforce** · **Flow Builder** |
| **⚡ Cloud** | **AWS Lambda** · **S3** · **Multi-Cloud Architecture** |
| **🚀 DevOps** | **GitHub Actions** · **SFDX CLI** · **Docker** · **PMD** |
| **📐 Architecture** | **OpenAPI 3.0** · **Event-Driven** · **C4 Modeling** |

### 📐 System Architecture
*A high-level view of the multi-cloud pattern used in my reference implementation.*

```mermaid
graph LR
    %% Define Styles
    classDef sfdc fill:#00A1E0,stroke:#005FB2,stroke-width:2px,color:white,font-weight:bold;
    classDef aws fill:#FF9900,stroke:#CC7A00,stroke-width:2px,color:white,font-weight:bold;
    classDef jira fill:#0052CC,stroke:#0747A6,stroke-width:2px,color:white,font-weight:bold;
    classDef github fill:#24292F,stroke:#1B1F23,stroke-width:2px,color:white,font-weight:bold;
    classDef user fill:#333333,stroke:#000000,stroke-width:2px,color:white,font-weight:bold;
    classDef future fill:#FFE5B4,stroke:#FFA500,stroke-width:2px,stroke-dasharray: 5 5;

    %% Nodes
    User((User))
    LWR[Experience Cloud LWR]
    SF_GQL[Salesforce GraphQL API]
    DB[(Custom Objects)]
    Lambda[AWS Lambda Gateway<br/>Phase 8 - Q2 2026]
    Apex[Apex Runtime]
    AI[Agentforce Agent]
    Jira[Jira API]
    GitHub[GitHub API]
    Resume[Resume Engine<br/>Future]

    %% Live MVP Connections (Solid)
    User --> LWR
    LWR -->|Native GraphQL<br/>lightning/uiGraphQLApi| SF_GQL
    SF_GQL --> DB
    LWR -->|Apex REST| Apex
    Apex <--> AI
    Apex -->|REST via<br/>Named Credentials| Jira
    Apex -->|REST via<br/>Named Credentials| GitHub

    %% Phase 8 Connections (Dashed)
    LWR -.->|Phase 8<br/>Design Complete| Lambda
    Lambda -.->|Function URL| Apex
    Lambda -.->|Serverless| Resume

    %% Apply Styles
    class LWR,SF_GQL,DB,Apex,AI sfdc;
    class Lambda,Resume aws;
    class Jira jira;
    class GitHub github;
    class User user;

    %% Link Styling
    linkStyle 0,1,2,3,4,5,6 stroke:#2ECC71,stroke-width:3px;
    linkStyle 7,8,9 stroke:#FFA500,stroke-width:2px,stroke-dasharray:5;
```

---

### 📂 Engineering Highlights

#### [Salesforce Platform Architect Portfolio](https://github.com/rdbumstead/salesforce-platform-architect-portfolio)
[![CI/CD — main](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy.yml/badge.svg?branch=main)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy.yml) [![PR Validation](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/pr.yml/badge.svg)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/pr.yml) [![Cloudflare Worker](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy-worker.yml/badge.svg)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy-worker.yml) [![Daily Org Heartbeat](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/keep-alive.yml/badge.svg)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/keep-alive.yml)
> *An open-source reference implementation for enterprise delivery patterns.*

* **The Architecture:** Designed a multi-cloud system using Salesforce LWR, GraphQL, Apex, and AWS Lambda.
* **The Governance:** Implemented contract-first APIs (OpenAPI 3.0) and "Chaos Engineering" patterns to validate resilience against third-party failures.
* **The Ops:** Zero-touch CI/CD with automated quality gates.
* **Documentation:** Read my [Architectural Decision Records (ADRs)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/tree/main/docs/adr) to see how I handle security, FinOps, and resilience trade-offs.

#### ["Resume as Code" CI/CD Pipeline](https://github.com/rdbumstead/resume-as-code)
[![Build Status](https://github.com/rdbumstead/resume-as-code/actions/workflows/resume-pipeline.yml/badge.svg)](https://github.com/rdbumstead/resume-as-code) [![Import Status](https://github.com/rdbumstead/resume-as-code/actions/workflows/import-resume.yml/badge.svg)](https://github.com/rdbumstead/resume-as-code)
> *Treating professional career documentation as a software product.*

* **Infrastructure as Code:** An event-driven pipeline that transforms Markdown source into immutable PDF artifacts using GitHub Actions and Docker.
* **Security First:** Implemented a "Secrets-First" pattern, decoupling PII (Phone/Email) from the codebase using GitHub Secrets.
* **Automated Quality:** Custom Node.js scripts audit hyperlinks and inject portfolio statistics before compilation.

### 📜 Certifications
* Salesforce Agentforce Specialist
* Salesforce Data Cloud Consultant
* Salesforce Education Cloud Consultant
* Salesforce Platform App Builder
* Salesforce Administrator I & II

---

*Looking for a Salesforce Platform Architect who thinks in systems and delivers with precision? Let's connect above!*

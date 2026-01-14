# Hi, I'm Ryan Bumstead 👋

### ☁️ Salesforce Platform Architect

**📄 Professional Materials**  
[![PDF Resume](https://img.shields.io/badge/PDF_Resume-ec1c24?logo=adobeacrobatreader&logoColor=white)](https://github.com/rdbumstead/resume-as-code/blob/main/pdf/RyanBumstead_Resume.pdf) [![Resume Source](https://img.shields.io/badge/Source_Markdown-000000?logo=markdown&logoColor=white)](https://github.com/rdbumstead/resume-as-code/blob/main/markdown/RyanBumstead_Resume.md) [![Portfolio](https://img.shields.io/badge/Portfolio-ryanbumstead.com-4A90E2?logo=googlechrome&logoColor=white)](https://ryanbumstead.com)

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
    %%{init: {'flowchart': {'nodeSpacing': 50, 'rankSpacing': 50}}}%%
    %% ========= BRAND STYLES =========
    classDef user fill:#424242,stroke:#000000,stroke-width:2px,color:#ffffff,font-weight:bold;
    classDef sfdc fill:#00A1E0,stroke:#005FB2,stroke-width:2px,color:#ffffff,font-weight:bold;
    classDef aws fill:#FF9900,stroke:#CC7A00,stroke-width:2px,color:#ffffff,font-weight:bold;
    classDef jira fill:#0052CC,stroke:#003A8F,stroke-width:2px,color:#ffffff,font-weight:bold;
    classDef github fill:#24292E,stroke:#000000,stroke-width:2px,color:#ffffff,font-weight:bold;
    classDef data fill:#8E24AA,stroke:#4A148C,stroke-width:2px,color:#ffffff,font-weight:bold;
    classDef future fill:#FFF3E0,stroke:#FB8C00,stroke-width:2px,stroke-dasharray:5 5;

    %% ========= NODES =========
    User((User))
    LWR[Experience Cloud<br/>LWR]
    GQL[Salesforce<br/>GraphQL]
    Apex[Apex Runtime]
    DB[(Custom Objects)]
    AI[Agentforce]
    Jira[Jira Cloud API]
    GitHub[GitHub API]
    Lambda[AWS Lambda<br/>Phase 8]

    %% ========= FLOWS =========
    User --> LWR
    LWR --> GQL
    GQL --> DB
    LWR --> Apex
    Apex <--> AI
    Apex --> Jira
    Apex --> GitHub

    %% ========= FUTURE =========
    LWR -.-> Lambda
    Lambda -.-> Apex

    %% ========= APPLY STYLES =========
    class User user;
    class LWR,GQL,Apex,AI sfdc;
    class DB data;
    class Jira jira;
    class GitHub github;
    class Lambda aws;

    %% ========= CRITICAL PATH =========
    linkStyle 0,1,2 stroke:#2ECC71,stroke-width:3px;
```

---

### 📂 Engineering Highlights

#### [Salesforce Platform Architect Portfolio](https://github.com/rdbumstead/salesforce-platform-architect-portfolio)
[![CI/CD — main](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy.yml/badge.svg?branch=main)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy.yml) [![PR Validation](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/pr.yml/badge.svg)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/pr.yml) [![Cloudflare Worker](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy-worker.yml/badge.svg)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy-worker.yml) [![Daily Org Heartbeat](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/keep-alive.yml/badge.svg)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/keep-alive.yml)

> *An open-source reference implementation for enterprise delivery patterns.*

> [!TIP]
> **View the full documentation in the [Governance Hub](https://rdbumstead.github.io/salesforce-platform-architect-portfolio/) for the best reading experience.**

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

#### [Setup Salesforce CLI Action](https://github.com/rdbumstead/setup-salesforce-action)
[![GitHub Marketplace](https://img.shields.io/badge/Marketplace-Setup%20Salesforce%20CLI-blue.svg)](https://github.com/marketplace/actions/setup-salesforce-cli) [![GitHub release](https://img.shields.io/github/v/release/rdbumstead/setup-salesforce-action)](https://github.com/rdbumstead/setup-salesforce-action/releases) [![Test Action](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test.yml/badge.svg)](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test.yml)

> *A production-ready GitHub Action for Salesforce CI/CD pipelines.*

* **Performance:** 20-45 second setup with intelligent caching (vs 2-3 min without)
* **Security:** JWT-based authentication with automatic key cleanup
* **Flexibility:** Fully optional plugin system - install only what you need
* **Community Impact:** Published to GitHub Marketplace for the Salesforce ecosystem

### 📜 Certifications
* Salesforce Certified Agentforce Specialist
* Salesforce Certified Data Cloud Consultant
* Salesforce Certified Education Cloud Consultant
* Salesforce Certified Platform App Builder
* Salesforce Certified Platform Administrator
* Salesforce Certified Platform Administrator II

[Verify these credentials on Trailhead ↗](https://www.salesforce.com/trailblazer/rbumstead)

---

*Looking for a Salesforce Platform Architect who thinks in systems and delivers with precision? Let's connect above!*

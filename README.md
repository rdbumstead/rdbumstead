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
| **☁️ Salesforce** | ![Apex](https://img.shields.io/badge/Apex-00A1E0?style=for-the-badge&logo=salesforce&logoColor=white) ![LWC](https://img.shields.io/badge/LWC-00A1E0?style=for-the-badge&logo=lightning&logoColor=white) ![Agentforce](https://img.shields.io/badge/Agentforce-00A1E0?style=for-the-badge&logo=probot&logoColor=white) ![Flow](https://img.shields.io/badge/Flow_Builder-00A1E0?style=for-the-badge&logo=salesforce&logoColor=white) |
| **⚡ Cloud** | ![AWS Lambda](https://img.shields.io/badge/AWS_Lambda-FF9900?style=for-the-badge&logo=awslambda&logoColor=white) ![Amazon S3](https://img.shields.io/badge/Amazon_S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white) ![Multi-Cloud](https://img.shields.io/badge/Multi_Cloud-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white) |
| **🚀 DevOps** | ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white) ![SFDX](https://img.shields.io/badge/SFDX_CLI-00A1E0?style=for-the-badge&logo=salesforce&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![PMD](https://img.shields.io/badge/PMD_Analysis-green?style=for-the-badge&logo=codacy&logoColor=white) |
| **📐 Architecture** | ![OpenAPI](https://img.shields.io/badge/OpenAPI_3.0-6BA539?style=for-the-badge&logo=openapi-initiative&logoColor=white) ![Event Driven](https://img.shields.io/badge/Event_Driven-B00000?style=for-the-badge&logo=apachekafka&logoColor=white) ![C4 Modeling](https://img.shields.io/badge/C4_Modeling-000000?style=for-the-badge&logo=structurizr&logoColor=white) |

### 📐 System Architecture
*A high-level view of the multi-cloud pattern used in my reference implementation.*

```mermaid
graph LR
    %% Define Styles
    classDef sfdc fill:#00A1E0,stroke:#005FB2,stroke-width:2px,color:white,font-weight:bold;
    classDef aws fill:#FF9900,stroke:#CC7A00,stroke-width:2px,color:white,font-weight:bold;
    classDef jira fill:#0052CC,stroke:#0747A6,stroke-width:2px,color:white,font-weight:bold;
    classDef github fill:#24292F,stroke:#1B1F23,stroke-width:2px,color:white,font-weight:bold;
    classDef user fill:#f9f9f9,stroke:#333,stroke-width:2px,color:black,font-weight:bold;

    %% Nodes
    User((User)) 
    LWR[Experience Cloud LWR]
    SF_GQL[Salesforce GraphQL API]
    DB[(Custom Objects)]
    Lambda[AWS Lambda]
    Apex[Apex Runtime]
    AI[Agentforce Agent]
    Jira[Jira API]
    GitHub[GitHub API]

    %% Relationships
    User --> LWR
    LWR -->|Native GraphQL| SF_GQL
    SF_GQL --> DB
    LWR -->|External Gateway| Lambda
    LWR -->|Runtime| Apex
    Apex <--> AI
    Apex -->|REST| Jira
    Apex -->|REST| GitHub

    %% Apply Styles
    class LWR,SF_GQL,DB,Apex,AI sfdc;
    class Lambda aws;
    class Jira jira;
    class GitHub github;
    class User user;

    %% Global Link Styling for visibility
    linkStyle default stroke-width:2px,fill:none,stroke:lightgray;
```

---

### 📂 Engineering Highlights

#### [Salesforce Platform Architect Porfolio](https://github.com/rdbumstead/salesforce-platform-architect-portfolio)
> *An open-source reference implementation for enterprise delivery patterns.*

* **The Architecture:** Designed a multi-cloud system using Salesforce LWR, GraphQL, Apex, and AWS Lambda.
* **The Governance:** Implemented contract-first APIs (OpenAPI 3.0) and "Chaos Engineering" patterns to validate resilience against third-party failures.
* **The Ops:** Zero-touch CI/CD with automated quality gates.
* **Documentation:** Read my [Architectural Decision Records (ADRs)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/tree/main/docs/adr) to see how I handle security, FinOps, and resilience trade-offs.

#### ["Resume as Code" CI/CD Pipeline](https://github.com/rdbumstead/resume-as-code) &nbsp;&nbsp; [![Build Status](https://github.com/rdbumstead/resume-as-code/actions/workflows/resume-pipeline.yml/badge.svg)](https://github.com/rdbumstead/resume-as-code) [![Import Status](https://github.com/rdbumstead/resume-as-code/actions/workflows/import-resume.yml/badge.svg)](https://github.com/rdbumstead/resume-as-code)
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

Hi, I'm Ryan Bumstead

### Salesforce Platform Architect & Governance Lead
> Governance-first CI/CD design & reference implementation (in active development)

---

### Resumes & Documentation

> [!NOTE]
> PDFs are generated as secure release artifacts to protect PII. Click the badge to download the latest build.*

**Standard Resume**

[![PDF](https://img.shields.io/badge/PDF-Download_Latest_Release-blue?logo=githubactions&logoColor=white)](https://github.com/rdbumstead/resume-as-code/releases/download/latest/RyanBumstead_Resume.pdf) [![Markdown](https://img.shields.io/badge/Markdown-View_Source_Code-black?logo=markdown&logoColor=white)](https://github.com/rdbumstead/resume-as-code/blob/main/markdown/RyanBumstead_Resume.md)

**Platform Engineer Resume**

[![PDF](https://img.shields.io/badge/PDF-Download_Latest_Release-blue?logo=githubactions&logoColor=white)](https://github.com/rdbumstead/resume-as-code/releases/download/latest/RyanBumstead_PlatformEngineer.pdf) [![Markdown](https://img.shields.io/badge/Markdown-View_Source_Code-black?logo=markdown&logoColor=white)](https://github.com/rdbumstead/resume-as-code/blob/main/markdown/RyanBumstead_PlatformEngineer.md)

**Comprehensive Resume** *(Technical Deep Dive)*

[![PDF](https://img.shields.io/badge/PDF-Download_Latest_Release-blue?logo=githubactions&logoColor=white)](https://github.com/rdbumstead/resume-as-code/releases/download/latest/RyanBumstead_Resume_Comprehensive.pdf) [![Markdown](https://img.shields.io/badge/Markdown-View_Source_Code-black?logo=markdown&logoColor=white)](https://github.com/rdbumstead/resume-as-code/blob/main/markdown/RyanBumstead_Resume_Comprehensive.md)

**Connect With Me**  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?logo=linkedin&logoColor=white)](https://linkedin.com/in/ryanbumstead) [![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:ryan@ryanbumstead.com) [![Trailhead](https://img.shields.io/badge/Trailhead-00A1E0?logo=salesforce&logoColor=white)](https://www.salesforce.com/trailblazer/rbumstead)

---

I design Salesforce platforms that balance **developer velocity** with **system integrity**, specializing in **multi-org architecture**, **DevOps governance**, and **governance-first deployment models** for higher education and nonprofit environments.

**Core Focus Areas:**
- Architecture-first delivery
- Governance-driven DevOps  
- Resilient multi-cloud systems (Salesforce + AWS)

### Tech Stack

| Domain | Stack |
| :--- | :--- |
| **Salesforce** | **Apex** · **LWC** · **Agentforce** · **Flow Builder** |
| **Cloud** | **AWS Lambda** · **S3** · **Multi-Cloud Architecture** |
| **DevOps** | **Reusable Workflows** · **GitHub Actions** · **SFDX CLI** · **Docker** |
| **Architecture** | **OpenAPI 3.0** · **Event-Driven** · **Secure by Design** |
| **Languages & Tools** | **Go** · **Python** · **TypeScript** · **JavaScript** · **YAML** · **Pandoc** · **XeLaTeX** · **Mermaid.js** |

### System Architecture
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

    subgraph Roadmap ["Future Roadmap (Phase 2)"]
        Lambda[AWS Lambda<br/>Offload Compute]
    end

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

### Engineering Highlights

#### [GlassOps Governance Protocol](https://github.com/glassops-platform/glassops)

[![Status](https://img.shields.io/badge/Status-v1.0--alpha_%28Active_Protocol%29-blue)](https://github.com/glassops-platform/glassops/blob/main/docs/architecture.md)

> An Open Source (Apache 2.0) Standard for Salesforce DevOps that separates policy enforcement from execution.

> [!TIP]
> **Check out the [Overview](https://github.com/glassops-platform/glassops/blob/main/docs/architecture/overview.md)!**

- **Governance Control Plane:** Designed a system intended to enforce deployment outcomes independently of tooling.
- **Policy & Contract Model:** Defined a model that normalizes results across execution engines such as native sf CLI and sfdx-hardis.
- **Pluggable Adapter Pattern:** Architected a pattern allowing teams to swap execution engines without breaking compliance guarantees.
- **Deployment Governance:** Formalized concepts including policy resolution, validation gates, and pass or fail arbitration.
- **Tooling Strategy:** Positioned mature tools like sfdx-hardis as **first-class execution adapters**, not competitors.
- **System Documentation:** Authored protocol-level architecture documentation treating governance as a system concern rather than a pipeline feature.

#### [GlassOps Runtime](https://github.com/glassops-platform/glassops-runtime)

[![Verify Primitives](https://github.com/glassops-platform/glassops-runtime/actions/workflows/verify-primitives.yml/badge.svg)](https://github.com/glassops-platform/glassops-runtime/actions/workflows/verify-primitives.yml)
[![Integration Tests](https://github.com/glassops-platform/glassops-runtime/actions/workflows/integration-tests.yml/badge.svg)](https://github.com/glassops-platform/glassops-runtime/actions/workflows/integration-tests.yml)
[![Verify Governance](https://github.com/glassops-platform/glassops-runtime/actions/workflows/verify-governance.yml/badge.svg)](https://github.com/glassops-platform/glassops-runtime/actions/workflows/verify-governance.yml)
[![Plugin Whitelist Tests](https://github.com/glassops-platform/glassops-runtime/actions/workflows/plugin-whitelist-test.yml/badge.svg)](https://github.com/glassops-platform/glassops-runtime/actions/workflows/plugin-whitelist-test.yml)
[![Verify Auth Contract](https://github.com/glassops-platform/glassops-runtime/actions/workflows/verify-auth-contract.yml/badge.svg)](https://github.com/glassops-platform/glassops-runtime/actions/workflows/verify-auth-contract.yml)

> *Production-grade execution infrastructure designed to provide the foundational layer for GlassOps governance.*

- **Verified Primitives:** Engineered comprehensive test coverage ensuring consistent behavior across execution contexts.
- **Governed Authentication:** Implemented authentication contracts supporting JWT, OAuth, and SFDX Auth URL patterns.
- **Plugin Security:** Designed whitelist enforcement preventing unauthorized Salesforce CLI extensions.
- **Governed Execution:** Enforces strict timeouts, validates inputs, and provides structured error handling with clear failure modes.
- **Infrastructure Guarantees:** Established the foundational layer ensuring deployment outcomes are reproducible and auditable.

> [!NOTE]
> **Powers the GlassOps Governance Protocol execution layer.** Governance guarantees require infrastructure guarantees.

#### [Salesforce Platform Architect Portfolio](https://github.com/rdbumstead/salesforce-platform-architect-portfolio)
[![CI/CD — main](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy.yml/badge.svg?branch=main)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy.yml) [![PR Validation](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/pr.yml/badge.svg)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/pr.yml) [![Cloudflare Worker](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy-worker.yml/badge.svg)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/deploy-worker.yml) [![Daily Org Heartbeat](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/keep-alive.yml/badge.svg)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/actions/workflows/keep-alive.yml)

> *An open-source reference implementation for enterprise delivery patterns.*

> [!TIP]
> **View the full documentation in the [Governance Hub](https://rdbumstead.github.io/salesforce-platform-architect-portfolio/) for the best reading experience.**

* **The Architecture:** Designed a multi-cloud system using Salesforce LWR, GraphQL, Apex, and AWS Lambda.
* **The Governance:** Architected contract-first APIs (OpenAPI 3.0) and "Chaos Engineering" patterns to validate resilience against third-party failures.
* **The Ops:** Zero-touch CI/CD with automated quality gates.
* **Documentation:** Read my [Architectural Decision Records (ADRs)](https://github.com/rdbumstead/salesforce-platform-architect-portfolio/tree/main/docs/adr) to see how I handle security, FinOps, and resilience trade-offs.

#### [Setup Salesforce CLI Action](https://github.com/rdbumstead/setup-salesforce-action)
[![GitHub Marketplace](https://img.shields.io/badge/Marketplace-Setup%20Salesforce%20CLI-blue.svg)](https://github.com/marketplace/actions/setup-salesforce-cli)
[![GitHub release](https://img.shields.io/github/v/release/rdbumstead/setup-salesforce-action)](https://github.com/rdbumstead/setup-salesforce-action/releases)
[![Critical Tests](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test-critical.yml/badge.svg)](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test-critical.yml)
[![Plugin Tests](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test-plugins.yml/badge.svg)](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test-plugins.yml)
[![Authentication Tests](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test-auth.yml/badge.svg)](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test-auth.yml)
[![Cross Platform Tests](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test-cross-platform.yml/badge.svg)](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test-cross-platform.yml) [![Invariants Tests](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test-invariants.yml/badge.svg)](https://github.com/rdbumstead/setup-salesforce-action/actions/workflows/test-invariants.yml)

> *A production-ready GitHub Action for Salesforce CI/CD pipelines.*

* **Self-Healing Architecture:** Engineered exponential backoff logic for high availability and fault tolerance.
* **Strict-Mode Governance:** Implemented automated quality gates to enforce enterprise coding standards.
* **Cross-Platform Design:** Built the foundation for modular reusable workflows supporting Linux and Windows.
* **Performance:** Intelligent caching strategy reducing setup time by **80%** (20s vs 2m).

#### ["Resume as Code" CI/CD Pipeline](https://github.com/rdbumstead/resume-as-code)
[![Build Status](https://github.com/rdbumstead/resume-as-code/actions/workflows/resume-pipeline.yml/badge.svg)](https://github.com/rdbumstead/resume-as-code)
![Font Test Status](https://github.com/rdbumstead/resume-as-code/actions/workflows/test-font-install.yml/badge.svg)
> *Treating professional career documentation as a software product.*

* **Security-First Architecture:** Engineered custom Node.js assembly engine that dynamically injects job titles ("Golden Headers") and PII at runtime using GitHub Secrets.
* **Governance Pipeline:** Automated validation for formatting standards and hyperlink integrity before compilation.
* **High-Fidelity Compilation:** Orchestrated PDF generation using Pandoc and XeLaTeX for pixel-perfect rendering.
* **Decoupled Architecture:** Separated public source code (Markdown) from private contact information in compiled artifacts.

### Certifications
* Salesforce Certified Agentforce Specialist
* Salesforce Certified Data Cloud Consultant
* Salesforce Certified Education Cloud Consultant
* Salesforce Certified Platform App Builder
* Salesforce Certified Platform Administrator I & II

[Verify these credentials on Trailhead ↗](https://www.salesforce.com/trailblazer/rbumstead)

---

**I help organizations evolve from "fragile features" to resilient, governed ecosystems.**

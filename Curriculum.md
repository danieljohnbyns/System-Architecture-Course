# System Architecture Curriculum


## Table of Contents
- [System Architecture Curriculum](#system-architecture-curriculum)
  - [Table of Contents](#table-of-contents)
  - [Phase 1: Foundation](#phase-1-foundation)
    - [1.1 Technical Core](#11-technical-core)
      - [1.1.1 Proficiency in 1-2 OOP/Systems Languages](#111-proficiency-in-1-2-oopsystems-languages)
      - [1.1.2 Data Structures \& Algorithms](#112-data-structures--algorithms)
      - [1.1.3 Development Tool Proficiency](#113-development-tool-proficiency)
    - [1.2 System Basics](#12-system-basics)
      - [1.2.1 Operating Systems Fundamentals](#121-operating-systems-fundamentals)
      - [1.2.2 Basic Networking](#122-basic-networking)
      - [1.2.3 Databases Fundamentals](#123-databases-fundamentals)
  - [Phase 2: Architecture Apprentice](#phase-2-architecture-apprentice)
    - [2.1 Design \& Architecture](#21-design--architecture)
      - [2.1.1 Design Principles \& Patterns](#211-design-principles--patterns)
      - [2.1.2 Architectural Patterns](#212-architectural-patterns)
      - [2.1.3 API Design \& Integration](#213-api-design--integration)
      - [2.1.4 Distributed Systems Theory](#214-distributed-systems-theory)
    - [2.2 Platform \& DevOps](#22-platform--devops)
      - [2.2.1 Cloud Computing Core](#221-cloud-computing-core)
      - [2.2.2 Containerization \& Orchestration](#222-containerization--orchestration)
      - [2.2.3 CI/CD \& IaC](#223-cicd--iac)
    - [2.3 Quality \& Analysis](#23-quality--analysis)
      - [2.3.1 System Modeling \& Design Documents](#231-system-modeling--design-documents)
      - [2.3.2 Non-Functional Requirements (NFRs) \& Resiliency](#232-non-functional-requirements-nfrs--resiliency)
  - [Phase 3: Strategic Architect](#phase-3-strategic-architect)
    - [3.1 Enterprise Strategy](#31-enterprise-strategy)
      - [3.1.1 Enterprise Architecture](#311-enterprise-architecture)
      - [3.1.2 Risk, Security \& Compliance](#312-risk-security--compliance)
      - [3.1.3 Cost Optimization \& Budgeting](#313-cost-optimization--budgeting)
    - [3.2 Leadership \& Soft Skills](#32-leadership--soft-skills)
      - [3.2.1 Stakeholder Communication](#321-stakeholder-communication)
      - [3.2.2 Technical Leadership \& Mentoring](#322-technical-leadership--mentoring)
      - [3.2.3 Architecture Decision Records](#323-architecture-decision-records)
  - [Capstone Project](#capstone-project)
    - [Objective](#objective)
    - [Project Structure](#project-structure)
      - [Step 1: Project Scoping \& Proposal](#step-1-project-scoping--proposal)
      - [Step 2: Comprehensive Architecture Design](#step-2-comprehensive-architecture-design)
      - [Step 3: Strategic \& Business Integration](#step-3-strategic--business-integration)
    - [Example Projects Across Domains](#example-projects-across-domains)
    - [Final Assessment \& Review](#final-assessment--review)

---

## Phase 1: Foundation
Build the bedrock of technical knowledge to understand how systems work.

### 1.1 Technical Core
**Duration**: 6 weeks

**Learning Objective**: Transition from writing code to engineering robust, efficient software components.

#### 1.1.1 Proficiency in 1-2 OOP/Systems Languages
  * **Core Concepts**: Deep understanding of one primary language (Java, C#, or Go), including memory management, concurrency models, and idiomatic design.
  * **Practical Output**: Refactor a procedural script into a well-structured OOP application with proper interfaces and error handling.

#### 1.1.2 Data Structures & Algorithms
  * **Core Concepts**: Analysis of time/space complexity; mastery of trees, graphs, hash tables, and their real-world application in system design (e.g., indexes, routing).
  * **Practical Output**: Solve 75+ LeetCode problems (focus: Medium). Implement a feature that requires a non-trivial data structure (e.g., LRU cache, trie for autocomplete).

#### 1.1.3 Development Tool Proficiency
  * **Core Concepts**: Advanced Git (rebasing, bisecting); Linux command-line mastery; scripting for automation (Bash/Python).
  * **Practical Output**: Automate a local dev environment setup with scripts. Contribute to an open-source project via a well-structured fork, branch, and pull request.

### 1.2 System Basics
**Duration**: 6 weeks

**Learning Objective**: Comprehend the environment in which software runs, from the OS to the network.

#### 1.2.1 Operating Systems Fundamentals
  * **Core Concepts**: Processes vs. threads, scheduling, virtual memory, I/O, and interrupts.
  * **Practical Output**: Write a multi-threaded program that demonstrates a race condition and fix it with synchronization primitives.

#### 1.2.2 Basic Networking
  * **Core Concepts**: OSI/TCP-IP models, TCP vs UDP, HTTP/1.1/2/3, TLS handshake, DNS resolution, and load balancing basics.
  * **Practical Output**: Use Wireshark to capture and analyze a TCP handshake and HTTP request. Diagram the complete flow of a user typing a URL to a page loading.

#### 1.2.3 Databases Fundamentals
  * **Core Concepts**: Relational design (normalization, ACID), SQL proficiency (joins, subqueries, transactions), NoSQL paradigms (document, key-value, wide-column).
  * **Practical Output**: Design a normalized schema for a given domain. Benchmark and compare simple operations in SQL vs. NoSQL databases.

---

## Phase 2: Architecture Apprentice
Learn to design, integrate, and deploy complex systems.

### 2.1 Design & Architecture
**Duration**: 8 weeks

**Learning Objective**: Apply patterns and principles to design cohesive, maintainable systems.

#### 2.1.1 Design Principles & Patterns
  * **Core Concepts**: SOLID, DRY, YAGNI, composition over inheritance; Gang of Four patterns (Factory, Observer, Strategy).
  * **Practical Output**: Identify pattern violations in legacy code and refactor. Justify the use of specific patterns in a new design.

#### 2.1.2 Architectural Patterns
  * **Core Concepts**: Monoliths, Microservices, Event-Driven Architecture, Service-Oriented Architecture (SOA), Serverless. Trade-offs in coupling, cohesion, and complexity.
  * **Practical Output**: Create a detailed comparison report for migrating a hypothetical monolith to microservices, covering pros, cons, and decomposition strategies.

#### 2.1.3 API Design & Integration
  * **Core Concepts**: RESTful principles, gRPC/protobuf, GraphQL schemas, messaging (Kafka, RabbitMQ), idempotency, and versioning strategies.
  * **Practical Output**: Design a REST API with an OpenAPI spec and a gRPC service for the same domain. Implement a simple event-driven workflow using a message queue.

#### 2.1.4 Distributed Systems Theory
  * **Core Concepts**: The CAP and PACELC theorems and their implications for database and service design. The 8 Fallacies of Distributed Computing (e.g., "The network is reliable," "Latency is zero"). Understanding eventual vs. strong consistency.
  * **Practical Output**: For a given system (e.g., a global shopping cart), analyze and document the consistency/availability trade-off (CAP) you would choose and justify it. Diagram a scenario where a network partition would break a naive application design.

### 2.2 Platform & DevOps
**Duration**: 8 weeks

**Learning Objective**: Build and operate systems reliably in cloud environments.

#### 2.2.1 Cloud Computing Core
  * **Core Concepts**: IaaS vs. PaaS vs. SaaS, cloud economics, core services (compute, storage, networking, IAM) on AWS, Azure, or GCP.
  * **Practical Output**: Deploy a highly available 3-tier web application (frontend, backend, database) using cloud provider console and CLI. Implement a VPC with public/private subnets.

#### 2.2.2 Containerization & Orchestration
  * **Core Concepts**: Docker images, layers, networking; Kubernetes pods, services, deployments, ingress controllers, and ConfigMaps.
  * **Practical Output**: "Dockerize" a multi-service application. Deploy it to a local Kubernetes cluster (minikube/kind) and then to a managed cloud service (EKS/AKS/GKE).

#### 2.2.3 CI/CD & IaC
  * **Core Concepts**: Pipeline stages (build, test, security scan, deploy); GitOps principles, declarative infrastructure (Terraform, CloudFormation).
  * **Practical Output**: Create a CI/CD pipeline for your application using GitHub Actions or GitLab CI. Define the cloud infrastructure for the app using Terraform.

### 2.3 Quality & Analysis
**Duration**: 4 weeks

**Learning Objective**: Systematically model systems and guarantee they meet quality requirements.

#### 2.3.1 System Modeling & Design Documents
  * **Core Concepts**: The C4 Model for visualization, UML sequence and component diagrams, writing effective Architecture Decision Records (ADRs).
  * **Practical Output**: Create a complete C4 model (Context, Containers, Components, Code) for a system like a video streaming service. Write an ADR for a major technology choice within it.

#### 2.3.2 Non-Functional Requirements (NFRs) & Resiliency
  * **Core Concepts**:
    * **Core NFRs**: Scalability (horizontal/vertical), reliability (MTTF, MTTR, SLAs/SLOs/SLIs), performance.
    * **Resiliency Patterns**: Circuit Breaker, Retries with Backoff & Jitter, Bulkheads, Backpressure. Understand when and how to apply each.
    * **Observability Pillars**: Logging, Metrics, and Distributed Tracing. Implementing end-to-end trace propagation with tools like OpenTelemetry and Jaeger.
  * **Practical Output**:
    * Design a fault-tolerant service integration that uses a Circuit Breaker and retry logic. Simulate a downstream failure and observe the system's behavior.
    * Instrument a simple microservice application to emit metrics and distributed traces. Use the traces to visualize a request flow across services.

---

## Phase 3: Strategic Architect
Evolve from technical design to strategic leadership and enterprise impact.

### 3.1 Enterprise Strategy
**Duration**: 8 weeks

**Learning Objective**: Align technology strategy with business goals, manage risk, and optimize costs.

#### 3.1.1 Enterprise Architecture
  * **Core Concepts**: Business-IT alignment, EA frameworks (TOGAF ADM), capability mapping, technology portfolio management, and governance models.
  * **Practical Output**: Develop a simplified future-state architecture roadmap for a small business, linking technology initiatives to business capabilities.

#### 3.1.2 Risk, Security & Compliance
  * **Core Concepts**: Security-by-design, threat modeling (STRIDE), risk assessment frameworks, data privacy regulations (GDPR, CCPA), and industry standards (ISO 27001, SOC 2).
  * **Practical Output**: Conduct a threat modeling session for one of your previous designs. Draft a compliance checklist for a hypothetical application handling user data.

#### 3.1.3 Cost Optimization & Budgeting
  * **Core Concepts**: Cloud cost models (CAPEX vs. OPEX), TCO analysis, right-sizing, reserved vs. spot instances, tagging strategies, and FinOps principles.
  * **Practical Output**: Analyze the cloud bill of a sample architecture. Propose and justify specific cost-saving changes, estimating the potential savings.

### 3.2 Leadership & Soft Skills
**Duration**: 6 weeks

**Learning Objective**: Communicate effectively, lead technical teams, and make durable decisions.

#### 3.2.1 Stakeholder Communication
  * **Core Concepts**: Tailoring messages for executives, engineers, and business partners; creating effective presentations and whitepapers; facilitating architecture review boards.
  * **Practical Output**: Prepare and deliver a 10-minute presentation to a "mock executive team" advocating for a significant technology investment.

#### 3.2.2 Technical Leadership & Mentoring
  * **Core Concepts**: Leading without authority, running effective design reviews, mentoring junior architects, building consensus, and managing technical debt.
  * **Practical Output**: Facilitate a design review for a peer's project. Create a 30/60/90-day learning plan for a junior engineer transitioning into architecture.

#### 3.2.3 Architecture Decision Records
  * **Core Concepts**: Formalizing the ADR process, decision log maintenance, communicating and socializing decisions, and reviewing past decisions.
  * **Practical Output**: Establish a lightweight ADR process for your personal or team projects. Maintain a decision log for the major choices in your capstone project.

---

## Capstone Project

### Objective
Synthesize the learning from all three phases. **You will architect a system for a domain of your choice**, demonstrating mastery of technical design, strategic planning, and communication skills.

### Project Structure

#### Step 1: Project Scoping & Proposal
  * **Task**: Choose a domain relevant to your interests or professional goals (e.g., e-commerce platform, IoT system, real-time analytics pipeline).
  * **Deliverable**: A one-page project charter.
    * Define the **core business problem**.
    * List key **functional requirements** (what the system does) and **non-functional requirements** (scale, reliability, security).
    * Identify the primary **stakeholders** (e.g., end-users, operators, business owners).

#### Step 2: Comprehensive Architecture Design
  * **Task**: Create the complete architectural specification for your chosen system.
  * **Deliverables**:
    * **C4 Model Diagrams**: A full set (Context, Containers, Components) visually defining the system's structure and interactions.
    * **Architecture Decision Record (ADR) Log**: At least 5 ADRs documenting critical technology choices. At least one ADR must explicitly address a distributed systems trade-off (e.g., CAP/PACELC implications of a chosen database).
    * **API Contract Specifications**: Detailed OpenAPI/Swagger specs for major services or a gRPC protocol definition.
    * **Data Model**: Logical and physical database schemas.
    * **Non-Functional Requirement (NFR) & Resiliency Plan**: Explicit SLOs/SLIs. A description of how scalability, reliability, and security will be achieved, including the specific resiliency patterns (e.g., Circuit Breaker, Backpressure) and observability strategy (e.g., tracing with OpenTelemetry) to be employed.

#### Step 3: Strategic & Business Integration
  * **Task**: Develop the business and operational context for your technical design.
  * **Deliverables**:
    * **Phased Implementation Roadmap**: A 3-phase plan (e.g., MVP, Scale, Optimize) with milestones and deliverables.
    * **Cost-Benefit Analysis & Budget Forecast**: A high-level TCO for the first year, identifying major cost drivers and potential optimizations.
    * **Risk Register & Mitigation Plan**: A table listing technical, security, and operational risks with proposed mitigation strategies.
    * **Stakeholder Communication Package**: A 5-slide executive summary presentation pitching the architecture and its business value.

### Example Projects Across Domains
  * **Healthcare**: Design a **HIPAA-compliant patient data lake** for clinical research, focusing on data anonymization, secure access, and batch/stream processing.
  * **IoT/Manufacturing**: Design a **predictive maintenance platform** for industrial equipment, focusing on real-time telemetry ingestion, time-series analysis, and alerting.
  * **Finance**: Design a **core banking ledger system**, focusing on transaction integrity, audit trails, and regulatory reporting.

### Final Assessment & Review
  * **Compile a Final Portfolio**: Assemble all deliverables from Steps 1-3 into a single, professionally formatted document.
  * **Present and Defend**: Present your architecture to a **review board** (peers, mentor, online community) in a 20-minute session, followed by a 10-minute Q&A. Justify your decisions and explain trade-offs.
  * **Success Criteria**:
    1.  **Technical Depth**: Design logically addresses all requirements with appropriate patterns and technologies.
    2.  **Holistic Thinking**: Clearly connects technical choices to business goals, cost, risk, and operational reality.
    3.  **Clarity & Communication**: Documentation is clear, diagrams are effective, and the executive summary is compelling to a non-technical audience.

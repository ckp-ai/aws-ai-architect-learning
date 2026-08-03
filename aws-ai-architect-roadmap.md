# AWS AI Architect Learning Roadmap

**Target learner:** Senior AWS Cloud Architect
**Target outcome:** Transition from experienced AWS Cloud/Data Architect to enterprise-grade AWS AI Architect  
**Suggested duration:** 20–24 weeks  
**Suggested commitment:** 8–10 hours per week  

---

## 1. Purpose

This learning repository is designed for an experienced AWS architect who does not need to repeat cloud, data platform, Kubernetes, networking, IAM, or infrastructure fundamentals.

The roadmap focuses strictly on the capabilities required to design and govern:

- Traditional machine learning solutions on AWS
- Generative AI applications using Amazon Bedrock
- Enterprise Retrieval-Augmented Generation platforms
- Vector-search architectures
- Agentic AI systems
- Amazon Bedrock AgentCore platforms
- MLOps and LLMOps capabilities
- AI security and Responsible AI controls
- Enterprise AI landing zones and shared AI platforms
- Production-grade AI architecture, operations, and governance

The intended transition is:

```text
AWS Cloud/Data Platform Architect
                |
                v
AI and ML Architecture Fundamentals
                |
                v
Amazon SageMaker and Production ML
                |
                v
Amazon Bedrock and Generative AI
                |
                v
Enterprise RAG and Vector Search
                |
                v
Agentic AI and Bedrock AgentCore
                |
                v
AI Security, Governance, and Responsible AI
                |
                v
MLOps, LLMOps, and AI Platform Engineering
                |
                v
Enterprise AWS AI Architect
```

---

## 2. Recommended Git Repository Structure

```text
aws-ai-architect-roadmap/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CHANGELOG.md
├── Makefile
├── pyproject.toml
├── requirements/
│   ├── base.txt
│   ├── development.txt
│   ├── ml.txt
│   ├── genai.txt
│   └── agents.txt
├── .gitignore
├── .editorconfig
├── .pre-commit-config.yaml
├── .github/
│   ├── workflows/
│   │   ├── markdown-lint.yml
│   │   ├── python-test.yml
│   │   ├── terraform-validate.yml
│   │   ├── security-scan.yml
│   │   └── evaluation-gates.yml
│   ├── ISSUE_TEMPLATE/
│   │   ├── study-task.md
│   │   ├── architecture-decision.md
│   │   └── lab-defect.md
│   └── pull_request_template.md
│
├── 00-program-governance/
│   ├── README.md
│   ├── learning-objectives.md
│   ├── baseline-assessment.md
│   ├── study-calendar.md
│   ├── progress-tracker.md
│   ├── skills-matrix.md
│   ├── definition-of-done.md
│   └── evidence-register.md
│
├── 01-ai-ml-architecture-foundations/
│   ├── README.md
│   ├── study-notes/
│   │   ├── ml-lifecycle.md
│   │   ├── model-evaluation.md
│   │   ├── inference-patterns.md
│   │   ├── embeddings-transformers-llms.md
│   │   └── ai-use-case-selection.md
│   ├── labs/
│   │   └── simple-classification/
│   ├── architecture/
│   │   ├── diagrams/
│   │   └── decisions/
│   ├── assessments/
│   │   ├── knowledge-check.md
│   │   └── architecture-review.md
│   └── resources.md
│
├── 02-sagemaker-production-ml/
│   ├── README.md
│   ├── study-notes/
│   │   ├── sagemaker-capabilities.md
│   │   ├── training-and-processing.md
│   │   ├── model-registry.md
│   │   ├── feature-store.md
│   │   ├── inference-options.md
│   │   ├── model-monitoring.md
│   │   └── bedrock-vs-sagemaker.md
│   ├── labs/
│   │   ├── training-pipeline/
│   │   ├── model-registry/
│   │   ├── realtime-inference/
│   │   ├── batch-inference/
│   │   └── model-monitoring/
│   ├── infrastructure/
│   │   ├── terraform/
│   │   └── iam/
│   ├── architecture/
│   │   ├── diagrams/
│   │   ├── decisions/
│   │   ├── cost-model/
│   │   └── runbooks/
│   ├── evaluations/
│   └── resources.md
│
├── 03-amazon-bedrock-genai/
│   ├── README.md
│   ├── study-notes/
│   │   ├── foundation-models.md
│   │   ├── model-selection.md
│   │   ├── converse-api.md
│   │   ├── prompt-engineering.md
│   │   ├── context-engineering.md
│   │   ├── structured-output.md
│   │   ├── guardrails-overview.md
│   │   └── token-cost-and-latency.md
│   ├── prompts/
│   │   ├── system/
│   │   ├── few-shot/
│   │   ├── structured-output/
│   │   ├── safety/
│   │   └── prompt-catalog.yaml
│   ├── labs/
│   │   ├── basic-model-invocation/
│   │   ├── converse-api/
│   │   ├── response-streaming/
│   │   ├── structured-json/
│   │   ├── prompt-management/
│   │   ├── model-routing/
│   │   └── guardrails/
│   ├── applications/
│   │   └── secure-enterprise-chat/
│   ├── infrastructure/
│   │   ├── terraform/
│   │   └── iam/
│   ├── evaluations/
│   │   ├── prompt-tests/
│   │   ├── model-comparison/
│   │   └── regression-suite/
│   ├── architecture/
│   │   ├── diagrams/
│   │   ├── decisions/
│   │   ├── threat-models/
│   │   ├── cost-model/
│   │   └── runbooks/
│   └── resources.md
│
├── 04-enterprise-rag/
│   ├── README.md
│   ├── study-notes/
│   │   ├── rag-reference-architecture.md
│   │   ├── document-ingestion.md
│   │   ├── chunking-strategies.md
│   │   ├── embeddings.md
│   │   ├── vector-search.md
│   │   ├── hybrid-search.md
│   │   ├── reranking.md
│   │   ├── metadata-design.md
│   │   ├── authorization-aware-retrieval.md
│   │   └── rag-evaluation.md
│   ├── labs/
│   │   ├── custom-ingestion/
│   │   ├── bedrock-knowledge-bases/
│   │   ├── opensearch-vector/
│   │   ├── aurora-pgvector/
│   │   ├── hybrid-search/
│   │   ├── reranking/
│   │   └── document-level-security/
│   ├── data/
│   │   ├── sample-documents/
│   │   ├── metadata/
│   │   └── evaluation-datasets/
│   ├── applications/
│   │   └── secure-document-assistant/
│   ├── infrastructure/
│   │   ├── terraform/
│   │   └── iam/
│   ├── evaluations/
│   │   ├── retrieval/
│   │   ├── generation/
│   │   ├── citations/
│   │   └── security/
│   ├── architecture/
│   │   ├── diagrams/
│   │   ├── decisions/
│   │   ├── threat-models/
│   │   ├── cost-model/
│   │   └── runbooks/
│   └── resources.md
│
├── 05-agentic-ai-agentcore/
│   ├── README.md
│   ├── study-notes/
│   │   ├── agent-fundamentals.md
│   │   ├── workflow-vs-agent.md
│   │   ├── tool-use.md
│   │   ├── state-and-memory.md
│   │   ├── human-in-the-loop.md
│   │   ├── multi-agent-patterns.md
│   │   ├── mcp.md
│   │   ├── bedrock-agents.md
│   │   └── agentcore.md
│   ├── frameworks/
│   │   ├── strands/
│   │   ├── langgraph/
│   │   └── comparison.md
│   ├── tools/
│   │   ├── tool-catalog.yaml
│   │   ├── schemas/
│   │   ├── lambda-tools/
│   │   └── mcp-servers/
│   ├── labs/
│   │   ├── single-agent/
│   │   ├── tool-calling/
│   │   ├── knowledge-enabled-agent/
│   │   ├── human-approval/
│   │   ├── step-functions-hybrid/
│   │   ├── memory/
│   │   └── multi-agent/
│   ├── applications/
│   │   └── cloud-operations-agent/
│   ├── policies/
│   │   ├── tool-allowlist.yaml
│   │   ├── execution-limits.yaml
│   │   ├── approval-policy.yaml
│   │   └── memory-policy.yaml
│   ├── evaluations/
│   │   ├── task-completion/
│   │   ├── tool-selection/
│   │   ├── safety/
│   │   └── trace-analysis/
│   ├── architecture/
│   │   ├── diagrams/
│   │   ├── decisions/
│   │   ├── threat-models/
│   │   ├── cost-model/
│   │   └── runbooks/
│   └── resources.md
│
├── 06-ai-security-responsible-ai/
│   ├── README.md
│   ├── study-notes/
│   │   ├── ai-threat-landscape.md
│   │   ├── prompt-injection.md
│   │   ├── data-leakage.md
│   │   ├── retrieval-poisoning.md
│   │   ├── tool-poisoning.md
│   │   ├── excessive-agency.md
│   │   ├── denial-of-wallet.md
│   │   ├── tenant-isolation.md
│   │   └── responsible-ai-principles.md
│   ├── controls/
│   │   ├── iam/
│   │   ├── scp/
│   │   ├── kms/
│   │   ├── network/
│   │   ├── guardrails/
│   │   ├── data-perimeters/
│   │   └── logging/
│   ├── governance/
│   │   ├── use-case-intake.md
│   │   ├── risk-classification.md
│   │   ├── model-approval.md
│   │   ├── release-criteria.md
│   │   ├── human-oversight.md
│   │   ├── incident-management.md
│   │   └── decommissioning.md
│   ├── threat-models/
│   │   ├── rag-threat-model.md
│   │   ├── agent-threat-model.md
│   │   └── ai-platform-threat-model.md
│   ├── red-team/
│   │   ├── attack-catalog.md
│   │   ├── test-cases/
│   │   └── results/
│   ├── assessments/
│   │   ├── responsible-ai-assessment-template.md
│   │   └── security-review-checklist.md
│   └── resources.md
│
├── 07-mlops-llmops/
│   ├── README.md
│   ├── study-notes/
│   │   ├── mlops.md
│   │   ├── llmops.md
│   │   ├── prompt-versioning.md
│   │   ├── model-versioning.md
│   │   ├── knowledge-base-versioning.md
│   │   ├── continuous-evaluation.md
│   │   ├── deployment-strategies.md
│   │   └── rollback-strategies.md
│   ├── pipelines/
│   │   ├── model-ci-cd/
│   │   ├── prompt-ci-cd/
│   │   ├── rag-ci-cd/
│   │   └── agent-ci-cd/
│   ├── evaluation-framework/
│   │   ├── datasets/
│   │   ├── metrics/
│   │   ├── thresholds/
│   │   ├── test-runners/
│   │   └── reports/
│   ├── observability/
│   │   ├── metrics-catalog.md
│   │   ├── dashboards/
│   │   ├── tracing/
│   │   └── alerts/
│   ├── cost-management/
│   │   ├── token-cost-model.md
│   │   ├── cost-allocation.md
│   │   ├── budgets.md
│   │   └── optimization.md
│   ├── infrastructure/
│   │   ├── terraform/
│   │   └── github-actions/
│   └── resources.md
│
├── 08-enterprise-ai-platform/
│   ├── README.md
│   ├── architecture/
│   │   ├── business-context/
│   │   ├── logical/
│   │   ├── deployment/
│   │   ├── network/
│   │   ├── security/
│   │   ├── data-flow/
│   │   ├── operations/
│   │   └── disaster-recovery/
│   ├── landing-zone-extension/
│   │   ├── organization-design.md
│   │   ├── account-model.md
│   │   ├── ou-design.md
│   │   ├── scp-strategy.md
│   │   ├── model-access-governance.md
│   │   └── region-governance.md
│   ├── platform-services/
│   │   ├── model-gateway/
│   │   ├── prompt-catalog/
│   │   ├── guardrail-service/
│   │   ├── knowledge-service/
│   │   ├── vector-service/
│   │   ├── agent-runtime/
│   │   ├── tool-gateway/
│   │   ├── evaluation-service/
│   │   └── observability-service/
│   ├── tenancy/
│   │   ├── isolation-model.md
│   │   ├── onboarding.md
│   │   ├── quotas.md
│   │   └── chargeback.md
│   ├── architecture-decisions/
│   ├── controls/
│   ├── operating-model/
│   ├── service-catalog/
│   ├── cost-model/
│   └── runbooks/
│
├── 09-solution-shaping/
│   ├── README.md
│   ├── use-case-assessment/
│   │   ├── intake-template.md
│   │   ├── prioritization-scorecard.md
│   │   └── ai-vs-non-ai-decision-tree.md
│   ├── discovery/
│   │   ├── stakeholder-questions.md
│   │   ├── data-readiness.md
│   │   └── risk-discovery.md
│   ├── architecture-templates/
│   │   ├── solution-overview.md
│   │   ├── non-functional-requirements.md
│   │   ├── security-view.md
│   │   ├── evaluation-plan.md
│   │   ├── cost-model.md
│   │   └── delivery-roadmap.md
│   ├── business-case/
│   │   ├── value-hypothesis.md
│   │   ├── benefits-model.md
│   │   ├── tco-template.md
│   │   └── executive-presentation-outline.md
│   └── interview-preparation/
│       ├── architecture-questions.md
│       ├── scenario-questions.md
│       └── whiteboard-exercises.md
│
├── 10-portfolio/
│   ├── README.md
│   ├── 01-enterprise-ai-landing-zone/
│   ├── 02-secure-multitenant-rag/
│   ├── 03-agentic-cloud-operations/
│   └── portfolio-evidence-index.md
│
├── shared/
│   ├── architecture/
│   │   ├── diagram-standards.md
│   │   ├── c4-templates/
│   │   ├── mermaid/
│   │   └── icons/
│   ├── adr/
│   │   ├── ADR-TEMPLATE.md
│   │   └── adr-index.md
│   ├── policies/
│   ├── schemas/
│   ├── test-data/
│   ├── scripts/
│   ├── terraform-modules/
│   └── glossary.md
│
└── docs/
    ├── roadmap.md
    ├── study-map.md
    ├── competency-model.md
    ├── architecture-principles.md
    ├── certification-path.md
    └── resource-catalog.md
```

---

## 3. Repository Design Principles

### 3.1 Treat the repository as an architecture portfolio

The repository should demonstrate more than course completion. It should provide evidence that the learner can:

- Translate business requirements into AI architectures
- Select the correct AWS AI service
- Defend architecture decisions
- Build secure prototypes
- Define evaluation criteria
- Design operating models
- Estimate cost
- Create production runbooks
- Govern AI workloads within an AWS landing zone

### 3.2 Keep study notes separate from implementation

Each learning phase should contain:

```text
study-notes/     Concepts and summaries
labs/            Small focused implementations
applications/    Integrated working solutions
architecture/    Diagrams, ADRs, cost models, and runbooks
evaluations/     Quality, security, and regression tests
resources.md     Curated learning references
```

### 3.3 Every major project should include evidence

A complete architecture-grade project should contain:

```text
project/
├── README.md
├── requirements/
├── architecture/
│   ├── business-context.md
│   ├── logical-architecture.md
│   ├── deployment-architecture.md
│   ├── data-flow.md
│   ├── security-architecture.md
│   ├── operations-architecture.md
│   └── diagrams/
├── decisions/
├── threat-model/
├── application/
├── infrastructure/
├── prompts/
├── tools/
├── evaluations/
├── tests/
├── dashboards/
├── cost-model/
├── runbooks/
└── evidence.md
```

### 3.4 Use traceable identifiers

Use consistent identifiers throughout the repository:

| Artifact | Pattern | Example |
|---|---|---|
| Requirement | `REQ-###` | `REQ-017` |
| Architecture decision | `ADR-###` | `ADR-006` |
| Risk | `RSK-###` | `RSK-012` |
| Security control | `CTL-###` | `CTL-025` |
| Evaluation | `EVAL-###` | `EVAL-009` |
| Test case | `TST-###` | `TST-041` |
| Runbook | `RBK-###` | `RBK-004` |
| Learning objective | `OBJ-###` | `OBJ-018` |

---

## 4. Focused Learning Roadmap

## Phase A — AI and ML Architecture Essentials

**Duration:** 2 weeks

### Objectives

- Understand the end-to-end ML lifecycle
- Distinguish deterministic software, analytics, ML, GenAI, RAG, and agents
- Understand model evaluation without becoming a data scientist
- Develop architecture-level knowledge of transformers and LLMs

### Topics

- ML problem types
- Training, validation, and testing
- Features and labels
- Batch and online inference
- Overfitting and data leakage
- Precision, recall, F1, ROC-AUC, MAE, and RMSE
- Embeddings, transformers, attention, and context windows
- Fine-tuning versus RAG
- Model confidence and human escalation

### Primary deliverable

`01-ai-ml-architecture-foundations/architecture/ai-use-case-decision-guide.md`

### Exit criteria

You can explain:

- Why a business problem requires AI
- Whether traditional ML or GenAI is appropriate
- What evaluation metric matters
- How a model is approved and monitored
- What happens when confidence is low

---

## Phase B — SageMaker and Production ML

**Duration:** 3 weeks

### Objectives

- Understand production ML architecture
- Design the ML lifecycle using SageMaker
- Select appropriate inference patterns
- Establish MLOps governance

### AWS capabilities

- SageMaker Processing
- SageMaker Training
- Feature Store
- Experiments
- Model Registry
- SageMaker Pipelines
- Model Monitor
- SageMaker Clarify
- Batch Transform
- Real-time endpoints
- Serverless inference
- Asynchronous inference
- Multi-model endpoints

### Required architecture decisions

- Bedrock versus SageMaker
- Real-time versus batch inference
- Serverless versus provisioned inference
- Managed algorithms versus custom containers
- Retraining trigger strategy
- Model rollback strategy

### Primary project

Build a production-style ML pipeline:

```text
S3
 |
 v
SageMaker Processing
 |
 v
Training
 |
 v
Evaluation
 |
 v
Model Registry
 |
 v
Approval
 |
 v
Deployment
 |
 v
Monitoring
```

### Exit criteria

You can design and govern a SageMaker solution without needing to develop advanced ML algorithms personally.

---

## Phase C — Amazon Bedrock and Generative AI

**Duration:** 4 weeks

### Objectives

- Master Amazon Bedrock architecture
- Build secure foundation-model applications
- Design prompt, context, routing, and guardrail strategies
- Establish token, latency, and cost controls

### Topics

- Foundation-model selection
- Bedrock Converse API
- Streaming
- Prompt Management
- Prompt versioning
- Embedding models
- Model evaluation
- Guardrails
- Batch inference
- Model customization
- Model routing and fallback
- Invocation logging
- Structured outputs

### Primary project

Build a secure enterprise chat application using:

- Amazon Bedrock
- API Gateway
- Lambda or EKS
- DynamoDB
- Guardrails
- CloudWatch
- KMS
- Private networking
- Terraform

### Required evidence

- Model-selection ADR
- Prompt catalogue
- Evaluation dataset
- Guardrail tests
- Token-cost model
- Failure and fallback design
- Operational runbook

---

## Phase D — Enterprise RAG

**Duration:** 4 weeks

### Objectives

- Design enterprise document ingestion and retrieval
- Build authorization-aware RAG
- Compare vector-storage options
- Evaluate retrieval and generation separately

### Topics

- Document extraction
- OCR and Textract
- Chunking strategies
- Embeddings
- Metadata
- Dense retrieval
- Sparse retrieval
- Hybrid search
- Reranking
- Query rewriting
- Document-level authorization
- Citation generation
- RAG evaluation
- Document lifecycle and deletion

### AWS capabilities

- Bedrock Knowledge Bases
- OpenSearch Service
- OpenSearch Serverless
- Aurora PostgreSQL with `pgvector`
- Amazon S3
- Textract
- Lambda
- Step Functions
- KMS

### Primary project

Build a secure multi-tenant document assistant with:

- Identity-aware retrieval
- Metadata filtering
- Source citations
- Hybrid search
- Guardrails
- Evaluation datasets
- Audit logging
- Cost metrics

### Required ADRs

- `ADR-001`: Managed Knowledge Base versus custom RAG
- `ADR-002`: OpenSearch versus Aurora PostgreSQL
- `ADR-003`: Chunking strategy
- `ADR-004`: Authorization-filtering model
- `ADR-005`: Reranking strategy

---

## Phase E — Agentic AI and Bedrock AgentCore

**Duration:** 4 weeks

### Objectives

- Understand controlled agent autonomy
- Build tool-using enterprise agents
- Learn Bedrock Agents and AgentCore
- Design human approval and policy enforcement
- Compare managed agents, EKS agents, and deterministic workflows

### Topics

- Agent planning
- Tool calling
- State and memory
- Human-in-the-loop
- Bedrock Agents
- AgentCore
- Strands Agents
- LangGraph
- MCP
- Multi-agent patterns
- Agent evaluation
- Agent observability
- Tool security

### Recommended enterprise pattern

```text
User request
     |
     v
Agent interprets intent
     |
     v
Agent selects an approved workflow
     |
     v
Step Functions performs controlled execution
     |
     v
Human approves sensitive action
     |
     v
Agent summarizes the result
```

### Primary project

Build a governed cloud-operations agent that can:

- Retrieve runbooks
- Query CloudWatch metrics
- Analyze incidents
- Recommend remediation
- Open a service ticket
- Request human approval
- Invoke a controlled Step Functions workflow
- Capture full execution traces

### Required controls

- Tool allowlist
- Least-privilege IAM
- Input and output schemas
- Execution-step limit
- Token budget
- Timeout
- Idempotency
- Human approval
- Memory expiry
- Complete audit trail

---

## Phase F — AI Security and Responsible AI

**Duration:** 3 weeks

### Objectives

- Extend landing-zone security patterns into AI
- Threat-model RAG and agent systems
- Establish Responsible AI governance
- Implement guardrails, data perimeters, and model controls

### Threats

- Prompt injection
- Indirect prompt injection
- Jailbreaking
- Sensitive-data disclosure
- Retrieval poisoning
- Vector-index poisoning
- Tool poisoning
- Excessive agency
- Memory poisoning
- Cross-tenant leakage
- Model denial of service
- Denial of wallet
- Insecure output handling

### AWS controls

- IAM
- Service Control Policies
- KMS
- PrivateLink and VPC endpoints
- CloudTrail
- CloudWatch
- Macie
- GuardDuty
- Security Hub
- AWS Config
- Bedrock Guardrails
- Data perimeters
- Central model-access governance

### Responsible AI governance

Document:

- Intended use
- Prohibited use
- Data classification
- Affected stakeholders
- Human oversight
- Evaluation thresholds
- Fairness considerations
- Explainability requirements
- Privacy controls
- Release criteria
- Incident handling
- Decommissioning

### Primary deliverables

- RAG threat model
- Agent threat model
- AI platform threat model
- Responsible AI assessment
- AI security review checklist
- Red-team test catalogue

---

## Phase G — MLOps, LLMOps, and AI Platform Engineering

**Duration:** 3 weeks

### Objectives

- Automate model, prompt, RAG, and agent delivery
- Establish continuous AI evaluation
- Design AI observability and FinOps
- Build a reusable enterprise AI platform architecture

### LLMOps areas

- Prompt versioning
- Model versioning
- Evaluation datasets
- RAG regression testing
- Agent regression testing
- Guardrail testing
- Knowledge Base versioning
- Model fallback
- Prompt rollback
- Continuous evaluation
- Trace analysis
- Cost per successful task

### Delivery pipeline

```text
Git commit
    |
    v
Code and prompt validation
    |
    v
Unit tests
    |
    v
Retrieval tests
    |
    v
Model evaluation
    |
    v
Security and guardrail tests
    |
    v
Agent tool tests
    |
    v
Staging deployment
    |
    v
Approval
    |
    v
Production canary
    |
    v
Continuous evaluation
```

### Evaluation gates

Define thresholds for:

- Correctness
- Groundedness
- Retrieval recall
- Citation accuracy
- Task-completion rate
- Tool-selection accuracy
- Unauthorized-action rate
- Safety
- Latency
- Cost per successful transaction

### Primary deliverable

An enterprise AI platform reference architecture containing:

- Model gateway
- Approved-model catalogue
- Prompt catalogue
- Guardrail service
- Knowledge service
- Vector service
- Agent runtime
- Tool gateway
- Evaluation service
- AI observability
- Tenant onboarding
- Cost allocation

---

## Phase H — Architecture Shaping and Executive Communication

**Duration:** 2 weeks

### Objectives

- Translate business problems into AI solution strategies
- Shape AI opportunities with sales and delivery teams
- Develop architecture and investment narratives
- Explain technical trade-offs to executives

### Use-case decision sequence

```text
Can deterministic software solve the problem?
 |
 +-- Yes --> Use conventional software
 |
 +-- No
       |
       v
Does the problem require prediction?
 |
 +-- Yes --> Traditional ML
 |
 +-- No
       |
       v
Does it require generation or unstructured reasoning?
 |
 +-- No --> Analytics or enterprise search
 |
 +-- Yes
       |
       v
Does it require enterprise knowledge?
 |
 +-- Yes --> RAG
 |
 +-- No --> Direct foundation-model invocation
       |
       v
Does it need adaptive actions?
 |
 +-- Yes --> Agent or hybrid workflow
 |
 +-- No --> GenAI application
```

### Required architecture outputs

- Business-context view
- Logical architecture
- Deployment architecture
- Data-flow view
- Trust-boundary view
- Network and private-connectivity view
- Model-selection ADR
- Vector-store ADR
- Security model
- Evaluation plan
- Responsible AI assessment
- RTO/RPO
- Cost model
- Delivery roadmap
- Operational runbooks

---

## 5. Suggested 24-Week Schedule

| Weeks | Focus | Primary output |
|---:|---|---|
| 1–2 | AI and ML architecture | AI use-case decision guide |
| 3–5 | SageMaker and production ML | Governed ML pipeline |
| 6–9 | Bedrock and GenAI | Secure Bedrock application |
| 10–13 | Enterprise RAG | Multi-tenant RAG assistant |
| 14–17 | Agentic AI and AgentCore | Governed operations agent |
| 18–20 | AI security and Responsible AI | Threat and governance pack |
| 21–22 | MLOps, LLMOps, and AI platform | Enterprise AI platform architecture |
| 23–24 | Solution shaping and portfolio | Architecture portfolio and interview pack |

---

## 6. Portfolio Projects

## 6.1 Enterprise AI Landing Zone

Extend AWS Control Tower and the existing landing zone to support AI workloads.

### Scope

- AI organizational units
- Experimentation, development, test, and production accounts
- Shared data and AI platform accounts
- Central logging and security accounts
- Model-access governance
- Region controls
- Service Control Policies
- Private Bedrock access
- KMS boundaries
- Prompt and model logging
- AI cost allocation
- Guardrail governance
- Tenant onboarding

### Key artifacts

- Organization and account model
- SCP catalogue
- Model access matrix
- Private connectivity design
- Security architecture
- Cost-allocation strategy
- AI workload onboarding runbook

---

## 6.2 Secure Multi-Tenant RAG Platform

### Scope

- Bedrock Knowledge Bases or custom RAG
- OpenSearch or Aurora PostgreSQL
- Tenant isolation
- Document-level authorization
- Metadata filters
- Hybrid search
- Reranking
- Citations
- Guardrails
- Evaluation
- Auditability
- Data deletion
- Cost dashboards

### Key artifacts

- Logical and deployment architecture
- Vector-store ADR
- Isolation model
- Authorization model
- Chunking strategy
- Evaluation report
- Threat model
- Cost-per-query model
- Operations runbook

---

## 6.3 Agentic Cloud-Operations Platform

### Scope

- Bedrock Agents or AgentCore
- Strands Agents or LangGraph
- Bedrock Knowledge Bases
- Step Functions
- Lambda
- EKS
- CloudWatch
- Systems Manager
- Ticketing integration
- Human approval

### Agent capabilities

- Investigate an incident
- Retrieve approved runbooks
- Query metrics
- Recommend remediation
- Request approval
- Invoke a controlled workflow
- Record evidence
- Summarize resolution

### Key artifacts

- Tool catalogue
- Tool permission matrix
- Agent state model
- Human-approval workflow
- Agent evaluation report
- Trace examples
- Threat model
- Failure-handling runbook
- Cost-per-task model

---

## 7. Progress Tracking

Use a phase-level status table in `00-program-governance/progress-tracker.md`.

| Phase | Status | Target date | Labs complete | Architecture complete | Evaluation passed |
|---|---|---|---:|---:|---:|
| AI/ML foundations | Not started |  | 0% | 0% | 0% |
| SageMaker | Not started |  | 0% | 0% | 0% |
| Bedrock | Not started |  | 0% | 0% | 0% |
| Enterprise RAG | Not started |  | 0% | 0% | 0% |
| Agentic AI | Not started |  | 0% | 0% | 0% |
| AI security | Not started |  | 0% | 0% | 0% |
| MLOps/LLMOps | Not started |  | 0% | 0% | 0% |
| AI platform | Not started |  | 0% | 0% | 0% |
| Portfolio | Not started |  | 0% | 0% | 0% |

---

## 8. Definition of Done for Each Phase

A phase is complete only when:

- Study notes are complete
- Mandatory labs run successfully
- Infrastructure can be recreated through code
- Architecture diagrams are stored in the repository
- Relevant ADRs are approved
- Security controls are documented
- Evaluation tests meet defined thresholds
- Cost implications are documented
- A runbook exists
- Evidence is linked from the phase README
- The learner can explain the architecture without notes

---

## 9. Recommended Branching Strategy

Use a lightweight Git model:

```text
main
├── phase/01-ai-ml-foundations
├── phase/02-sagemaker
├── phase/03-bedrock
├── phase/04-enterprise-rag
├── phase/05-agentic-ai
├── phase/06-ai-security
├── phase/07-mlops-llmops
├── phase/08-ai-platform
└── project/<project-name>
```

Recommended workflow:

1. Create one branch for a learning phase.
2. Complete notes, labs, architecture, and evaluation.
3. Open a pull request.
4. Use the pull-request checklist as a phase review.
5. Merge only after the phase definition of done is met.
6. Tag major milestones.

Suggested tags:

```text
v0.1-ai-ml-foundations
v0.2-sagemaker
v0.3-bedrock
v0.4-rag
v0.5-agentic-ai
v0.6-ai-security
v0.7-ai-platform
v1.0-portfolio-complete
```

---

## 10. Commit Message Convention

Use Conventional Commits:

```text
docs: add Bedrock model-selection notes
feat: implement streaming Converse API
lab: add OpenSearch hybrid-search exercise
arch: document multi-tenant RAG design
adr: select Aurora PostgreSQL for vector storage
eval: add citation-accuracy test suite
security: add prompt-injection controls
fix: correct Knowledge Base ingestion policy
runbook: add agent failure-recovery procedure
```

---

## 11. Suggested README for Each Phase

```markdown
# Phase Name

## Objective

Describe the capability to be developed.

## Prerequisites

List prior phases or required services.

## Learning Outcomes

- Outcome 1
- Outcome 2
- Outcome 3

## Topics

- Topic 1
- Topic 2
- Topic 3

## Labs

| Lab | Status | Evidence |
|---|---|---|
| Lab 1 | Not started | |
| Lab 2 | Not started | |

## Architecture Artifacts

- Logical architecture
- Deployment architecture
- Security view
- ADRs
- Threat model
- Cost model
- Runbook

## Evaluation Criteria

Define measurable completion thresholds.

## Resources

Link to `resources.md`.

## Completion Status

- [ ] Study notes complete
- [ ] Labs complete
- [ ] Architecture reviewed
- [ ] Security reviewed
- [ ] Evaluation passed
- [ ] Cost model complete
- [ ] Runbook tested
```

---

## 12. Recommended Study-Time Allocation

| Area | Allocation |
|---|---:|
| Bedrock and foundation-model architecture | 20% |
| Enterprise RAG and vector search | 20% |
| Agentic AI and AgentCore | 20% |
| AI security and Responsible AI | 15% |
| SageMaker and MLOps | 10% |
| LLMOps and evaluation | 10% |
| Business shaping and architecture communication | 5% |

---

## 13. Certification Path

For an architect with extensive AWS experience:

### Optional

- AWS Certified AI Practitioner

### Recommended

1. AWS Certified Machine Learning Engineer – Associate
2. AWS Certified Generative AI Developer – Professional

Certifications should validate the practical learning program. They should not replace architecture projects, labs, threat models, evaluation reports, or operating runbooks.

---

## 14. Final Competency Target

At completion, the learner should be able to state and demonstrate:

> I can extend an AWS landing zone into a governed enterprise AI platform; design traditional ML and GenAI solutions; implement secure multi-tenant RAG; deploy controlled agentic systems; and establish AI security, Responsible AI, evaluation, LLMOps, observability, FinOps, and operational governance.

The repository should function simultaneously as:

- A structured study plan
- A working laboratory
- An architecture knowledge base
- An implementation reference
- An interview preparation asset
- A professional AWS AI architecture portfolio

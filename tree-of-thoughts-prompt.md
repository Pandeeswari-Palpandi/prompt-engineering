# give a tree of thoughts prompt for creating a AI agent

# Tree-of-Thoughts Prompt for Creating an AI Agent

## ROLE

You are an expert AI Agent Architect, Software Engineer, and Solution Designer.

Your task is to design, plan, and implement an AI Agent for the user's requirements.

Use a **Tree-of-Thoughts-inspired problem-solving approach**:

- Explore multiple possible approaches internally.
- Break the problem into independent branches.
- Evaluate each branch against clear criteria.
- Select the strongest approach.
- Refine the selected approach before implementation.
- Do not reveal private chain-of-thought or hidden reasoning. Provide only concise decisions, evaluations, and conclusions.

---

# 1. UNDERSTAND THE REQUIREMENT

First identify:

- What problem the AI Agent should solve
- Target users
- Main objective
- Expected inputs
- Expected outputs
- Required actions
- External systems/APIs involved
- Required tools
- Data sources
- Security requirements
- Performance requirements
- Cost constraints
- Deployment environment

If requirements are unclear, ask only the minimum necessary questions.

---

# 2. DEFINE THE AI AGENT

Create an agent definition containing:

### Agent Name

Give the agent a meaningful name.

### Purpose

Clearly describe what the agent does.

### Responsibilities

List the major responsibilities.

### Inputs

Define all expected inputs.

### Outputs

Define the expected outputs.

### Tools

Identify tools the agent needs, such as:

- Web Search
- Database
- REST API
- File System
- Email
- Calendar
- Python
- Browser
- Vector Database
- RAG
- External SaaS APIs

### Memory

Determine whether the agent requires:

- Short-term memory
- Long-term memory
- Conversation memory
- User preferences
- Vector memory

---

# 3. CREATE MULTIPLE SOLUTION BRANCHES

Generate 3-5 possible architectures.

For example:

### Branch A — Simple AI Agent

LLM
↓
Prompt
↓
Tools
↓
Response

### Branch B — RAG Agent

User
↓
Agent
↓
Retriever
↓
Vector Database
↓
LLM
↓
Response

### Branch C — Multi-Agent System

User
↓
Orchestrator
├── Research Agent
├── Analysis Agent
├── Execution Agent
└── Validation Agent
↓
Final Response

### Branch D — Workflow-Based Agent

Trigger
↓
AI Agent
↓
Decision
├── Action A
├── Action B
└── Action C
↓
Result

Evaluate which architecture best matches the requirement.

---

# 4. EVALUATE EACH BRANCH

Score every architecture from 1-10 using:

| Criteria        | Score |
| --------------- | ----: |
| Simplicity      |   /10 |
| Scalability     |   /10 |
| Reliability     |   /10 |
| Cost            |   /10 |
| Performance     |   /10 |
| Maintainability |   /10 |
| Security        |   /10 |
| Extensibility   |   /10 |

Then provide:

- Recommended architecture
- Why it was selected
- Main trade-offs
- Why the other approaches were rejected

---

# 5. DESIGN THE AGENT ARCHITECTURE

Create a high-level architecture containing:

```text
User
  ↓
Interface
  ↓
API / Gateway
  ↓
AI Agent
  ↓
Orchestrator
  ├── LLM
  ├── Memory
  ├── Knowledge / RAG
  ├── Tools
  ├── APIs
  └── Validation
  ↓
Response
```

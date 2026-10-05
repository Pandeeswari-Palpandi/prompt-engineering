# Prompt I gave in chatGpt to get the sequential prompt

## give a sequential prompt to learn and execute about n8n workflow

# n8n Workflow Learning & Execution — Master Prompt

## Role

Act as my **n8n Automation Mentor, Workflow Architect, and Practical Trainer**.

My goal is to learn n8n from beginner to advanced level by **building real workflows**, not just reading theory.

Every topic should include:

- Simple explanation
- Practical use case
- Step-by-step n8n implementation
- Node-by-node configuration
- Sample input/output data
- Testing instructions
- Common errors and fixes
- Best practices
- Mini assignment

Use **simple language** and assume I am learning n8n for the first time.

---

# Learning Rules

Follow the learning stages sequentially.

Do **not** jump to advanced topics until the current stage is completed.

For every workflow:

1. Explain the business problem
2. Show the workflow architecture
3. List all required n8n nodes
4. Explain why each node is required
5. Give exact node configuration
6. Provide sample data
7. Explain how data flows between nodes
8. Tell me how to execute/test it
9. Explain expected output
10. Explain common errors
11. Give an improvement challenge

Whenever possible, show the workflow like:

```text
Trigger
   ↓
Node 1
   ↓
Node 2
   ↓
Condition
   ↓
Action
   ↓
Output
```

---

# STAGE 1 — n8n Fundamentals

## Day 1 — Introduction to n8n

Teach me:

- What is n8n?
- What is workflow automation?
- n8n vs Zapier vs Make
- What are nodes?
- What are triggers?
- What are actions?
- What is workflow execution?
- What is JSON data?
- What is an expression?
- What is a credential?

### Practical Task

Create:

```text
Manual Trigger
      ↓
Set/Edit Fields
      ↓
Output
```

Create a simple JSON object:

```json
{
  "name": "John",
  "email": "john@example.com",
  "age": 30
}
```

Explain exactly how to create and execute it.

### Assignment

Create a workflow that accepts:

- name
- email
- phone
- city

and outputs a formatted customer object.

---

# STAGE 2 — Data Handling

## Day 2 — Understanding JSON

Teach:

- JSON objects
- Arrays
- Nested JSON
- Accessing JSON fields
- Expressions
- Dynamic values
- `$json`
- Referencing previous nodes

### Practical Workflow

```text
Manual Trigger
      ↓
Set Data
      ↓
Edit Fields
      ↓
Output
```

Practice:

```text
{{$json.name}}
{{$json.email}}
```

### Assignment

Create customer data and generate:

```json
{
  "customerName": "...",
  "contact": "...",
  "location": "..."
}
```

---

## Day 3 — Expressions

Teach:

- String expressions
- Number expressions
- Date expressions
- Conditional expressions
- Combining fields
- Basic JavaScript expressions

### Practical Task

Input:

```json
{
  "firstName": "John",
  "lastName": "David",
  "age": 28
}
```

Generate:

```json
{
  "fullName": "John David",
  "isAdult": true
}
```

### Assignment

Create a customer profile formatter.

---

# STAGE 3 — Logic & Conditions

## Day 4 — IF Node

Teach:

- IF node
- Boolean conditions
- String comparison
- Number comparison
- Multiple conditions

### Practical Workflow

```text
Customer Input
      ↓
IF — Age >= 18
      ↓
   ┌──┴──┐
  Yes   No
   ↓     ↓
Adult   Minor
```

### Assignment

Create an employee salary classification:

```text
< 5 LPA       → Junior
5–10 LPA      → Mid Level
> 10 LPA      → Senior
```

---

## Day 5 — Switch Node

Teach:

- Switch node
- Multiple branches
- Routing data

### Practical Workflow

```text
Customer Type
      ↓
    Switch
   ┌───┼────┐
   ↓   ↓    ↓
Premium Standard Basic
```

Each branch should perform a different action.

### Assignment

Create a support ticket routing workflow:

```text
Billing    → Finance Team
Technical  → Engineering Team
Sales      → Sales Team
Other      → Support Team
```

---

# STAGE 4 — APIs

## Day 6 — HTTP Request

Teach:

- REST API
- GET
- POST
- PUT
- DELETE
- Headers
- Query parameters
- Request body
- Authentication
- JSON response

### Practical Workflow

```text
Manual Trigger
      ↓
HTTP Request
      ↓
Process Response
      ↓
Output
```

Use a public test API.

### Assignment

Call an API and extract:

- ID
- Name
- Email
- Address

---

## Day 7 — API Integration

Build:

```text
Webhook
   ↓
Validate Request
   ↓
HTTP Request
   ↓
Transform Data
   ↓
Response
```

Teach:

- Webhook
- Request body
- Query parameters
- Response
- API testing using Postman

### Assignment

Build a simple customer registration API workflow.

---

# STAGE 5 — Databases

## Day 8 — Database Basics

Teach n8n database integration.

Start with:

- PostgreSQL
- MySQL

Teach:

- Connection
- SELECT
- INSERT
- UPDATE
- DELETE
- Parameterized queries
- Handling database results

### Workflow

```text
Webhook
   ↓
Validate Customer
   ↓
Database
   ↓
Response
```

### Assignment

Create a customer registration workflow.

---

## Day 9 — Database + API

Build:

```text
API Request
      ↓
Validate
      ↓
Database Query
      ↓
IF
      ↓
Response
```

Example:

Check whether an email already exists.

If exists:

```text
Customer already exists
```

Otherwise:

```text
Insert customer
```

---

# STAGE 6 — Loops & Data Processing

## Day 10 — Working With Multiple Items

Teach:

- Arrays
- Multiple items
- Looping
- Split Out
- Aggregate
- Merge

### Practical Workflow

```text
Customer List
      ↓
Split Items
      ↓
Process Each Customer
      ↓
Aggregate Results
```

### Assignment

Process 100 customer records and classify them.

---

## Day 11 — Merge & Data Transformation

Teach:

- Merge
- Combining API responses
- Joining datasets
- Data transformation

### Assignment

Combine:

```text
Customer API
     +
Order API
```

into:

```json
{
  "customer": "...",
  "orders": [],
  "totalOrderValue": 0
}
```

---

# STAGE 7 — Scheduling & Automation

## Day 12 — Schedule Trigger

Teach:

- Schedule Trigger
- Cron
- Daily execution
- Weekly execution
- Monthly execution

### Practical Workflow

```text
Schedule
   ↓
Fetch Data
   ↓
Process
   ↓
Send Report
```

### Assignment

Create a daily sales report workflow.

---

## Day 13 — Email Automation

Build:

```text
Schedule
   ↓
Fetch Data
   ↓
Generate Report
   ↓
Send Email
```

Practice:

- Gmail
- SMTP
- Email templates
- Attachments

### Assignment

Create an automated daily business report.

---

# STAGE 8 — Real Business Automation

## Day 14 — Lead Management

Build:

```text
Website Form
      ↓
Webhook
      ↓
Validate Lead
      ↓
Store Lead
      ↓
Lead Score
      ↓
Send Notification
      ↓
Email Lead
```

Teach:

- Lead qualification
- CRM concepts
- Notifications
- Email automation

---

## Day 15 — Google Sheets Automation

Build:

```text
Google Form
      ↓
Google Sheets
      ↓
n8n
      ↓
Process Lead
      ↓
Email
      ↓
Notification
```

Teach Google Sheets integration.

### Assignment

Create an automated lead management system.

---

# STAGE 9 — AI + n8n

## Day 16 — Introduction to AI Nodes

Teach:

- LLM
- Prompt
- AI Agent
- Chat Model
- Memory
- Tools
- Structured output

Explain how AI fits into n8n.

---

## Day 17 — AI Text Processing

Build:

```text
Webhook
      ↓
Customer Message
      ↓
AI
      ↓
Classify
      ↓
Route
      ↓
Response
```

Example:

Customer message:

```text
"I want to cancel my subscription."
```

AI output:

```json
{
  "category": "Cancellation",
  "priority": "High",
  "sentiment": "Negative"
}
```

---

## Day 18 — AI Lead Scoring

Build:

```text
Lead
 ↓
AI Analysis
 ↓
Lead Score
 ↓
IF
 ├── Hot Lead
 ├── Warm Lead
 └── Cold Lead
```

AI should evaluate:

- Industry
- Company size
- Requirement
- Budget
- Buying intent

---

# STAGE 10 — AI Agent

## Day 19 — Build an AI Agent

Teach:

- AI Agent
- Tools
- Memory
- System prompt
- Tool calling
- Structured responses

Build:

```text
User
 ↓
AI Agent
 ├── Database Tool
 ├── API Tool
 ├── Calculator
 └── Knowledge Tool
```

### Assignment

Build an AI business assistant.

---

# STAGE 11 — Advanced n8n

## Day 20 — Error Handling

Teach:

- Error Trigger
- Retry
- Continue on Fail
- Error workflows
- Logging
- Notifications

Build:

```text
Workflow
   ↓
Process
   ↓
Error
   ↓
Log Error
   ↓
Send Alert
```

---

## Day 21 — Production Best Practices

Teach:

- Credentials
- Environment variables
- Security
- Webhook security
- API authentication
- Rate limits
- Retry strategy
- Idempotency
- Logging
- Monitoring
- Workflow naming
- Reusable sub-workflows

---

# STAGE 12 — Real-World Projects

After completing the learning stages, build these projects sequentially.

## Project 1 — Automated Lead Generator

```text
Website
   ↓
Webhook
   ↓
Lead Validation
   ↓
AI Lead Scoring
   ↓
Database
   ↓
CRM
   ↓
Email
   ↓
WhatsApp/Notification
```

---

## Project 2 — AI Customer Support

```text
Customer
   ↓
Webhook
   ↓
AI Agent
   ├── FAQ Knowledge
   ├── Order API
   ├── Customer Database
   └── Ticket Creation
   ↓
Response
```

---

## Project 3 — Invoice Automation

```text
Invoice Data
   ↓
Validation
   ↓
Database
   ↓
Generate Invoice
   ↓
PDF
   ↓
Email Customer
```

---

## Project 4 — AI SEO Lead Generation

```text
Website URL
   ↓
Website Analysis
   ↓
SEO Analysis
   ↓
AI
   ↓
SEO Score
   ↓
Recommendations
   ↓
Lead Report
   ↓
Email
```

---

# FINAL PROJECT — Business Automation Platform

Build a complete automation platform using:

- n8n
- PostgreSQL
- REST APIs
- AI
- Google Sheets
- Email
- Webhook
- Dashboard

Architecture:

```text
                 ┌──────────────┐
                 │   Website    │
                 └──────┬───────┘
                        ↓
                 ┌──────────────┐
                 │   Webhook    │
                 └──────┬───────┘
                        ↓
                 ┌──────────────┐
                 │     n8n      │
                 │ Orchestrator │
                 └──────┬───────┘
                        ↓
          ┌─────────────┼─────────────┐
          ↓             ↓             ↓
      PostgreSQL       AI          REST APIs
          ↓             ↓             ↓
          └─────────────┼─────────────┘
                        ↓
              ┌─────────────────┐
              │ Business Logic  │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │ Email / Alerts  │
              └─────────────────┘
```

---

# How You Should Teach Me

For each day, respond using this exact structure:

## 1. Concept

Explain the concept in simple terms.

## 2. Why It Matters

Explain where this is used in real companies.

## 3. Architecture

Show the workflow visually.

## 4. Nodes Required

Provide a table:

| Node    | Purpose         |
| ------- | --------------- |
| Trigger | Starts workflow |
| Node 1  | ...             |
| Node 2  | ...             |

## 5. Step-by-Step Implementation

Give exact steps for creating the workflow in n8n.

## 6. Configuration

For every node, explain:

- Node name
- Operation
- Important fields
- Expressions
- Sample values

## 7. Test Data

Give copy-paste-ready JSON.

## 8. Expected Output

Show the expected JSON/result.

## 9. Common Errors

Explain likely errors and fixes.

## 10. Mini Challenge

Give me one small task to complete myself.

## 11. Interview Questions

Give me 3–5 n8n interview questions related to the topic.

## 12. Real-World Challenge

Explain how this concept would be used in a production system.

---

# Important Learning Rule

Do not simply give me the complete solution immediately.

First explain the task.

Let me attempt it.

If I ask for help:

1. Give a hint first.
2. If I still need help, show the relevant configuration.
3. Finally provide the complete solution.

Track my progress as:

```text
Day 1 — Not Started
Day 2 — Not Started
Day 3 — Not Started
...
Final Project — Not Started
```

When I say:

```text
START DAY 1
```

begin Day 1.

Do not move to Day 2 until I complete the Day 1 assignment.

When I say:

```text
NEXT
```

move to the next topic only after briefly checking whether I understood the previous topic.

When I say:

```text
SHOW SOLUTION
```

provide the complete solution.

When I say:

```text
EXPLAIN
```

explain the current topic with a simpler real-world example.

When I say:

```text
INTERVIEW MODE
```

switch to n8n interview questions and evaluate my answers.

When I say:

```text
PROJECT MODE
```

start building a production-style n8n project step by step.

When I say:

```text
DEBUG
```

help me troubleshoot my workflow using the error/output I provide.

---

# START

Start with:

## DAY 1 — What is n8n and Your First Workflow

Do not move to Day 2 until I complete the Day 1 assignment.

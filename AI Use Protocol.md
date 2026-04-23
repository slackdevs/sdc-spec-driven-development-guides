# AI Use Protocol — AI Projects 

---

## 1. Purpose

This document defines how AI is used across AI Projects.

**Objectives:**

* Prevent security, legal, and compliance risks
* Standardize AI usage across the team
* Increase execution speed without compromising control

**This protocol is mandatory and will evolve over time.**

---

## 2. Core Principle

* AI is a tool. Humans are responsible.
* AI does not make decisions
* AI does not control systems
* The user is fully accountable for outputs

---

## 3. AI Usage Categories

### 3.1 Automation (No Human Review Required)

**Definition:**
Low-risk tasks where AI transforms existing content without creating new meaning.

**Allowed Use Cases:**

* Translation (EN ↔ ES)
* Text formatting / cleanup
* Summarization
* Data extraction
* Rewriting (same meaning preserved)
* Classification / tagging

**Conditions:**

* No sensitive data
* No financial or legal impact
* No decision-making outputs

---

### 3.2 Content Generation (Human Validation Required)

**Definition:**
AI generates new content, logic, or ideas.

**Allowed Use Cases:**

* Code generation
* Documentation
* Product specs
* User flows
* UI components
* Marketing content
* AI-generated simulations

**Mandatory Rule:**
All outputs must be reviewed and approved by a human.

**Validator Responsibility:**

* Accuracy
* Compliance
* Alignment with product rules

**Validation Checklist:**

* Is it correct?
* Is it compliant?
* Could it be interpreted as financial advice?
* Does it introduce risk?

If unclear → escalate.

---

### 3.3 Prohibited Use (Strictly Forbidden)

#### A. Financial & Legal Risk

* Generating financial advice as authoritative
* Making automated investment decisions
* Communicating recommendations without disclaimers

#### B. System Control

* Executing actions in production
* Triggering payments or investment flows
* Autonomous agents performing transactions

#### C. Security Violations

* Sharing API keys, credentials, tokens
* Exposing private repositories
* Connecting AI directly to internal systems

#### D. Sensitive Data Exposure

* User financial data
* PII
* KYC / AML data
* Legal or partner agreements

---

## 4. Input & Access Restrictions

**Never provide AI with:**

* Production access
* Database credentials
* API keys / secrets
* Financial or personal user data
* Internal system architecture
* Partner contracts

**Allowed Inputs:**

* Mock data
* Sanitized data
* Public or non-sensitive internal docs

---

## 5. AI Tools & Infrastructure (MCP, External Tools, etc.)

This section governs which AI tools can be used and how.

### 5.1 Approved Tool Types

* LLM interfaces (ChatGPT, Claude, Gemini)
* IDE copilots (code assistants)
* Internal AI workflows
* MCP Servers (Model Context Protocol)
* Automation tools with AI capabilities

---

### 5.2 MCP Servers & Advanced Integrations

**Definition:**
MCP servers or similar systems that allow AI to:

* Access tools
* Retrieve data
* Execute workflows

**Rules for MCP / Tool Integrations**

**STRICT REQUIREMENTS:**

* **No Production Access**
  MCP tools must NOT connect to production environments

* **Sandbox Only**
  Only staging / sandbox environments allowed

* **No Secrets Exposure**
  API keys must never be passed through prompts
  Use secure environment variables only

* **Scoped Permissions**
  Tools must have minimal required access (least privilege)

* **No Autonomous Execution**
  AI cannot execute:

  * Financial transactions
  * Investment routing
  * Payments

* **Auditability**
  All tool usage must be traceable

---

### 5.3 Tool Approval Process

Before using a new AI tool:

**Evaluate:**

* Data access
* Security risks
* Compliance impact

**Required:**

* Product approval
* Engineering validation (if integrated)
* Documentation of use case

---

### 5.4 Forbidden Tool Usage

**Connecting AI directly to:**

* Production DB / systems
* Payment systems
* Banking APIs (Plaid, Stripe, etc.)

**Uploading:**

* Real user data
* Internal financial data

---

## 6. Decision Framework (Quick Check)

Before using AI, ask:

* Does this involve real user data?
* Could this impact money or investments?
* Am I exposing credentials or system access?
* Will this output go live without review?
* Could this create legal risk?

If any answer = **YES** → stop or require validation

---

## 7. Responsibility Model

The AI user is responsible for:

* Inputs
* Outputs
* Consequences

**No exceptions.**

---

## 8. Compliance Alignment

This protocol ensures alignment with:

* No custody risk (MVP requirement)
* Secure access control
* Clear separation from financial advice

Failure to comply can:

* Block launch
* Create regulatory exposure
* Compromise user trust

---

## 9. Evolution

This is a living document.

It will evolve based on:

* Product needs
* Compliance updates
* Team learnings

---

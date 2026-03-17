# Meta-Data-Driven-AI-Agents

A collection of **patterns, frameworks, and reusable building blocks** for building AI agents that behave like domain experts, evaluate work like professors, hydrate documents from unstructured data, enforce governance policies, and operate like full applications — all without custom code or model training.

---

## Repository Structure

```
ProfessorJarvisAIAgent/
├── Rubrics/                    AI grading agents with structured rubrics
├── Personalities/              Richly detailed fictional human personas
├── Communities/                Multi-agent orchestration & governance
├── DataMapping/                Document hydration from unstructured data
└── DynamicApplications/        AI agents that behave like full applications
```

---

## Rubrics/

**Problem:** Evaluating unstructured work (essays, proposals, code, resumes) is inconsistent, slow, unscalable, and opaque. Two reviewers score the same submission differently. Feedback is vague. Rubrics exist on paper but aren't enforced systematically.

**Solution:** Each rubric agent is powered by three knowledge source files (instruction set JSON, grading heuristics JSON, agent instructions TXT) that can be uploaded directly into Microsoft Copilot Studio, Azure AI Agent Service, OpenAI Assistants, or any AI platform that supports knowledge grounding. No code, no fine-tuning, no model training.

**What's Inside:** 11 professor agents spanning Art, Business, Computer Science, English, History, Law, Math, Music, Philosophy, Psychology, and Science — each with domain-specific rubrics, scoring criteria, penalty rules, and a mandatory 6-step evaluation workflow.

**Use Cases:**
- Automated essay and assignment grading with evidence-based feedback
- Consistent evaluation across hundreds of submissions
- Compliance document review against structured criteria
- Resume screening with defensible, rubric-based scoring

---

## Personalities/

**Problem:** AI agents default to generic, personality-less responses. They lack the depth needed to simulate realistic professional interactions — no backstory, no communication style, no ethical boundaries, no domain-specific vocabulary.

**Solution:** 13 richly detailed fictional human personas, each defined by a structured JSON schema covering identity, psychometrics, values, backstory, scenario hooks, dialogue samples, and behavioral constraints. Each persona includes an instruction file that tells an AI agent exactly how to embody the character.

**What's Inside:** Personas spanning healthcare (Doctor, Nurse, Chaplain), law (Criminal Defense Attorney), public safety (Police Officer, Firefighter), trades (Electrician, Plumber), education (High School Teacher), government (City Council Member), and financial services (Retirement Advisor, Stock Market Advisor, Wealth Advisor). Includes a deployment framework for pushing personas to Azure AI Agent Service.

**Use Cases:**
- Training simulations (medical, legal, law enforcement scenarios)
- Customer service agent prototyping with realistic personality
- Multi-agent community members (see Communities/)
- Narrative design and conversational AI testing
- Empathy and communication skills training

---

## Communities/

**Problem:** Complex decisions rarely live in a single domain. A veteran's transition involves healthcare, legal, financial, career, and mental health expertise. Getting multi-disciplinary guidance today requires finding the right experts, coordinating schedules, bridging vocabulary across specialties, and ensuring advice doesn't contradict.

**Solution:** The **Community Orchestrator Pattern** — a single gateway agent routes user requests to a community of connected personality agents, each representing a distinct expert. The orchestrator manages intent detection, routing, multi-agent invocation, and response synthesis so the user experiences a seamless panel of experts through one conversational interface.

**What's Inside:**
- Orchestrator pattern documentation and use case analysis
- Governance policy framework (global, safety, domain, tone) with layered priority enforcement
- Policy manifests and example policy sets for deploying governed agent communities

**Use Cases:**
- Multi-disciplinary advisory panels (veteran services, procurement, incident response)
- Governed AI agent communities with layered safety and compliance policies
- Domain-specific guardrails (medical, legal, financial) applied across agent fleets

---

## DataMapping/

**Problem:** Organizations spend significant time manually transcribing data from unstructured sources (emails, dictations, meeting notes, scanned forms) into structured document templates. This process is time-consuming, error-prone, inconsistent, and audit-risky.

**Solution:** A **document hydration pattern** that uses AI inference to extract structured field values from unstructured text, normalize them against a JSON schema, map them into document templates with confidence scoring, and produce a graded mapping report — all driven by a mapping specification rather than application code.

**What's Inside:**
- **Example 1** — Enterprise Service Request: 42-field business intake form hydrated from a casual email. Demonstrates the core pattern with keyword detection, confidence scoring, and a 100-point grading model.
- **Example 2** — VA CPRS Primary Care Progress Note: 75-field clinical note hydrated from a physician dictation. Extends the pattern with clinical safety rules (mandatory clinician review for risk assessment and diagnoses), ICD-10 validation, SOAP section inference, and vital sign normalization.
- Reusable creation prompt for generating new document hydration solutions

**Use Cases:**
- Clinical note completion from provider dictations
- Enterprise intake form processing from emails
- Insurance application hydration from scanned documents
- Incident report generation from narrative accounts
- HR onboarding form completion from candidate submissions
- Any unstructured-to-structured document workflow

---

## DynamicApplications/

**Problem:** Building interactive CRUD applications traditionally requires full-stack development — frontend, backend, database, API layer, validation logic. For simple structured-data applications, this overhead is disproportionate to the value delivered.

**Solution:** AI agents that behave like fully functional applications, operating from metadata contracts, schemas, and heuristics rather than compiled code. The agent maintains application state, enforces data models, validates input, handles errors, and presents menus — all defined through declarative JSON files.

**What's Inside:**
- **ContactBlackBook** — A complete contacts/address book application defined entirely through 10 metadata files: data model schema, tool contracts, CRUD workflows, menus, validation heuristics, error messages, security rules, and test scenarios. The AI agent interprets these files and operates as a deterministic, schema-enforced CRUD application.

**Use Cases:**
- Rapid prototyping of data-entry applications without code
- Contact management, task tracking, inventory systems
- Schema-enforced CRUD interfaces for any structured data domain
- Application behavior testing through declarative test scenarios

---

## Design Philosophy

All patterns in this repository share common principles:

| Principle | Description |
|---|---|
| **No custom code** | Solutions are driven by structured knowledge files (JSON schemas, instruction sets, mapping specs) — not application code or model fine-tuning |
| **Platform agnostic** | Knowledge files work with Microsoft Copilot Studio, Azure AI Agent Service, OpenAI Assistants, or any platform supporting knowledge grounding |
| **Human-in-the-loop** | Every pattern explicitly accounts for partial automation, ambiguity, and human review — especially in clinical, legal, and compliance contexts |
| **Deterministic** | Given the same inputs and knowledge files, agents produce the same outputs |
| **Layered governance** | Policies, personas, and instructions compose hierarchically — global rules override domain rules which override agent-level rules |

---

## Getting Started

1. **Pick a pattern** — Choose the folder that matches your use case
2. **Read the README** — Each folder contains its own documentation
3. **Upload knowledge files** — Load the JSON/TXT/MD files into your AI platform as knowledge sources
4. **Test with examples** — Each pattern includes sample inputs and expected outputs
5. **Extend** — Add new personas, rubrics, document templates, or application schemas following the established patterns

# AI-Friendly Project Scaffold

This repository provides two reusable documents for starting software projects that will be developed with Coding Agents.

It is **not** a framework, code generator, technology stack, or application starter. Its purpose is to establish a clear project knowledge system before implementation begins, so humans and Coding Agents can work from the same product, architecture, testing, and collaboration context.

## What This Repository Contains

### `PROJECT-BRIEF-TEMPLATE.md`

A client- or sponsor-facing template for preparing the initial business context.

It captures what is already known at project initiation, such as:

- background and trigger;
- problem or opportunity;
- initial objective;
- business motivation;
- known facts and constraints;
- available source materials;
- assumptions, unknowns, and discovery questions.

It intentionally does **not** require the client to define Personas, User Journeys, User Stories, Acceptance Criteria, Domain Models, service architecture, APIs, databases, technology stacks, or CI/CD. Those should be discovered and designed later.

### `AI-FRIENDLY-PROJECT-SCAFFOLD-PROMPT.md`

A technology-neutral meta-prompt for a Coding Agent.

Given a completed Project Brief, it instructs the Agent to create and maintain an AI-friendly repository knowledge base, including:

- `README.md` — project entry point;
- `SPEC.md` — current product contract, with each User Story next to its Acceptance Criteria;
- `ARCHITECTURE.md` — current Domain Model, service/runtime architecture, data ownership, Clean Architecture mapping, and test architecture;
- `AGENTS.md` — permanent operating rules for Coding Agents;
- `PROJECT-STATE.md` — current collaboration phase, scope, blockers, and next authorized step;
- `REVIEW.md` — decision history, superseded designs, evidence, technical debt, and retrospective;
- `AI-CODING-PRACTICE.md` — human–AI collaboration record and correction history.

The prompt also establishes:

- a permanent Business Discovery → Final Audit workflow;
- Clean Architecture dependency rules;
- a layered automated-testing pyramid;
- explicit evidence classifications;
- automatic context rehydration for new Coding Agent windows;
- strict protection of the original Project Brief and scaffold prompt.

## Recommended Workflow

### 1. Prepare the Project Brief

Copy the template into the new project and rename the completed file:

```text
PROJECT-BRIEF-TEMPLATE.md  ->  PROJECT-BRIEF.md
```

The client, sponsor, or human project owner completes it using only currently known information. Unknown topics may remain marked as `Unknown`, `To be discovered`, or as discovery questions.

### 2. Add the Scaffold Prompt

Copy `AI-FRIENDLY-PROJECT-SCAFFOLD-PROMPT.md` into the target project repository.

The target repository initially needs only:

```text
PROJECT-BRIEF.md
AI-FRIENDLY-PROJECT-SCAFFOLD-PROMPT.md
```

### 3. Hand Both Files to the Coding Agent

Ask the Coding Agent to read both files and run the scaffold bootstrap with parameters such as:

```text
PROJECT_BRIEF_PATH=PROJECT-BRIEF.md
SCAFFOLD_PROMPT_PATH=AI-FRIENDLY-PROJECT-SCAFFOLD-PROMPT.md
TARGET_REPOSITORY_PATH=.
REPOSITORY_MODE=new
PRIMARY_DOCUMENT_LANGUAGE=English
AGENT_ADAPTERS=codex
```

Example instruction:

```text
Read PROJECT-BRIEF.md and AI-FRIENDLY-PROJECT-SCAFFOLD-PROMPT.md in full.
Use the parameters above and perform the repository bootstrap exactly as defined
by the scaffold prompt. Do not implement product features, choose a technology
stack, create CI/CD, commit, or push.
```

For an existing repository, use:

```text
REPOSITORY_MODE=existing
```

The Agent should inspect the current repository before aligning or creating the project documents.

### 4. Review the Generated Baseline

Before implementation begins, humans should review at least:

- `SPEC.md` for the product scope, discovery status, User Stories, and Acceptance Criteria;
- `ARCHITECTURE.md` for the Domain Model, service responsibilities, dependencies, data ownership, Clean Architecture boundaries, and testing strategy;
- `AGENTS.md` for permanent Agent rules;
- `PROJECT-STATE.md` for the current phase and next authorized step.

Unresolved product or architecture questions should remain explicit. The Coding Agent must not invent answers merely to make the documents look complete.

### 5. Continue Through the Defined Lifecycle

Future work should follow the lifecycle established by the scaffold prompt:

```text
Context Rehydration and Current-State Audit
-> Business Discovery
-> Product Definition and UX/Interaction Design
-> Domain and Architecture Design
-> Increment Planning
-> Increment Implementation
-> Increment Verification and Audit
-> Integration, Regression, and Documentation Closure
-> Final Audit
```

When a new Coding Agent window starts, the Agent should automatically recover context from the protected inputs, `AGENTS.md`, `PROJECT-STATE.md`, current specification and architecture documents, Git state, relevant source, and tests. The user should not need to manually reconstruct the previous conversation.

## Protected Input Rule

In the **target project**, the following become protected, immutable inputs after handoff:

```text
PROJECT-BRIEF.md
AI-FRIENDLY-PROJECT-SCAFFOLD-PROMPT.md
```

A project Coding Agent must never edit, reformat, rename, move, delete, overwrite, or bulk-modify them.

If either input needs to change, the client, sponsor, or human project owner must prepare a new version outside Coding Agent execution. The Agent may then read the replacement and record its impact in the repository-owned project documents.

`PROJECT-BRIEF-TEMPLATE.md` in this template repository remains a reusable source template; the immutable rule applies to the completed Project Brief after it is handed to a project Coding Agent.

## What This Repository Does Not Do

This repository does not:

- replace Business Discovery;
- generate a complete application;
- prescribe a programming language or framework;
- require a monorepo or microservices;
- create CI/CD by default;
- require Domain Services or Domain Events;
- authorize a Coding Agent to invent product or architecture decisions;
- prove that anything has been implemented, tested, deployed, or production-verified.

Its role is to create a durable, auditable context in which those decisions and implementation steps can happen safely.

## Intended Users

This toolkit is useful for:

- clients or sponsors preparing initial project context;
- architects defining product and solution boundaries;
- teams starting AI-assisted software projects;
- developers using Codex, Claude Code, Cursor, Copilot, or other Coding Agents;
- existing projects that need clearer documentation ownership and Agent governance.

## Files

- [`PROJECT-BRIEF-TEMPLATE.md`](PROJECT-BRIEF-TEMPLATE.md)
- [`AI-FRIENDLY-PROJECT-SCAFFOLD-PROMPT.md`](AI-FRIENDLY-PROJECT-SCAFFOLD-PROMPT.md)

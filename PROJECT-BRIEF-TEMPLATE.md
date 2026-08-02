# Project Brief Template

> Version: 1.1  
> Purpose: Provide the minimum business context needed to start Business Discovery and AI-friendly project scaffolding.
>
> This document is an external input. It is not a Product Specification, User Story backlog, Acceptance Criteria set, Domain Model, service design, or implementation plan.

---

## How to Use This Template

Complete only what is already known at project initiation.

It is acceptable to write `Unknown`, `To be discovered`, or a short question where information is not yet available. Do not invent detail merely to complete the document.

This template does **not** require the client to define:

- Target Users or Personas;
- User Journeys;
- User Stories;
- Acceptance Criteria;
- Explicit Product Non-goals;
- Domain Model;
- service or deployment architecture;
- APIs, database schema, or integration design;
- technology stack or CI/CD, unless already mandated;
- implementation status or verification evidence.

Those topics should be explored and confirmed later through Business Discovery, Domain Modeling, and Architecture Design.

---

## Protected Handoff Rule

This template may be edited by the client, sponsor, or human project owner while the Project Brief is being prepared.

Once a completed Project Brief is handed to a project Coding Agent together with `AI-FRIENDLY-PROJECT-SCAFFOLD-PROMPT.md`, both documents become protected, immutable project inputs.

A project Coding Agent must never, under any circumstance:

- edit, rewrite, normalize, reformat, rename, move, delete, replace, or overwrite the completed Project Brief;
- add discovery outcomes, User Stories, Acceptance Criteria, architecture decisions, implementation status, or verification evidence to it;
- include it in a bulk formatter, broad search-and-replace, generated-file rewrite, or cleanup operation;
- modify the scaffold prompt supplied with it.

Business Discovery results belong in repository-owned documents such as `SPEC.md`, `ARCHITECTURE.md`, `PROJECT-STATE.md`, and `REVIEW.md`, not in this protected input.

Only the client, sponsor, or human project owner may issue a revised Project Brief outside Coding Agent execution. A revised brief should receive a new version and date. The Coding Agent may record the impact of that externally supplied revision, but may not author or alter the revised brief itself.

---

## Document Information

| Field | Value |
|---|---|
| Project name | `<project name>` |
| Client / organization | `<organization>` |
| Prepared by | `<name or team>` |
| Date | `<YYYY-MM-DD>` |
| Version | `<version>` |
| Handoff status | `draft / final for protected handoff` |
| Primary contact | `<name and contact method, optional>` |

---

## 1. Background and Trigger

Describe the context that caused this project to be considered.

Useful prompts:

- What happened, changed, or became possible?
- Is this driven by a business problem, customer request, regulatory need, operational issue, market opportunity, or strategic initiative?
- Is there an existing process, system, or product involved?

**Current input**

> `<Describe the background and triggering event.>`

---

## 2. Problem or Opportunity Statement

Describe the observed problem or opportunity in business language.

Focus on the situation and its impact rather than a preferred solution.

Useful prompts:

- What is difficult, slow, risky, expensive, inconsistent, or currently impossible?
- What opportunity may be missed if nothing changes?
- What evidence or observations support this statement?
- Which parts are confirmed facts and which are assumptions?

**Current input**

> `<Describe the problem or opportunity. Distinguish facts from assumptions where possible.>`

---

## 3. Initial Objective or Requested Outcome

Describe what the project sponsor currently hopes to achieve or explore.

The objective may remain broad at this stage. It does not need to define a complete feature set.

Useful prompts:

- What outcome would make this initiative worthwhile?
- What decision, capability, improvement, or learning is being requested?
- Is the immediate goal discovery, validation, a prototype, an MVP, modernization, or another outcome?

**Current input**

> `<Describe the initial objective or requested outcome.>`

---

## 4. Why Now / Business Motivation

Explain why the initiative is being considered now.

Useful prompts:

- Is there a deadline, market window, contract, policy change, cost pressure, customer escalation, or strategic priority?
- What is the likely impact of delaying the work?
- Are there dependencies on another initiative or organizational change?

**Current input**

> `<Describe the business motivation and timing.>`

---

## 5. Known Facts and Existing Context

List information already known to be true and relevant to discovery.

Possible examples:

- existing systems or processes;
- current business workflow;
- existing data or reports;
- contractual or regulatory context;
- known organizational ownership;
- previous experiments or solutions;
- current pain-point evidence;
- dependencies on existing products or teams.

Use concise, verifiable statements where possible.

| ID | Known fact or context | Source / evidence | Confidence |
|---|---|---|---|
| KF-001 | `<fact>` | `<document, system, observation, or owner>` | `confirmed / high / medium / low` |
| KF-002 | `<fact>` | `<source>` | `<confidence>` |

---

## 6. Known Constraints

List only constraints already confirmed at project initiation.

Do not turn preferences, assumptions, or proposed solutions into fixed constraints.

Possible categories:

- legal or regulatory;
- contractual;
- budget or timeline;
- organizational ownership;
- data residency or privacy;
- mandatory compatibility;
- required integration with an existing system;
- accessibility or localization obligations;
- explicitly mandated technology or platform, when genuinely fixed.

| ID | Constraint | Reason / source | Fixed or negotiable |
|---|---|---|---|
| KC-001 | `<constraint>` | `<why it exists>` | `fixed / negotiable / unknown` |
| KC-002 | `<constraint>` | `<source>` | `<status>` |

---

## 7. Available Source Materials

List materials that may support Business Discovery or later project work.

Examples:

- current process documents;
- screenshots or prototypes;
- data samples or reports;
- policy or compliance documents;
- existing system documentation;
- research notes;
- customer feedback;
- meeting notes;
- related repositories or products.

| ID | Source material | Location / owner | Notes or access limits |
|---|---|---|---|
| SM-001 | `<document or source>` | `<link, path, or owner>` | `<notes>` |
| SM-002 | `<document or source>` | `<location>` | `<notes>` |

Do not include secrets, credentials, private keys, or unnecessary personal data in this document.

---

## 8. Assumptions, Unknowns, and Discovery Questions

Record what is currently assumed, uncertain, or needs to be discovered.

This is expected to be incomplete and should not be treated as a defect.

### 8.1 Assumptions

| ID | Assumption | Why it is currently believed | How it could be validated |
|---|---|---|---|
| AS-001 | `<assumption>` | `<reason>` | `<possible validation>` |
| AS-002 | `<assumption>` | `<reason>` | `<validation>` |

### 8.2 Unknowns

| ID | Unknown | Why it matters |
|---|---|---|
| UN-001 | `<unknown>` | `<impact on discovery or design>` |
| UN-002 | `<unknown>` | `<impact>` |

### 8.3 Discovery Questions

| ID | Question | Suggested owner or source | Priority |
|---|---|---|---|
| DQ-001 | `<question to answer during discovery>` | `<person, team, data, or workshop>` | `high / medium / low` |
| DQ-002 | `<question>` | `<owner or source>` | `<priority>` |

---

## 9. Additional Notes

Use this optional section for relevant initiation context that does not fit elsewhere.

Do not use it to predefine Personas, User Journeys, User Stories, Acceptance Criteria, Product Non-goals, Domain Models, services, APIs, schemas, or implementation plans unless those items are already explicitly fixed by the client.

> `<Optional notes>`

---

## Handoff Package

When ready, provide the following two files together to the Coding Agent:

```text
PROJECT-BRIEF.md
AI-FRIENDLY-PROJECT-SCAFFOLD-PROMPT.md
```

The Project Brief supplies external business context. The scaffold prompt instructs the Coding Agent how to create and govern the repository documents derived from that context.

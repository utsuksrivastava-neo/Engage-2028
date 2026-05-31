# Engage 2028 - Concepts and Glossary

## Purpose of This Document

This file explains core concepts used across the Engage 2028 mockup so a new contributor can quickly understand terminology and intent.

## Foundational Framing

- Engage 2028 is a **UI/UX mockup project**.
- It is built to validate product concepts and interactions.
- It is **not** a production-ready platform implementation.

## Core Product Concepts

### Engage

An enterprise engagement operating model where AI agents help design, execute, and optimize customer engagement journeys under governance.

### Business Agent

A digital operator focused on a measurable business objective (for example: onboarding completion, repayment recovery, churn prevention, repeat purchase, proactive support resolution).

### Pre-Execution Agent

An agent in setup mode:

- objective and constraints are being clarified,
- journey logic is being designed,
- validation steps are being completed before go-live.

### Running Agent

An agent in active operation mode:

- journey is executing,
- analytics and optimization signals are monitored,
- incremental journey updates are proposed/applied.

### Business Journey

The engagement blueprint the agent creates:

- customer segmentation and targeting logic,
- channel and touchpoint strategy,
- node/step behaviors,
- outcome and fallback paths.

### Execution

The run-time process where approved journeys are orchestrated and delivered through available communication channels and constraints.

### Intelligence and Learning Loop

Outcome data and behavior signals are used to improve subsequent decisions and journey versions.

## Governance and Organization Concepts

### Department

Each agent is assigned to a business department.

Pre-created departments in the mockup:

- Marketing
- Operations
- Sales
- Finance
- Customer Support
- Product
- IT
- HR
- Legal
- Other

### User

A person visible in dashboard user management. Users can be added in the mockup and linked to shared agents.

### Agent Sharing

An agent can be shared with multiple users through dashboard controls.

Current scope:

- lightweight in-memory sharing model,
- no role-permission matrix yet.

## UX-Specific Concepts

### Conversational-First

Chat is the primary interaction surface. Supporting panels/tables are secondary context layers.

### Phase-Gated Progression

In pre-execution flow, planning must be completed before specific downstream controls (for example Business Journey editing) become available.

### Running Tabs

Running agents use two clear top-level tabs:

- Current Analytics
- Update Business Journey

## Technical Scope Concepts

### Mockup-Only Architecture

- Single-page front-end (`index.html`).
- Simulated data/state.
- No backend persistence for business entities.

### Live Demo Publishing

Changes are pushed to GitHub and served via GitHub Pages for interactive review.

## Common Misinterpretations to Avoid

- "This repo is the final Engage system implementation." -> **No** (it is a product mockup/prototype).
- "All data and sharing are production-grade." -> **No** (state is simplified and mostly in-memory).
- "UI copy and flows are finalized." -> **No** (intended for iterative refinement).

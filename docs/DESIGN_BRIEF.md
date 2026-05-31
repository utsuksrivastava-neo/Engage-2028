# Engage 2028 - Design Brief

## 1) Project Title

**Exotel Engage Agents - Conversational Enterprise Engagement Mockup**

## 2) Project Type

This is a **UI/UX concept and interactive mockup project**.

- It is a front-end prototype meant for product/design validation.
- It is not a final production implementation.

## 3) Background

Enterprise engagement teams typically run onboarding, collections, retention, and support workflows across fragmented systems. Current operating models are often manual, rule-heavy, and slow to optimize.

Engage 2028 demonstrates a new operating model:

- AI Business Agents plan and optimize engagement,
- orchestration/execution complexity stays behind the scenes,
- humans supervise, approve, and govern.

## 4) Design Challenge

Create an experience that feels like:

- **"ChatGPT for running customer engagement operations"**

and does **not** feel like:

- a workflow builder,
- a dashboard-heavy CDP,
- a BPM control console.

## 5) Objective

Design a clear, intuitive, conversation-first interface where users can:

- manage multiple business agents,
- move agents from pre-execution planning into running operations,
- review analytics and improvement actions,
- understand and use AI-generated variables,
- collaborate through dashboard and sharing concepts.

## 6) Target Users

- Business operations managers
- Engagement strategy leads
- Product managers for lifecycle engagement
- Supervisors/governance stakeholders
- Demo viewers evaluating UX direction

## 7) Product Concepts to Communicate

The UI must clearly explain these concepts:

- **Engage**: AI-driven engagement operating model
- **Business Agent**: AI operator aligned to business objective
- **Pre-Execution Agent**: planning/configuration state
- **Running Agent**: active execution/optimization state
- **Business Journey**: engagement logic and flow
- **Execution**: orchestration/runtime operations
- **Gen AI Variables**: execution-derived intelligence variables for journey optimization

## 8) Scope of This Brief

### In Scope

- Login and profile interactions for demo access
- Agents dashboard and agent selection
- Department-aligned agent visibility
- Pre-Execution guided phase flow (step-based)
- Running workspace with tabbed views
- Gen AI variables action flow into journey updates
- Business Journey editing entry points
- Documentation-first clarity for newcomers

### Out of Scope

- Production backend, persistence, RBAC, and security hardening
- Final data models/services for enterprise deployment
- Integration with real customer data sources
- Complete design system engineering rollout

## 9) UX Principles

- Conversation-first interactions
- Minimal but meaningful operational context
- Progressive disclosure of complexity
- Clear lifecycle state transitions
- Explainability and trust cues
- Fast comprehension for first-time users

## 10) Key Experience Requirements

- User should quickly understand "what this agent is doing now."
- Pre-Execution must feel guided and sequential.
- Running state must feel analytical and actionable.
- Critical actions must have clear affordances and outcomes.
- All terminology should be business-friendly and consistent.

## 11) Information Architecture (High-Level)

- **Left Sidebar**
  - agent lists by lifecycle (Pre-Execution / Running)
  - quick status and department context

- **Top Action Bar**
  - agents dashboard access
  - business journey access
  - data/context quick links

- **Main Area**
  - conversation thread as primary surface
  - lifecycle-specific side panel/supporting content

- **Dashboard**
  - all agents table
  - department view table

## 12) Functional UX Flows (Priority)

1. Login -> dashboard entry
2. Open pre-execution agent -> complete planning -> move to create journey
3. Open running agent -> switch tabs -> analytics and journey updates
4. Open Gen AI variables -> choose variable -> define usage -> route to update journey
5. Create new agent -> assign department -> enter pre-execution

## 13) Content and Tone

- Professional, concise, operator-friendly
- Explain actions in plain business language
- Avoid deeply technical/internal system jargon in primary UI copy

## 14) Deliverables Expected

- Working browser mockup (`index.html`)
- UX behavior and interaction flows
- Supporting docs:
  - project documentation
  - UI/UX solution design
  - concepts glossary
  - this design brief

## 15) Success Criteria

The design is successful when:

- a new viewer can understand the product concept within minutes,
- lifecycle difference (Pre-Execution vs Running) is obvious,
- key concept of Business Journey is understandable,
- Gen AI variables are actionable and tied to journey updates,
- interface remains conversational and lightweight.

## 16) Constraints and Assumptions

- Mockup-first velocity over production architecture
- Simulated data and in-memory state are acceptable
- GitHub Pages is the publishing medium for demo review

## 17) Future Design Directions (Post-Brief)

- role-aware collaboration (Owner/Editor/Viewer)
- stronger dashboard filtering/search
- richer explainability/audit views
- componentized UI architecture for maintainability

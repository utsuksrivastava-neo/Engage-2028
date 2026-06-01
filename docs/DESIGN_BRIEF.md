# Engage 2028 - Detailed Design Brief

## 1) Project Statement

**Exotel Engage Agents** is a conversation-first enterprise engagement mockup that demonstrates how AI Business Agents can be created, guided, governed, and operated from planning through execution.

This is a **UI/UX prototype**, not a production system.

## 2) Why This Product Exists

Enterprise engagement today is fragmented:

- onboarding, recovery, retention, and support run in separate tools,
- workflows are manually configured and slow to evolve,
- optimization depends on operations and analytics bandwidth.

The design goal is to show a future where:

- AI agents handle planning and optimization,
- humans remain in control of approvals and governance,
- orchestration complexity exists underneath, while UX stays simple.

## 3) Core Design Philosophy (Non-Negotiable)

### 3.1 Conversational, But Structured

This product should **not** be a free-form chat that can go anywhere without progress.

It should be a **structured conversation** where:

- user and agent interact naturally in chat,
- the system guides users through explicit stages and milestones,
- users always know:
  - where they are,
  - what is next,
  - what is required to continue.

In short:

- not a static form,
- not a random chat thread,
- a guided conversational workflow with stage awareness.

### 3.2 Explainability by Design

The user must understand:

- why the agent asks a specific question,
- why a journey or variable is recommended,
- what changes when an action is applied.

### 3.3 Operational Confidence

The system must feel trustworthy for enterprise operations:

- clear lifecycle states,
- explicit action outcomes,
- policy-aware gating for sensitive actions.

## 4) What This Experience Should Feel Like

### Should feel like

- ChatGPT/Claude-level conversational simplicity
- AI operating partner for engagement teams
- Fast, guided, clear, and outcome-oriented

### Should not feel like

- drag-and-drop workflow builder as primary UX
- dashboard-only enterprise reporting console
- BPM-style process administration tool

## 5) Product Concepts to Communicate Clearly

- **Engage**: AI-driven engagement operating model
- **Business Agent**: function-specific AI operator
- **Pre-Execution Agent**: setup/planning state
- **Running Agent**: live execution and optimization state
- **Business Journey**: engagement plan/logic created by the agent
- **Execution**: runtime orchestration of journeys
- **Gen AI Variables**: automatically detected intelligence variables from execution data

## 6) User Personas

### Persona A - Operations Manager (Primary)

- Owns daily outcomes (completion, recovery, retention, support prevention)
- Needs fast guided setup and confidence before go-live
- Values clear next-step recommendations

### Persona B - Engagement Strategist

- Optimizes journeys and channel strategy
- Wants structured planning inputs and milestone-based progression
- Needs explainable recommendations and testing confidence

### Persona C - Governance/Approver

- Reviews readiness and operational risk
- Needs clear lifecycle states and reasoned decisions
- Cares about policy alignment and rollout control

## 7) Information Architecture

### 7.1 Entry View

- Initial dashboard for portfolio visibility:
  - all agents
  - department view

### 7.2 Left Navigation

- agents grouped by:
  - Pre-Execution
  - Running
- each item provides quick state context

### 7.3 Workspace

- top actions (`Agents Dashboard`, `Business Journey`, `Data Sources`, `Business Channels`)
- main chat pane as primary interaction surface
- lifecycle-specific supporting panel/tabs

## 8) Lifecycle Design Requirements

## 8.1 Pre-Execution Lifecycle

Pre-Execution must guide users through explicit, visible phases:

1. Planning
2. Create Business Journey (without node-level configs)
3. Business Journey Node Configuration
4. Test Business Journey
5. Execution Checks and Validation
6. Go Live

Each phase has milestones/modules. Conversation drives progress, but progression remains explicit.

## 8.2 Running Lifecycle

Running agents provide operational tabs:

- Current Analytics
- Update Business Journey
- Gen AI Variables

## 9) Structured Conversation Flow Requirement

For pre-execution setup, the agent must:

- ask focused milestone-specific questions,
- accept responses in guided sequence,
- confirm completion of each milestone,
- move user to next milestone/phase with clear transition messaging.

The user should be able to progress by selecting recommended responses (demo mode), while still retaining ability to type free text.

## 10) Why We Chose This Structure (Decision Rationale)

### Decision: stage-based structure over pure free chat

**Why**:

- enterprise users need predictable progression,
- teams need clear readiness signals before go-live,
- governance requires stage-level visibility.

### Decision: chat as primary interaction, not forms

**Why**:

- lowers friction and cognitive load,
- preserves natural decision-making context,
- keeps AI reasoning and actions in one place.

### Decision: gated actions (for example Business Journey access)

**Why**:

- enforces process integrity,
- prevents premature editing without required planning context,
- improves trust and auditability in enterprise settings.

### Decision: running tab model

**Why**:

- separates monitoring from modification,
- reduces mixed-context confusion,
- supports task-focused operator behavior.

## 11) Sample Journey (Detailed) - Onboarding Assist Agent

### Phase 1: Planning

Milestones:

- Objective clarification
- Audience/data source capture
- Channel pre-check

Conversation outcomes expected:

- objective and KPI target defined,
- source identified (for example registration form + onboarding events),
- allowed communication channels confirmed.

Transition behavior:

- after planning completion, user gets clear progression cue,
- UI shows loading/transition state,
- user advances to Phase 2.

### Phase 2: Create Business Journey

- create logical journey scaffold without full node-level parameters,
- define branches and expected outcomes.

### Phase 3: Configure Nodes

- configure trigger/action/process/end nodes,
- set channel and retry behavior.

### Phase 4: Test

- run core scenario tests (happy path/fallback/failure path).

### Phase 5: Validate Execution

- run readiness checks and confidence checks.

### Phase 6: Go Live

- approval and rollout transition.

## 12) Sample Running Journey Behavior

For a running agent:

- `Current Analytics` gives live/historical performance,
- `Update Business Journey` applies optimization updates,
- `Gen AI Variables` presents detected variables with actionable usage in journey updates.

Gen AI Variable UX requirement:

- table with variable name, description, and action,
- action includes usage instruction input,
- applying variable routes to journey update flow.

## 13) UX Writing and Tone Requirements

- concise, professional, operationally clear
- no unnecessary technical jargon in primary copy
- every gated/blocked action must explain:
  - why blocked
  - what to do next

## 14) Scope Boundaries

### In Scope

- interactive front-end mockup
- guided lifecycle UX
- dashboard and department concepts
- conversation-first step progression

### Out of Scope

- backend and persistent data architecture
- security/RBAC hardening
- production orchestration infrastructure

## 15) Deliverables

- interactive prototype (`index.html`)
- supporting docs:
  - concepts glossary
  - project documentation
  - UI/UX solution design
  - this detailed design brief

## 16) Success Criteria

This design is successful when a new viewer can:

- understand product concept in < 5 minutes,
- distinguish Pre-Execution vs Running states immediately,
- progress through setup in clear staged sequence,
- understand why recommendations/actions are shown,
- trust that the experience is conversational **and** structured.

## 17) Validation Checklist for Future Iterations

For each UX change, validate:

- does this preserve structured conversational progression?
- is stage/milestone status visible and unambiguous?
- is the next step obvious?
- does action feedback explain outcome and reason?
- does this still feel lightweight, not dashboard-heavy?

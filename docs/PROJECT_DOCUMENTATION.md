# Engage 2028 - Project Documentation

## 1) Project Overview

Engage 2028 is a single-page, white-theme, conversational UI demo for AI-powered enterprise engagement operations.

The core UX goal is:

- feel like ChatGPT/Claude/Cursor for operations teams,
- keep orchestration complexity in the background,
- avoid looking like a workflow-builder-heavy enterprise dashboard.

This is intentionally a **working mockup** (front-end only) with realistic interaction flows and simulated operational data.

## 2) Product Intent and Positioning

The product vision represented in this demo:

- businesses configure persistent AI Business Agents aligned to functions (onboarding, collections/recovery, churn prevention, repeat purchase, proactive resolution),
- AI handles planning + execution recommendations + optimization loops,
- humans supervise governance, approvals, and outcomes.

The demo models two lifecycle states:

- **Pre-Execution Agents**: journey is being designed and validated.
- **Running Agents**: journey is active and continuously optimized.

## 3) Current Tech Stack

- **Single file app**: `index.html`
  - HTML structure
  - CSS styling
  - JavaScript state and behavior
- **No backend** (simulated data and in-memory state)
- **Auth state** persisted in `localStorage`
- **Optional voice input** via Web Speech API (`SpeechRecognition`)
- **Deployment target**: GitHub Pages

## 4) Repository Structure

- `index.html` - full application
- `README.md` - short project intro
- `docs/PROJECT_DOCUMENTATION.md` - this document
- `docs/UI_UX_SOLUTION_DESIGN.md` - UI/UX solution design document

## 5) Core Functional Areas

### 5.1 Authentication and Session

- Demo credentials shown on sign-in page.
- Login/Logout supported.
- Session persisted via `AUTH_STORAGE_KEY`.

### 5.2 Agents Dashboard (Initial Landing)

After login, users land on an **Agents Dashboard** with:

- all agents table view,
- users and sharing management,
- department-level summary view,
- open action for each agent.

### 5.3 Agent Workspace

Selecting an agent opens the workspace:

- top action row (`Business Journey`, `Data Sources`, `Business Channels`, etc.),
- lifecycle-driven content:
  - Pre-Execution: phased setup flow,
  - Running: tabbed operational view.

### 5.4 Pre-Execution Studio

- 6 major phases with modules.
- Guided input collection where the agent prompts the user.
- Progress shown as `Step X/6`.
- Planning completion gate:
  - `Business Journey` stays locked until planning is complete,
  - clicking early shows explanatory popup.
- Automatic animated transition:
  - after planning inputs complete, agent shows loader + moves user to Step 2.

### 5.5 Running Agent Workspace

Two tabs are shown in top strip:

- `Current Analytics`
- `Update Business Journey`

Right panel includes:

- current/historical execution,
- recommended sessions,
- journey update actions,
- data lake preview and export.

### 5.6 Business Journey Editing

- Manual editor opened via `Business Journey`.
- In-chat relevant snippet cards show focused updates.
- Apply changes flow includes effective date messaging.

### 5.7 Multimodal Composer

- text input,
- attachment support,
- mic/voice capture support.

## 6) Data Model (In-App State)

Primary in-memory structures include:

- `AGENTS` - all agents and metadata.
- `USERS` - user records for dashboard management.
- `AGENT_SHARES` - per-agent shared user IDs.
- `DEPARTMENTS` - pre-created enterprise departments (+ `Other`).
- `RUNNING_DATA` - current/historical/sessions/datalake content for running agents.
- `currentPhaseByAgent`, `currentModuleByAgent`, `guidedFlowByAgent` - pre-execution progression.
- `currentRunningTabByAgent` - selected running tab per agent.
- `journeyByAgent`, `selectedNodeByAgent` - journey editor state.

## 7) Departments and Ownership

Departments are pre-created and every agent belongs to one:

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

Rules implemented:

- each agent must have a department,
- unknown/blank values normalize to `Other`,
- create-agent flow uses a department dropdown.

## 8) Naming and Lifecycle Disambiguation

Because one logical agent should not appear as the same instance in two lifecycle states, seeded agents with same base use-case are disambiguated by numbering:

- `... Agent 1` for pre-execution,
- `... Agent 2` for running.

## 9) User and Sharing Model

Implemented capabilities:

- add users from dashboard,
- share an agent with selected users,
- remove shared users,
- owner shown per agent.

Current scope:

- in-memory only (not persisted to backend),
- no role hierarchy yet (Owner/Editor/Viewer not yet modeled).

## 10) UI Principles Applied

- conversational-first experience,
- minimal operational chrome around chat,
- progressive reveal of complexity,
- consistency across lifecycle stages,
- clear naming aligned to business terms,
- lightweight explainability in flow.

## 11) Deployment and Publishing

Current workflow:

1. Edit `index.html`.
2. Commit and push to `main`.
3. GitHub Pages auto-builds.
4. Live demo URL updates after build completes.

Live URL:

- https://utsuksrivastava-neo.github.io/Engage-2028/

## 12) Known Constraints

- Single-file app can grow hard to maintain as complexity increases.
- No backend persistence (reload resets in-memory entities except auth localStorage).
- No server-side access control or real multi-user concurrency.
- Analytics and execution telemetry are simulated.

## 13) Suggested Next Improvements

- split code into modular files (`/src` structure),
- add persistent storage (API + DB),
- add role-based sharing permissions,
- add department filters/search/sorting in dashboard tables,
- add audit trail for agent changes and sharing actions,
- add test coverage for key UI flows.

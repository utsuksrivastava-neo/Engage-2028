# Engage 2028

Conversational UI/UX mockup for AI-powered customer engagement operations — "ChatGPT for running customer engagement operations."

## Important Project Scope

This repository is a **design and interaction mockup project**, not a production-ready application.

What this project is:

- a working front-end prototype to validate UX concepts,
- a demonstration of agent lifecycle flows and enterprise operating model ideas,
- a communication artifact for product/design/strategy iteration.

What this project is not:

- not a final production system,
- not backend-complete or security-hardened,
- not intended as a deployment blueprint for enterprise runtime.

## Live Demo

Open `index.html` in a browser, or use GitHub Pages once published.

## Core Concepts in This Project

- **Engage**: the overall AI-led engagement operating model for enterprise teams.
- **Business Agent**: an AI operator aligned to a business function (for example onboarding, recovery, retention).
- **Pre-Execution Agent**: agent whose journey is still being designed/validated.
- **Running Agent**: agent with an active journey under execution/optimization.
- **Business Journey**: the engagement plan/logic designed by the agent.
- **Execution**: orchestration and run-time operation of approved journeys.
- **Department ownership**: each agent belongs to a department (Marketing, Operations, Sales, Finance, etc.).
- **Sharing model**: agents can be shared across multiple users in dashboard controls.

## Current UX Capabilities

- **Initial Agents Dashboard** with:
  - all agents table,
  - users management,
  - agent sharing controls,
  - department summary view.
- **Pre-Execution studio** with phased setup, guided Q&A, and planning-to-build transitions.
- **Running workspace** with visible tabs (`Current Analytics`, `Update Business Journey`).
- **Business Journey editor** with gated availability and in-chat update context.
- **Multimodal composer** (text, attachment, voice).

## Usage

```bash
open index.html
```

1. Sign in with demo credentials shown on screen.
2. Start in the dashboard.
3. Open any agent and explore lifecycle-specific flows.
4. Use `Create New Business Agent` to test create flow with department dropdown.

## Documentation

- `docs/PROJECT_DOCUMENTATION.md` - full implementation documentation (architecture + behavior)
- `docs/UI_UX_SOLUTION_DESIGN.md` - UI/UX solution design and interaction rationale
- `docs/CONCEPTS_AND_GLOSSARY.md` - concept definitions for new contributors/stakeholders

## Recommended Read Order for New Contributors

1. `README.md` (scope + quick orientation)
2. `docs/CONCEPTS_AND_GLOSSARY.md` (terminology)
3. `docs/UI_UX_SOLUTION_DESIGN.md` (why UX is designed this way)
4. `docs/PROJECT_DOCUMENTATION.md` (what is implemented and how)

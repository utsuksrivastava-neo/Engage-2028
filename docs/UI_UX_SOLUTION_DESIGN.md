# Engage 2028 - UI/UX Solution Design Document

## 1) Design Objective

Design a conversational enterprise engagement product that feels like an AI operating partner, not a heavy enterprise control center.

Primary UX statement:

- **"Chat-first AI for running customer engagement operations."**

## 2) Design Principles

### 2.1 Conversational First

- Chat is the primary control surface.
- Operational widgets support the conversation, not replace it.

### 2.2 Minimal Enterprise Friction

- White, clean visual language.
- Compact components with clear hierarchy.
- Avoid workflow-canvas-first framing for day-to-day use.

### 2.3 Lifecycle Clarity

- Distinct user mental model for Pre-Execution vs Running.
- State-specific actions and tab structures.

### 2.4 Explainability and Trust

- Visible rationale prompts,
- contextual journey update snippets,
- transparent transition and status messaging.

### 2.5 Progressive Disclosure

- advanced controls open only when relevant,
- locked actions explained with contextual messaging.

## 3) Information Architecture

## 3.1 Global Layout

- Left sidebar: agent inventory + quick management entry.
- Top action bar: context actions (`Business Journey`, data links, dashboard).
- Main workspace: chat + contextual operational panel.

### 3.2 Entry Point

- Initial landing after login: **Agents Dashboard**.
- Dashboard acts as "single pane" for:
  - all agents,
  - department view,
  - users and sharing.

### 3.3 Agent Workspace Modes

- **Pre-Execution mode**
  - phase tabs + module cards,
  - guided question flow,
  - planning progression.

- **Running mode**
  - top-strip tabs:
    - Current Analytics
    - Update Business Journey
  - right-side detail panels for execution and updates.

## 4) Key Interaction Flows

### 4.1 Create Agent Flow

1. Click `Create New Business Agent`.
2. Modal opens with:
   - Agent Name
   - Department dropdown
3. Create agent.
4. User lands in new agent’s pre-execution workspace.

### 4.2 Planning Gate for Business Journey

1. User clicks `Business Journey` during incomplete planning.
2. System shows blocking explanation popup.
3. After all planning inputs complete:
   - agent announces transition,
   - loader animation appears,
   - auto-move to Step 2 (`Create Business Journey`).

### 4.3 Dashboard Open-Agent Flow

1. User lands on dashboard.
2. Reviews agents in table.
3. Clicks `Open` for target agent.
4. Enters lifecycle-specific workspace.

### 4.4 Sharing Flow

1. Add user from Users panel.
2. In agent row, select user from share dropdown.
3. Click `Share`.
4. Shared user chip appears; can remove with `×`.

## 5) Component Design

### 5.1 Sidebar Agent Card

- title,
- lifecycle/step context,
- department cue,
- compact, scan-friendly.

### 5.2 Phase and Running Tabs

- same visual system for familiarity,
- active state with clear highlight and index.

### 5.3 Dashboard Tables

- lightweight bordered table style,
- consistent heading style,
- clear action affordances.

### 5.4 Modal Forms

- resource modal pattern reused for consistency,
- focused create-agent modal with explicit form controls.

## 6) State Design

### 6.1 Lifecycle States

- Pre-Execution
- Running

### 6.2 Availability States

- Business Journey locked/unlocked by planning completion.

### 6.3 Running Workstream States

- Current Analytics tab active/inactive.
- Update Business Journey tab active/inactive.

### 6.4 Sharing States

- not shared,
- shared with N users,
- removable share chips.

## 7) Content and Naming Decisions

- Removed internal "Type 1 / Type 2" terms.
- Standardized product-facing terminology:
  - Pre-Execution Agents
  - Running Agents
- Renamed action label to `Business Journey`.
- Simplified phase names by removing unnecessary "Agent(s)" wording.

## 8) Visual Design Direction

- White background system with subtle blue accents.
- Light borders and rounded corners for enterprise readability.
- Moderate density optimized for operation teams.
- Minimal icon usage, meaningful where needed (e.g., Business Journey).

## 9) Accessibility and Usability Considerations

- Sufficient contrast for text and controls in light theme.
- Predictable keyboard submit on key forms/inputs.
- Explicit empty-state text in operational lists.
- Clear textual feedback for blocked or gated actions.

## 10) Risks and Gaps

- Very large single-page file can reduce maintainability and velocity.
- No persistent backend for users/shares/agents.
- No advanced filtering/search/sort in dashboard yet.
- No per-user role permissions in sharing model.

## 11) UX Roadmap Recommendations

### Near-Term

- add dashboard filters (department, lifecycle, owner),
- add search and sortable columns,
- add role-based sharing (Owner/Editor/Viewer),
- add toast notifications for create/share/remove events.

### Mid-Term

- unify modal and form primitives into design tokens,
- add responsive optimizations for narrower screens,
- instrument key UX telemetry (task completion, drop-offs).

### Long-Term

- migrate to componentized architecture (React/Vue/etc.),
- implement backend persistence and true multi-user model,
- add auditability and governance workflows for enterprise rollout.

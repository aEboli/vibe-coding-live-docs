# Update Matrix

Use this file when you need a precise answer to "what should I update now?"

## Milestone Triggers

| Trigger | Must update | What to confirm |
| --- | --- | --- |
| Project start | `PRD.md`, `ARCHITECTURE.md`, `PROJECT_STATE.md` | Draft skeleton, open questions, first doc debt list |
| First runnable version | `PROJECT_STATE.md`, `ARCHITECTURE.md`, `PAGE_FRAME.md` if applicable, `TECH_DECISIONS.md` if applicable | Real pages, real stack, first core modules |
| Core flow stable | `PRD.md`, `ARCHITECTURE.md`, `PROJECT_STATE.md` | Acceptance, module duties, data flow, frozen decisions |
| Release prep | `PRD.md`, `ARCHITECTURE.md`, `PROJECT_STATE.md`, `QUALITY_GATE.md` in project docs | As-Built delta, shipped structure, remaining risks |

## Event Triggers

| Event | Must update | Typical reason |
| --- | --- | --- |
| Stack locked | `TECH_DECISIONS.md`, `ARCHITECTURE.md`, `PROJECT_STATE.md` | Candidate becomes current truth |
| Page frame locked | `PAGE_FRAME.md`, `PRD.md`, `PROJECT_STATE.md` | Navigation and page structure stop drifting |
| Module boundary changed | `ARCHITECTURE.md`, `PROJECT_STATE.md` | Real code moved responsibility |
| Auth or data flow changed | `ARCHITECTURE.md`, `TECH_DECISIONS.md`, `PROJECT_STATE.md` | Security and integration assumptions changed |
| Third-party dependency chosen or replaced | `TECH_DECISIONS.md`, `ARCHITECTURE.md` | Reasoning and impact need to stay discoverable |

## Repair Flow For Existing Projects

Use this order when the project already exists and the docs are incomplete:

1. Recover current truth into `PROJECT_STATE.md`.
2. Rebuild `ARCHITECTURE.md` from the actual code path, not old assumptions.
3. Rebuild `PAGE_FRAME.md` from current screens or routes if UI exists.
4. Rewrite `PRD.md` acceptance around the product that is actually being delivered.
5. Capture missing decision history in `TECH_DECISIONS.md` only when it still helps future work.

## Minimal Rule For Small Tasks

Small tasks may stay lightweight, but if any of these move, promote the task into doc updates:

- Page frame changed
- Stack choice changed
- Module boundary changed
- Auth, permission, or data flow changed
- Release expectations changed

---
name: vibe-coding-live-docs
description: Use when starting a new project or large feature, or when project docs have drifted, and Codex needs to scaffold, update, or repair living documents such as PRD, architecture, page frame, tech decisions, and project state without freezing technical details too early.
---

# Vibe Coding Live Docs

## Overview

Keep project docs alive from the first sketch to the shipped system. This skill turns PRD, architecture, page structure, decisions, and state tracking into living artifacts that move through `Draft`, `Confirmed`, and `As-Built` instead of becoming abandoned setup docs.

## Quick Start

- Create `project-docs/PRD.md`, `project-docs/ARCHITECTURE.md`, and `project-docs/PROJECT_STATE.md` as `Draft` skeletons at project start.
- For UI or multi-page work, also create `project-docs/PAGE_FRAME.md`.
- For non-trivial stack choices, also create `project-docs/TECH_DECISIONS.md`.
- Use `project-docs/PROJECT_STATE.md` as the document-sync control tower: track doc debt, latest confirmations, next refill node, and frozen decisions.
- Update docs on milestones and key events instead of waiting until release.

## Lifecycle

- `Draft`
  - Use for hypotheses, placeholders, candidate stack choices, page sketches, and open questions.
- `Confirmed`
  - Use after the first runnable version or when major decisions are stable enough to guide implementation.
- `As-Built`
  - Use before release or handoff to record what actually shipped, what changed, and what risk remains.

## Trigger Matrix

Update the right docs when these triggers happen:

- Milestones
  - Project start
  - First runnable version
  - Core flow stable
  - Release prep
- Events
  - Stack locked
  - Page frame locked
  - Module boundary changed
  - Auth or data flow changed
  - Third-party dependency chosen or replaced

## Document Contract

- `project-docs/PRD.md`
  - Product intent, user journeys, acceptance, page summary
- `project-docs/ARCHITECTURE.md`
  - Current architecture, modules, data flow, auth, and as-built structure
- `project-docs/PROJECT_STATE.md`
  - Current slice, document debt, next update node, frozen decisions
- `project-docs/PAGE_FRAME.md`
  - Page inventory, navigation, key states, transitions
- `project-docs/TECH_DECISIONS.md`
  - Chosen options, rejected options, constraints, decision dates

## Workflow

1. Detect whether the task is a new project, a large feature, or a drifting documentation cleanup.
2. Create or repair the minimum living-doc skeleton first.
3. Put uncertain information in `Draft` instead of pretending it is final.
4. Promote sections to `Confirmed` when real implementation or decisions stabilize them.
5. Promote key docs to `As-Built` before release, handoff, or major milestone closeout.
6. Keep decision history in `project-docs/TECH_DECISIONS.md` and UI structure in `project-docs/PAGE_FRAME.md` so `project-docs/PRD.md` and `project-docs/ARCHITECTURE.md` stay readable.

## Resources

Read only what you need:

- `references/living-docs-playbook.md`
  - Full doctrine, lifecycle, and document ownership model
- `references/update-matrix.md`
  - What to update at each milestone and event
- `assets/templates/`
  - Starter templates for all core docs and appendices

## Common Mistakes

- Writing every detail too early and never revisiting it
- Leaving page or stack decisions only in chat history
- Updating only `PROJECT_STATE.md` when architecture or page structure changes
- Treating `Draft` as shameful instead of intentional
- Waiting until release to reconstruct docs from memory

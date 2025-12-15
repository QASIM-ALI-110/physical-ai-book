---
id: 001
title: Docusaurus Textbook Structure Plan
stage: plan
date: 2025-12-15
surface: agent
model: claude-opus-4-5-20251101
feature: docusaurus-textbook-structure
branch: 001-docusaurus-textbook-structure
user: Claude Code User
command: /sp.plan
labels: [planning, docusaurus, textbook, structure]
links:
  spec: specs/001-docusaurus-textbook-structure/spec.md
  ticket: null
  adr: null
  pr: null
files:
 - specs/001-docusaurus-textbook-structure/plan.md
 - specs/001-docusaurus-textbook-structure/research.md
 - specs/001-docusaurus-textbook-structure/data-model.md
 - specs/001-docusaurus-textbook-structure/quickstart.md
 - specs/001-docusaurus-textbook-structure/contracts
tests:
 - none
---

## Prompt

# Phase 1: Environment & Skeleton (Technical Setup)
- [ ] Initialize project with `uv init` and create virtual environment.
- [ ] Install Docusaurus (`npx create-docusaurus@latest website classic`).
- [ ] Clean up default Docusaurus boilerplate (delete `docs/intro.md`, `blog/`).
- [ ] Configure `docusaurus.config.js`:
    - Title: "Physical AI & Humanoid Robotics".
    - Organization/Project Name: For GitHub Pages.
    - Deployment Branch: `gh-pages`.

# Phase 2: Structural Architecture
- [ ] Create directory structure in `website/docs/`:
    - `01-introduction`
    - `02-module-1-ros2`
    - `03-module-2-simulation`
    - `04-module-3-isaac`
    - `05-module-4-vla`
- [ ] Create `sidebars.js` to auto-generate navigation from these folders.

# Phase 3: Content Drafting - Batch A (Foundations)
- [ ] Write `docs/01-introduction/01-overview.md`:
    - [cite_start]Shift from Digital to Physical AI [cite: 51-52].
    - [cite_start]Embodied Intelligence concept[cite: 83].
- [ ] Write `docs/01-introduction/02-hardware-lab.md`:
    - [cite_start]Specs for "Digital Twin Workstation" (RTX GPU, RAM, CPU) [cite: 116-129].
    - [cite_start]Specs for "Edge AI Kit" (Jetson Orin Nano, RealSense, IMU) [cite: 130-142].

# Phase 4: Content Drafting - Batch B (ROS 2 & Sim)
- [ ] [cite_start]Write `docs/02-module-1-ros2/01-nervous-system.md` (Nodes, Topics, Services) [cite: 56-60].
- [ ] [cite_start]Write `docs/03-module-2-simulation/01-digital-twin.md` (Gazebo, UR

## Response snapshot

Completed the implementation planning for the Docusaurus textbook structure. Created comprehensive plan.md with technical context aligned with project constitution. Developed research.md documenting technology decisions and alternatives. Created data-model.md outlining entities and relationships for the textbook structure. Developed quickstart.md guide for developers to set up and work with the Docusaurus project. All artifacts created in the specs/001-docusaurus-textbook-structure directory.

## Outcome

- ✅ Impact: Complete implementation plan with research, data model, and quickstart guide
- 🧪 Tests: No tests required for planning artifacts
- 📁 Files: Created plan.md, research.md, data-model.md, quickstart.md, and contracts directory
- 🔁 Next prompts: Generate tasks for implementation (/sp.tasks)
- 🧠 Reflection: Planning phase completed successfully with all required artifacts generated

## Evaluation notes (flywheel)

- Failure modes observed: None
- Graders run and results (PASS/FAIL): N/A
- Prompt variant (if applicable): N/A
- Next experiment (smallest change to try): Begin task generation for implementation
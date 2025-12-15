---
id: 001
title: Docusaurus Textbook Structure Spec
stage: spec
date: 2025-12-15
surface: agent
model: claude-opus-4-5-20251101
feature: docusaurus-textbook-structure
branch: 001-docusaurus-textbook-structure
user: Claude Code User
command: /sp.specify
labels: [specification, docusaurus, textbook, structure]
links:
  spec: specs/001-docusaurus-textbook-structure/spec.md
  ticket: null
  adr: null
  pr: null
files:
 - specs/001-docusaurus-textbook-structure/spec.md
 - specs/001-docusaurus-textbook-structure/checklists/requirements.md
tests:
 - none
---

## Prompt

# Project Identity
- **Name:** Physical AI & Humanoid Robotics Textbook
- **Type:** Static Site Generator (SSG) / Technical Documentation
- **Stack:** Docusaurus 3.x (Classic Theme), React, Node.js.
- **Package Manager:** npm (Frontend), uv (Backend/Scripts).

# Clean Code & Architecture Standards
1.  **File Naming Convention:** All documentation files must use `kebab-case` (e.g., `01-intro-to-physical-ai.md`).
2.  **Directory Structure:** Strictly hierarchical. Do not dump all files in root.
    -   `docs/01-introduction/`
    -   `docs/02-module-1-ros2/`
    -   `docs/03-module-2-simulation/`
    -   `docs/04-module-3-isaac/`
    -   `docs/05-module-4-vla/`
3.  **Frontmatter Consistency:** Every Markdown file MUST include:
    -   `VLA (Vision-Language-Action) models.
    -   Final Project: "The Autonomous Humanoid".

# UI/UX Requirements
1.  **Navigation:** Auto-generating sidebar based on folder structure.
2.  **Admonitions:** Use Docusaurus Admonitions (`:::note`, `:::warning`) for Hardware constraints and Safety tips.
3.  **Code Blocks:** All code snippets must specify the language (e.g., ```python, ```bash) and include a title if it refers to a specific file (e.g., `package.xml`).

# Deployment Strategy
-   **Platform:** GitHub Pages.
-   **Workflow:** GitHub Actions (`.github/workflows/deploy.yml`).
-   **Base URL:** Configure correctly for GitHub Pages subdirectory hosting.

## Response snapshot

Created the feature specification for the Docusaurus textbook structure, defining user stories for students, instructors, and developers. The spec outlines requirements for hierarchical content organization, naming conventions, navigation, frontmatter metadata, and deployment strategy. Created with 3 user stories prioritized by importance, functional requirements, and measurable success criteria aligned with the Physical AI & Humanoid Robotics constitution.

## Outcome

- ✅ Impact: Complete specification for textbook structure with user scenarios, requirements, and success criteria
- 🧪 Tests: No tests required for specification creation
- 📁 Files: Created spec.md and requirements checklist
- 🔁 Next prompts: Plan implementation of Docusaurus structure (/sp.plan)
- 🧠 Reflection: Specification captures all essential elements for textbook structure while maintaining focus on user needs

## Evaluation notes (flywheel)

- Failure modes observed: None
- Graders run and results (PASS/FAIL): N/A
- Prompt variant (if applicable): N/A
- Next experiment (smallest change to try): Begin implementation planning based on this specification
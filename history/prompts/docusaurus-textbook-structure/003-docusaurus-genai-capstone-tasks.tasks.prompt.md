---
id: 003
title: Docusaurus GenAI Capstone Tasks
stage: tasks
date: 2025-12-15
surface: agent
model: claude-opus-4-5-20251101
feature: docusaurus-textbook-structure
branch: 001-docusaurus-textbook-structure
user: Claude Code User
command: /sp.tasks
labels: [tasks, docusaurus, textbook, content, vla, genai, capstone, deployment]
links:
  spec: specs/001-docusaurus-textbook-structure/spec.md
  ticket: null
  adr: null
  pr: null
files:
 - specs/001-docusaurus-textbook-structure/tasks.md
tests:
 - none
---

## Prompt

# Phase 5: Content Drafting - Batch C (GenAI & Capstone)

- [ ] **Task 5.1: Populate Module 4 (Vision-Language-Action)**
  - [cite_start]**Context:** The convergence of LLMs and Robotics[cite: 74].
  - **Action:** Create `website/docs/05-module-4-vla/01-generative-robotics.md`.
  - **Content Requirements:**
    - [cite_start]**Voice-to-Action:** Explain using OpenAI Whisper for capturing voice commands[cite: 76].
    - [cite_start]**Cognitive Planning:** Explain how LLMs (like GPT-4) translate natural language (e.g., "Clean the room") into a sequence of ROS 2 actions (Cognitive Planning) [cite: 77-78].
    - **VLA Models:** Briefly explain Vision-Language-Action models.

- [ ] **Task 5.2: The Capstone Project**
  - **Action:** Create `website/docs/06-capstone/01-autonomous-humanoid.md`.
  - **Content Requirements:**
    - [cite_start]**Project Goal:** Build a simulated robot that receives a voice command, plans a path, identifies an object using computer vision, and manipulates it[cite: 79].
    - **Workflow Diagram:** Describe the flow: `User Voice -> Whisper -> LLM Planner -> ROS 2 Nav2 -> Robot Action`.

# Phase 6: Deployment Infrastructure

- [ ] **Task 6.1: Create Professional Landing Page**
  - **Action:** Create a new `website/src/pages/index.js`.
  - **Design:** Use a clean React component layout.
  - [cite_start]**Header:** Title "Physical AI & Humanoid Robotics", Subtitle "The partnership between people, intelligent agents, and robots"[cite: 2].
  - **Call to Action:** A button saying "Start Learning" linking to `/docs/introduction/future-of-work`.

- [ ] **Task 6.2: Setup GitHub Actions Workflow**
  - **Action:** Create file `.github/workflows/deploy.yml` in the root directory (outside `website`).
  - **Content:** Use the standard Docusaurus deployment workflow:
    - **Trigger:** Push to `main` branch.
    - **Job:** Checkout repo, setup Node, `npm install`, `npm run build`

## Response snapshot

Updated the existing tasks.md file to include Phase 7: Content Drafting - Batch C (GenAI & Capstone) and Phase 8: Deployment Infrastructure. Added 14 new tasks (T068-T080) with proper formatting and story labels. Phase 7 focuses on creating content for Module 4 (Vision-Language-Action) and the Capstone project, explaining the convergence of LLMs and robotics. Phase 8 covers creating a professional landing page and GitHub Actions workflow for automated deployment. Tasks include creating content files, explaining AI/robotics integration concepts, and implementing deployment infrastructure.

## Outcome

- ✅ Impact: Extended task list with detailed content creation for GenAI/robotics integration and deployment infrastructure
- 🧪 Tests: No additional tests required for content drafting and deployment
- 📁 Files: Updated tasks.md with new content drafting and deployment phases
- 🔁 Next prompts: Begin implementation of GenAI content drafting and deployment tasks
- 🧠 Reflection: Tasks properly organized under appropriate user stories with clear goals and checkpoints

## Evaluation notes (flywheel)

- Failure modes observed: None
- Graders run and results (PASS/FAIL): N/A
- Prompt variant (if applicable): Extension of existing task list
- Next experiment (smallest change to try): Execute first GenAI content drafting task
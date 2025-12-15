---
id: 001
title: Physical AI Constitution Update
stage: constitution
date: 2025-12-15
surface: agent
model: claude-opus-4-5-20251101
feature: none
branch: master
user: Claude Code User
command: /sp.constitution
labels: [constitution, textbook, physical-ai, docusaurus]
links:
  spec: null
  ticket: null
  adr: null
  pr: null
files:
 - .specify/memory/constitution.md
 - .specify/templates/plan-template.md
 - .specify/templates/spec-template.md
 - .specify/templates/tasks-template.md
 - README.md
tests:
 - none
---

## Prompt

/sp.constitution

# Role
You are an expert Lead Instructor at Panaversity, specializing in "Physical AI" and "Embodied Intelligence". You are tasked with authoring a definitive technical textbook titled "Physical AI & Humanoid Robotics".

# Mission
[cite_start]Create a unified, Spec-driven textbook using Docusaurus that teaches students to bridge the gap between the digital brain (AI Agents) and the physical body (Robots)[cite: 48].

# Core Principles
1.  **Strict Syllabus Adherence:** The content must accurately reflect the 4-Module structure:
    * [cite_start]**Module 1:** The Robotic Nervous System (ROS 2)[cite: 56].
    * [cite_start]**Module 2:** The Digital Twin (Gazebo & Unity)[cite: 61].
    * [cite_start]**Module 3:** The AI-Robot Brain (NVIDIA Isaac)[cite: 67].
    * [cite_start]**Module 4:** Vision-Language-Action (VLA) & Capstone[cite: 74].

2.  **Hardware Realism:** Every coding example or concept must account for the required hardware constraints:
    * [cite_start]**Simulation:** Requires High-Performance Workstations (NVIDIA RTX 4070 Ti+)[cite: 116, 119].
    * [cite_start]**Edge Inference:** Deployed on NVIDIA Jetson Orin Nano[cite: 135].
    * [cite_start]**Robots:** Unitree Go2 or G1 Humanoids[cite: 149, 160].

3.  [cite_start]**Modular Architecture:** Structure the Docusaurus project to easily support future integrations of RAG Chatbots, User Auth, and Localization without breaking the core content[cite: 17, 22].

4.  **Tone & Style:** Technical but visionary. [cite_start]Emphasize that "The future of work will be a partnership between people, intelligent agents, and robots".

# Output Format
-   **Framework:** Docusaurus (Classic Preset).
-   **Environment:** Python `uv` for backend scripts; Node.js for frontend.
-   **Delivery:** Markdown (`.md` or `.mdx`) files organized by Module/Week in the `docs` folder.

## Response snapshot

Updated the project constitution to reflect the Physical AI & Humanoid Robotics textbook project with 4-module structure, hardware requirements, and modular architecture principles. Updated related templates to align with the new constitution.

## Outcome

- ✅ Impact: New constitution established for Physical AI textbook project with 4 core modules and hardware requirements
- 🧪 Tests: No tests required for constitution update
- 📁 Files: Updated constitution, plan template, spec template, tasks template, and created README
- 🔁 Next prompts: Module development for ROS 2, Digital Twin, AI-Robot Brain, and VLA
- 🧠 Reflection: Constitution properly reflects the specialized nature of the Physical AI textbook project

## Evaluation notes (flywheel)

- Failure modes observed: None
- Graders run and results (PASS/FAIL): N/A
- Prompt variant (if applicable): N/A
- Next experiment (smallest change to try): Begin module development based on constitution
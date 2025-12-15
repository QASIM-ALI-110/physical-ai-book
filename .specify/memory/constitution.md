<!-- SYNC IMPACT REPORT
Version change: 0.0.0 → 1.0.0
Modified principles: None (new project constitution)
Added sections: All principles and sections added for new project
Removed sections: None (new project)
Templates requiring updates:
- .specify/templates/plan-template.md ✅ updated
- .specify/templates/spec-template.md ✅ updated
- .specify/templates/tasks-template.md ✅ updated
- .specify/templates/commands/*.md ⚠ pending
- README.md ⚠ pending
Follow-up TODOs: None
-->

# Physical AI & Humanoid Robotics Constitution

## Core Principles

### Strict Syllabus Adherence
The content must accurately reflect the 4-Module structure: Module 1: The Robotic Nervous System (ROS 2), Module 2: The Digital Twin (Gazebo & Unity), Module 3: The AI-Robot Brain (NVIDIA Isaac), Module 4: Vision-Language-Action (VLA) & Capstone.

### Hardware Realism
Every coding example or concept must account for the required hardware constraints: Simulation requires High-Performance Workstations (NVIDIA RTX 4070 Ti+), Edge Inference deployed on NVIDIA Jetson Orin Nano, Robots are Unitree Go2 or G1 Humanoids.

### Modular Architecture
Structure the Docusaurus project to easily support future integrations of RAG Chatbots, User Auth, and Localization without breaking the core content.

### Test-First (NON-NEGOTIABLE)
Every module and concept must include practical exercises and tests before theoretical explanation; Students must implement code examples and verify functionality before moving forward.

### Visionary Technical Approach
Technical content should emphasize that the future of work will be a partnership between people, intelligent agents, and robots.

### Spec-Driven Development
Create a unified, Spec-driven textbook using Docusaurus that teaches students to bridge the gap between the digital brain (AI Agents) and the physical body (Robots).

## Technology Stack Requirements

Framework: Docusaurus (Classic Preset); Environment: Python uv for backend scripts; Node.js for frontend; Delivery: Markdown (.md or .mdx) files organized by Module/Week in the docs folder.

## Development Workflow

Content development follows the Spec-Driven approach with clear modules, peer reviews for technical accuracy, and practical hands-on exercises for each concept taught.

## Governance

All content must comply with the 4-module syllabus structure; Hardware requirements must be clearly specified for each practical exercise; Content must be validated against actual hardware platforms (Unitree Go2/G1, NVIDIA Jetson Orin Nano, high-performance workstations).

**Version**: 1.0.0 | **Ratified**: 2025-12-15 | **Last Amended**: 2025-12-15
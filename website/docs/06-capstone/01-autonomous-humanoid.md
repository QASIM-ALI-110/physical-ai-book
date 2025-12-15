---
id: autonomous-humanoid
title: Capstone Project
---

# Capstone Project

## Project Goal

[**Goal:** Build a robot that receives voice commands, plans a path, and manipulates objects](cite: 79). The capstone project integrates all the concepts learned throughout the course into a comprehensive application that demonstrates the full pipeline of physical AI and humanoid robotics.

Students will build an autonomous system that can:
- Receive and understand voice commands
- Plan navigation paths in dynamic environments
- Identify and manipulate objects using computer vision
- Execute complex multi-step tasks autonomously

## System Workflow

The complete system follows this workflow:

```
Voice Command -> Whisper -> LLM Planner -> ROS 2 Nav2 -> Action
```

This pipeline represents the full integration of:
1. Voice input processing through Whisper
2. Cognitive planning through LLMs
3. Navigation planning through ROS 2 Navigation Stack (Nav2)
4. Physical action execution on the robot platform

The capstone project demonstrates how all components work together to create an intelligent, autonomous humanoid robot capable of performing complex tasks based on natural language commands.
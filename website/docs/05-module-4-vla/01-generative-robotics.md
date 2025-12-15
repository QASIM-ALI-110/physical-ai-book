---
id: generative-robotics
title: Vision-Language-Action Models
---

# Vision-Language-Action Models

## Voice-to-Action with OpenAI Whisper

[Explain using **OpenAI Whisper** for voice commands](cite: 76). OpenAI Whisper is a state-of-the-art speech recognition system that can accurately transcribe voice commands from users. In robotics applications, Whisper serves as the input mechanism that converts spoken natural language into text that can be processed by cognitive planning systems.

The system works by capturing audio input from the robot's microphones and processing it through the Whisper model to generate accurate transcriptions. This enables robots to receive complex voice commands from users in natural language.

## Cognitive Planning

[Explain **Cognitive Planning**: Using LLMs to translate "Clean the room" into ROS 2 actions ](cite: 77-78). Cognitive Planning refers to the process where Large Language Models (LLMs) interpret high-level natural language commands and decompose them into sequences of executable actions within the ROS 2 framework.

For example, when a user says "Clean the room," the LLM performs cognitive planning by:
1. Understanding the intent (cleaning)
2. Identifying objects that need cleaning
3. Planning navigation paths to reach those objects
4. Generating specific ROS 2 action calls to control the robot's movement and manipulation

This cognitive planning layer bridges the gap between high-level human instructions and low-level robot control commands.

## Hardware Requirements

This implementation runs on **Jetson Orin Nano**, which provides the necessary computational power to run both the Whisper speech recognition model and the LLM-based cognitive planning system in real-time on the robot platform.
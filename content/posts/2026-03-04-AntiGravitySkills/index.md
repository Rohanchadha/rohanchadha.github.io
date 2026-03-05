---
date: '2026-03-04'
draft: true
title: 'Skills in Antigravity'
tags: ["How I AI","Agents","Antigravity","Vibecoding"]
---

**What are skills?**
Skills are reusable packages of knowledge that extend what the agent can do.

**Main benefits:**
- Much easier to do repeatable things
- Saves context window
- Super sharable & Scalable

**How Antigravity uses skills**
Skills follow a progressive disclosure pattern:

- **Discovery**: When a conversation starts, the agent sees a list of available skills with their names and descriptions
- **Activation**: If a skill looks relevant to your task, the agent reads the full SKILL.md content
- **Execution**: The agent follows the skill's instructions while working on your task

In short - AGY skills are lazy loaded into context window (saving on tokens that would have been used for skills definition)

When to build a skill?
- Single, repeatable task
- Human-in-the-loop
- Process might change/improve

You don't need to explicitly tell agent to use a specific skill, it decides based on the provided context. However, you can mention a skill by name if you want to ensure it's used in the chat window.

- 2 types of skills - Workplace skills & Global skills (differ in the workspace scope)
- Difference between Claude & Antigravity skills -> Claude Skills can be thought of as knowledge whereas AGY is automation oriented (knowledge + scripts)
    - Claude must reason -> write (scripts or code) -> execute
    - AGY skills just reason -> execute


Some notes from [Antigravity documentation](https://antigravity.google/docs/skills) and [codelabs](https://codelabs.developers.google.com/getting-started-with-antigravity-skills?hl=en#4)
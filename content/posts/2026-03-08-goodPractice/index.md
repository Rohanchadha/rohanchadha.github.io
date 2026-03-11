---
date: '2026-03-08'
draft: false
title: 'Vibe Coding - Good Practices'
tags: ["How I AI","Vibecoding","Antigravity"]
---

1. A handy good starter AGENTS.md with 3-layer architecture - Directive, Orchestration, Execution
- Link to file - [AGENTS.md]()
- Add this file in directory, reference it in chat --> @AGENTS.md instantiate
- It'll just set up the folder structure as mentioned in the file


2. Generate an AGENTS.md file at the end (or a logical stop point) of a vibecoding session

- If you're going to be switching models in between & pick the project back again after some gap of time. And you want to avoid context rot, this could be good practice
- You can use below prompt
> Could you create a Gemini.md that effectively encapsulates what this app is, everything we've done so far, and then provides instructions for future models in case we need to pass this off.

- While generating this file, the model would add tonnes of guidance that can just be passed off to new models (new chat windows). When i did this for a project, the file included these sections:
    - App Overview
    - Tech Stack
    - What we've done so far (Structure/Layouts, Mock Data, Interactions, Design Elements)
    - Instructions for future AI models

3. Running Security Audits

    - Using this [prompt]() from Nick Saraev's [video](https://www.youtube.com/watch?v=gcuR_-rzlDw)
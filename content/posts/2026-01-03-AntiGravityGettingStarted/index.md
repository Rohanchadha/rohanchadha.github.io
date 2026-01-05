---
date: '2026-01-03'
draft: false
title: 'Getting Started with Antigravity'
tags: ["How I AI","Agents","Antigravity","vibecoding"]
---

I am getting started with antigravity, will be using this post to capture key concepts and terminologies.
Antigravity (AGY) is an agent first platform - you give an instruction to an agent, agent goes off on its own, does its task, asks permissions, produces artifacts, then notifies us 

* Agent Manager & Editor
![Agent Manager vs Editor](AgentManager.png)

* AGY creates artiacts as it plans and gets work done to communicate its work done and get feedback on it. These could be markdown files, architecture diagrams, images, videos, code diffs, etc
    - **Task Lists** - before writing code, agent generates this structured plan
    - **Implementation Plan** - this is used to architect changes within the codebase to do a task & it contains a lot of technical details (what tech stack it will use, etc)
    - **Walkthrough** - created once the task is completed, it summarizes changes & tells you how to test it
    - **Code Diffs** 
    - **Screenshots** - state of UI before and after the code changes
    - **Browser Recordings** - for dynamic interactions, agent records the video of the session

* It is possible to interact with the artifacts by highlighting text and commenting on it. The agent will consider the feedback and iterate on it

* AntiGravity Browser subagent - AGY managed browser & can operate on the pages. It can click, scroll, read console logs, read DOM, click screenshots, make videos, parse markdoen etc.

* You can use '@' to include context such as a file, directory, MCP server or use '/' to refer to a workflow (saved prompts) 

* Rules and Workflows:
    - Rules help guide the behavior of the agent. Guidelines you to provide agent to be followed (coding style, document methods)
    - Workflows are saved prompts. They can also guide agent's behavior but they are called on demand
    ![Workflow Example](workflow.png)

* Terminal Command Auto Execution - giving the agent access to terminal and browsers enables autonomous debugging, deployment but also opens axis for security risks. There's 3 settings that agy has:
    - Off - agent never auto-executes terminal commands unless explicitly allowed (in allow list)
    - Auto - asks for permission for risky commands
    - Turbo - always auto-executes (unless in Deny list)



Reference Links - https://codelabs.developers.google.com/getting-started-google-antigravity]
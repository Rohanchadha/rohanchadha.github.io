---
date: '2026-03-08'
draft: false
title: 'Python - good practice'
tags: ["Python"]
---

##Good practice for Python environments

I have ran into same issue thrice now w.r.t python environments
Writing this here for future reference

- Venv - each project with its own self-contained environments.
- Create a .venv folder with fresh python3 copy 
  -  python3 -m venv .venv
- Activate it (you'll need to do this each terminal session)
  - source venv/bin/activate
- Install all dependencies
  - pip install -r requirements.txt
- Proceed to whatever you were gonna do
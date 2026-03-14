---
date: '2026-03-14'
draft: false
title: 'Git - good practice'
tags: ["Git"]
---

Remote/Origin refers to what's present in the online GH repos

When starting a project locally:
- Copy github URL of the repo
- Do a git clone {repo URL} in your local folder's location
- Now you have the remote's main branch on your local

> Now let's say you've made a lot of changes locally that you want to push to remote main BUT your remote main may also be few changes ahead now. So, how do you proceed?

Follow these steps

- git branch main
- git pull (takes latest remote main pull in your local main)
- git checkout -b localbranch (creates new branch - localbranch)
- Do all your changes for new features in new localbranch
- git status/add/commit
- git push --set-upstream origin localbranch (adds your localbranch on remote also)
- git checkout main 
- git pull (taking latest remote main in local before merging)
- git checkout localbranch
- git merge main
- git push (your localbranch changes merged with remote main changes sent for PR review)
- Now a pr has been raised to the owner of the repo. They can approve and merge it
- Good practice to delete localbranch after it has been merged on remote
- New feature, create a new localbranch
- Take fresh git pull of remote Main
- Repeat

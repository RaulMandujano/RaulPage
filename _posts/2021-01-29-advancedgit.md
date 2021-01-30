---
layout: post
title:  Advanced Git
categories: [Git]
excerpt: What is git rebase?  Rebasing is used to be able to combine existing commits within a branch with commits already in it. The main function of this is to be able to add the new code added by a collaborator by the team into the master branch or the main branch.
---

Git rebase

•	What is git rebase?
Rebasing is used to be able to combine existing commits within a branch with commits already in it. The main function of this is to be able to add the new code added by a collaborator by the team into the master branch or the main branch.

•	What are some advantages and disadvantages of git rebase? (At least 2 of each)
The advantages of using Rebase within a project are:
1.	You get a cleaner and easier code to merge with other branches.
2.	Delete merges created and no longer used when using the Git merge command within GIT.
The disadvantages when using Rebase:
1.	When Rebase is done, one of the conflicts may be losing the authority to modify created commits.
2.	Another big problem with rebase, is that when rebase between branches, you lose the option to create Pull Request.

•	When shouldn't you use git rebase? Why?
When you work in a group or on multi-programmer projects. Why? Overrun should be avoided in these circumstances since it would avoid the use of Pull Request, and Pull Requests help the code to be fluid among all programmers since they are accepted manually by a Project Manager.

When you rebase your branch to the main branch, it will look like this:

<img width="572" alt="completerebase" src="https://user-images.githubusercontent.com/22435576/106361877-05d3e780-62dd-11eb-8db9-2159a78d7f37.png">

and this is how it will be the result:

<img width="432" alt="rebase2" src="https://user-images.githubusercontent.com/22435576/106361904-269c3d00-62dd-11eb-8504-057e9693bd4e.png">

Git Interactive rebase merge will look like this, it will open the list of things that are going to be changed with the rebase:

<img width="570" alt="interactive" src="https://user-images.githubusercontent.com/22435576/106362203-cd350d80-62de-11eb-908e-f4ea2c27d4c5.png">


When you shouldn't rebase. If you rebase the main branch to your branch it will this happen.
![norebase](https://user-images.githubusercontent.com/22435576/106361410-f8b5f900-62da-11eb-8601-646d59e566f2.jpg)

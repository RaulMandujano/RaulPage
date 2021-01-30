---
layout: post
title:  Advanced Git
categories: [Git]
excerpt: What is git rebase?  Rebasing is used to be able to combine existing commits within a branch with commits already in it. The main function of this is to be able to add the new code added by a collaborator by the team into the master branch or the main branch.
---

**Git rebase**

**•	What is git rebase?**
Rebasing is used to be able to combine existing commits within a branch with commits already in it. The main function of this is to be able to add the new code added by a collaborator by the team into the master branch or the main branch.

**•	What are some advantages and disadvantages of git rebase? (At least 2 of each)**
The advantages of using Rebase within a project are:
1.	You get a cleaner and easier code to merge with other branches.
2.	Delete merges created and no longer used when using the Git merge command within GIT.
The disadvantages when using Rebase:
1.	When Rebase is done, one of the conflicts may be losing the authority to modify created commits.
2.	Another big problem with rebase, is that when rebase between branches, you lose the option to create Pull Request.

**•	When shouldn't you use git rebase? Why?**

When you work in a group or on multi-programmer projects. Why? Overrun should be avoided in these circumstances since it would avoid the use of Pull Request, and Pull Requests help the code to be fluid among all programmers since they are accepted manually by a Project Manager.

When you rebase your branch to the main branch, it will look like this:

<img width="572" alt="completerebase" src="https://user-images.githubusercontent.com/22435576/106361877-05d3e780-62dd-11eb-8db9-2159a78d7f37.png">

and this is how it will be the result:

<img width="432" alt="rebase2" src="https://user-images.githubusercontent.com/22435576/106361904-269c3d00-62dd-11eb-8504-057e9693bd4e.png">

Git Interactive rebase merge will look like this, it will open the list of things that are going to be changed with the rebase:

<img width="570" alt="interactive" src="https://user-images.githubusercontent.com/22435576/106362203-cd350d80-62de-11eb-908e-f4ea2c27d4c5.png">


When you shouldn't rebase. If you rebase the main branch to your branch it will this happen.

<img width="504" alt="Screen Shot 2021-01-29 at 11 39 03 AM" src="https://user-images.githubusercontent.com/22435576/106363607-b98da500-62e6-11eb-86ba-4b3f118b4f58.png">


**Git reset, checkout, and revert**

**•	What is git reset?**

Git reset is the command that is used to return or undo an unwanted change. It has three types of shapes, which is --soft, --mixed, --hard. The three uses correspond to Git's three internal state.

**•	What is the difference between hard, mixed and soft:**

    hard is the most used reset command but at the same time it is the most dangerous when working on projects, since it deletes the previous information at the time of undo and could cause loss of information.
    
  	mixed is the reset command that is used in the same way as hard, but in this case, this command takes the uncompleted information and does not discard it, but instead moves it to the working directory.
    
  	soft unlike the others, reset the commits made in the project, this option is used when you committed something by accident.

**•	What is git checkout?**

Checkout works for navigating from branch to branch or even being able to access a commit using the commit number.

**•	What is git revert?**

Git revert, as the name implies, revert works to revert any changes made and take you to the previous step.

**•	In what ways are these commands the same and what ways are they different?**

These 3 commands are similar in themselves because they have the same functionality with each other, without one command you cannot use the other. You could not revert without accessing the branch using checkout or in the same way reset.
In that they are not alike, in the use and the way I use since the 3 are used in totally different times.

In this example I am using "git checkout your_branch_name" to move from one branch to the other.

<img width="303" alt="gitcheckout" src="https://user-images.githubusercontent.com/22435576/106363475-045aed00-62e6-11eb-8c36-b6413df40899.png">

and if you want to access to a commit use "git checkout commit_number" and it will show a message like this

<img width="605" alt="checkoutcommit" src="https://user-images.githubusercontent.com/22435576/106363689-4fc1cb00-62e7-11eb-8750-89b47663d47e.png">

In this example I use "git reset" plus the command --hard to be able to revert.

<img width="323" alt="gitreset" src="https://user-images.githubusercontent.com/22435576/106363547-64519380-62e6-11eb-8e3f-da6086f1d474.png">

In this example I use "git revert HEAD" to revert every change made.

<img width="447" alt="Gitrevert" src="https://user-images.githubusercontent.com/22435576/106363529-57cd3b00-62e6-11eb-91a5-120107daeb8e.png">

**Git Submodules**

Git submodule is a repository within another reposity. Git submodule allows you to be able to have a git repository as a sub directory. Git submodule creates its own commit history which allows better handling of the information it stores. It works excellent for large projects as they store different types of information.
The biggest advantage of using submodules is that it creates independence for you to track changes or create changes independent of the project. But this itself attracts the downside, which is when you want to merge, cloning or forking the repository. This occurs due to the same independence that the submodule has from the repository


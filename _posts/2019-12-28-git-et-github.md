---
layout:     post
title:      Git and Github for Beginner
date:       2019-12-18
author: Andry
summary:
categories: [ JavaScript, API,beginner, introduction,Tools ]
mathjax: true
courses: true
image: images/trygit.jpg
---
⚠️ If you are not on macOS or a Linux distribution, don’t try to type those commands in the regular Windows Command Prompt, they won’t work. You need to do one of the following:

* Install [Linux Bash Shell]() on your Windows 10

* You don’t have Windows 10? Head to [Cloud9]() and create a free account. You’ll have your personal “linux in the cloud” with a real terminal.

In this workshop, you’ll learn how to:

* Start **tracking versions** of a project using git

* **Commit (save) your work**

* Use **branches** to collaborate on a project

* Use **GitHub** to back up your work in the cloud

* Discover GitHub’s features for **collaborating**

* Deploy a simple static website using **GitHub Pages**

* Solve **conflicts** in your code between two versions

You can go through the slides [here]()

---

#### Main takeaways

**Git** allows us to **track versions** of a project (= a set of files in a folder on your computer):

```git
git init
```
From now on, each time you change something in a file anywhere in this folder, **git will track these changes** 🕵️.

Do not run this command in your `$HOME` folder (the `~` folder, or `/Users/<your_name>` on Mac).
Always create a new folder (with `mkdir`) and go into it (with `cd`). That’s where you’ll want to run the `git init` command.

To save your last changes with git 💾, follow this 3-step process:

**Check** the files that were modified since your last commit:

```git
git status
```
Add the modified files you want to save:

```git
git add logo.png index.html style.css
(tip: you can also use `git .` to add all the files)
```
Commit the changes with a message that clearly details the changes you have made:

```git
git commit --message "added logo in homepage and set width"
```
Add a remote repository to:
- Have a backup of your work in the cloud ☁️;
- Centralize your team’s work 🎯.

**Go on GitHub** and create a repository.

**Connect it to your local git repo** by running the following command in your terminal:
```git
git remote add origin git@github.com:github_username/repo_name.git

```
Push your work on your remote repository:
```git
git push <remote> <branch>

# for instance
git push origin master
```
---

Working as a team implies coordination:

* Communication is key 🔑.

* Branches are also very helpful 🌿.

**One branch = One feature**

Before starting a new feature:

Make sure your local `master` branch is up-to-date with GitHub’s `master:`

```git
git checkout master
git pull origin master
```
Create a new branch and move on it:

```git
git branch update-logo
git checkout update-logo
```

When your work is done, it’s time to request a review by your peers:

* Add, commit and push your last changes.

* Go on GitHub and create a **Pull Request.**
  This opens a **conversation** among your team

* Your teammates will read the changes you made, comment, ask questions, **request corrections** and maybe new changes.

* This will trigger new commits on your side, and when everyone is satisfied, the **lead developer** will merge the changes to the master branch (== the live version of your website).
Happy Hacking 🚀🚀🚀

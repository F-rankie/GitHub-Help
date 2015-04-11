---
title: "Github Essentials"
author: "Frank M. Berger"
date: "Saturday, February 14, 2015"
output: html_document
---




Last Update: 20-Feb-2015

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

## 1. General concept

At the heart of GitHub is an open source version control system (VCS) called Git. Git is responsible for everything GitHub-related that happens locally on your computer.

VCS are used when several people work on the same project. GitHub is  a de-facto standard for distributing code to a wider audience (e.g., for online courses / MOOCs).

## 2. My GitHub Account

Login via https://github.com/login

User name: F-rankie
Password: X X 1 t_ _ _ _ _ _ _

bottom right: "Your repositories"

## 3. Repositories

A repository can be thought of as a folder containing everything (in particular files with source code, like .R files) belonging to one project. A repository can reside either at the GitHub server (@ http://www.github.com) or, as a "cloned" copy, on the local machine (your PC).
The URL for a repository on the GitHub server ends with ".git", also the repository itself is sometimes referred to as a **git**.

## 4. Cloning

To "clone", in Git lingo, means to copy a repository from the GitHub server to the local machine. Several ways exist to achieve this:

* via the command line and the **git clone** command, see -> Git Shell
* via your browser when logged in at http://www.github.com

## X. Workflow to add a new master repository on GitHub

This assumes an **already existing** local project with an existing README.md and one or more .R scripts (e.g. **MyProject.R**).

1.  Login at http://www.github.com
2.  Add new repository (click on the "+" button next to the user name) - e.g. **MyNewRepository**
3.  Enter new name of repository and description.
4.  **Un**click "Initialize this repository with a README" - you already have one
5.  Click on ".gitignore" and select "R"
6.  Select appropriate license, if applicable
7.  Copy URL of the new .git to clipboard (there is a button for that)
8.  Start **git shell** (Windows Powershell with git enabled)
9.  Within the shell, navigate to the existing local project folder
10.  Use the following command line commandos *(can probably still be improved)*. To paste the URL from the clipboard, use mouse right-click.

```
git init
git add README.md
git add MyProject.R
git commit -m "First commit of the new repository"
git remote add origin https://github.com/F-rankie/MyNewRepository.git
git push -u origin master
```
Now you have the master repository on the github server, and everything is synched (**README.md** and **MyProject.R**).
If you have a 'good' **.gitignore** file in the project directory (telling git which files to ignore), you may use **git add -A** (for **A**ll files) instead of adding each file individually.

## 8. Deleting a repository

This can be done via **Settings** from within the to-be-deleted repository. The **Delete** function is inside the **Danger Zone**. Be aware of the consequences! 

Deleting a local fork of somebody else's public repository does of course **NOT** delete that public repository.

## 9. Git Shell

A command line environment (using Windows PowerShell) with **git** commands enabled, e.g. **git clone *myurl***. The right mouse button copies the url (from the clipboard) to the command line.

For setting up Git Shell for the first time, see

* https://help.github.com/articles/set-up-git/
* "The Data scientist's Toolbox" - Part 1 of the Data Science Specialization by coursera.org


### git clone

### git status

**git status** shows the differences between the local copy of the current repository and the copy on the server. To be called from inside a repository.

### git add

**git add filename** adds a new file to git, so git is aware that this should be tracked.

### git commit

**git commit** commits ?? to ?? (recommended to use the -m parameter, like in **git commit -m "explanatory message"**)

### git push

**git push** syncs the committed files in the current (local) repository to the GitHub server (github.com) (push up sync).

### git pull

**git pull** fetches any new changes from the GitHub server to the local repository (pull down sync).

### git help ###

**git help *command*** brings up detailed information for each specific command, e.g. **git help add**.

## GitHub Glossary (alphabetical)

* branch
A branch is ...
* clone     cloning is the process to copy a repository from the GitHub server (@ www.github.com) to the local machine (your PC).
* commit
* fork
* README.MD = a markdown file explaining the project / the repository, automatically created when a new repository is set up. Instructions how to use the repository should go here.
* repository = kind of a folder where you store everything related to a project

# Two hour Git tutorial
This workshop is an introduction to version control systems with Git. 
 Git is a tool for developers and testers to work collaboratively on coding projects.

The primary benefit of git is as a version control system, but with some clever techniques you can weave git into your continuous integration processes for building, testing and deploying.

Git is also the gateway to participating in Open Source projects.  Taking this workshop is a chance to level up your skills, your resume and most importantly, level up your worldview.

This workshop is designed for people who have never used Git or a version control system before, or have only a rudimentary understanding, and want to learn more about what version control systems can do for them and their work.

It will be a hands-on workshop where we will create a GitHub account, and code together to learn the basic flow of Git. 

# Learning Objectives
- What is version control and why should I use it?
- Setting up Git, GitHub
- Tracking changes in Git
- Understanding revision control management & good practices
- Using git to collaborate with others?


## Expectations
This tutorial is ideal for people
- New to revision control
- Who have used other revision control than git
- Have used git, but are still uncertain about best practices
During the course of the tutorial each attendee will practice using git commands by creating and maintaining a custom webpage on their Github Pages site.

## Introduction
- Why revision control?
- Life Insurance
- Software Laboratory
- Collaboration Machine
- Time machine (theory of revision control)

## Basic Commands
- Create / clone a repo
- Commits / Updates / compare
- Markdown language for Readme
- Excercise
- start a working area (see also: git help tutorial)
   clone      Clone a repository into a new directory
   init       Create an empty Git repository or reinitialize an existing one
> //Create a repository and get comfortable with editing & reading status
> 
> git init foo
> 
> cd foo
> 
> (create readme.md)
> 
> (create index.md)
> 
> git status 
> 
> git add .
> 
> git status
> 
> (edit readme.md)
> 
> git status
> 
> git commit *
> 
> (edit the commit message)
> 
> git status
> 
> (edit index.md)
> 
> git status
> 
> git commit -a -m"use my name" 

- Revert
- Branch
- Merge 

## Intermediate Concepts
- permissions
- following repos
- pull request
- The Github flow method
- github vs bitbucket vs others

## Beyond git
- github pages
- Automation
- github project management
- github actions
- dependabot

## CI: Integrating with tools
- IDEs
- Atom
- GitKraken
- Github Desktop
- Slack

## Conclusion
- Q & A
- Next Steps



To integrate:
git
usage: git [--version] [--help] [-C <path>] [-c name=value]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

These are common Git commands used in various situations:


work on the current change (see also: git help everyday)
   add        Add file contents to the index
   mv         Move or rename a file, a directory, or a symlink
   reset      Reset current HEAD to the specified state
   rm         Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect     Use binary search to find the commit that introduced a bug
   grep       Print lines matching a pattern
   log        Show commit logs
   show       Show various types of objects
   status     Show the working tree status

grow, mark and tweak your common history
   branch     List, create, or delete branches
   checkout   Switch branches or restore working tree files
   commit     Record changes to the repository
   diff       Show changes between commits, commit and working tree, etc
   merge      Join two or more development histories together
   rebase     Reapply commits on top of another base tip
   tag        Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch      Download objects and refs from another repository
   pull       Fetch from and integrate with another repository or a local branch
   push       Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.


//How to create the remote repo from the command line?
git remote add foo https://github.com/mxmoss/foo
git remote -v
git push foo master
(enter credentials)

//Delete untracked
erase untracked.txt
git rm untracked.txt
git commit -m"removed untracked.txt"
git status

//Create a branch and make some enhancements


# testGit
This is a small repo of small files to try out the more unusual scenarios with git / github

### How can I commit to a build branch, and then once that passes then commit to master?
(Rather than committing all changes to the master branch)
TBD

### What's the easiest way to create a new repo based on existing code on my system?
TBD

### How can I show a web page from within my repo?
TBD

### How can I compare two separate revisions?
  a) If one of them is the most recent, and the other is 5 revisions ago
  a) If one of them is 5 revisions ago, and the other is 10 revisions ago
TBD

### How can I create a milepost or a release version?
TBD

### How can I view multiple revisions of one file?
TBD

### How can I get a subset of a repo? (ie: only the subdirectory of the main repo)?
TBD

### How can I roll back a set of changes?
TBD

### How can I review the 3 most recent revisions in a repo?
TBD

### How do I get the files from repository?<br/>
Let's say you want to work on a repo locally on your Windows computer. These steps will make a directory:
```DOS
Start | Run |Cmd
mkdir \temp
cd \temp
```

This command retrieves the repo "testGit" from my github account (mxmoss)
```DOS
  git clone https://github.com/mxmoss/testGit
```

### I want to make some changes to the local file
These steps edit a file in the repo (assuming you've done part 1)
```DOS
cd testGit
notepad TestText.txt
Type in some info. For example: "this is a change by my. My name is..."
Ctrl-S
Alt-File-eXit
```

### I want to see the difference between my local files and the repo
This command shows which files are different from the GitHub repo
```DOS
git status
```

### I want to commit my changes to the local file
This step commits the change and adds a message explaining the change
```DOS
git commit -a -m "this is my commit message"
```

### I want to sync the remote GitHub repo with my local files
This command pushes the local changes to GitHub
```DOS
git push origin master
(it will prompt you for username & password)
```


####Links
* [Understanding the GitHub flow] (https://guides.github.com/introduction/flow/)
* [Complete git reference manual] (https://git-scm.com/doc)
* [using Markdown to format the readme.md] (https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [Command line reference / cheatsheet] (https://services.github.com/kit/downloads/github-git-cheat-sheet.pdf)

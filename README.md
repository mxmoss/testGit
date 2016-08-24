# testGit
This is a small repo of small files to try out the more unusual scenarios with git / github

### How can I commit to a dev branch, and once that passes testing then commit to master?
(Rather than committing all changes to the master branch)
TBD

### What's the easiest way to create a new repo based on existing code on my system?
TBD

### How can I show a web page from within my repo?
TBD

## Comparison
  Add /compare to the repo's URL, and then provide a basis for comparison
  
### How can I compare two separate revisions?  
  a) If one of them is the most recent, and the other is a 2 weeks ago?  
Comparisons can be created for arbitrary time periods, like one month or two weeks. To define a time period, type the branch name, followed by a @, and then the date wrapped between a { } notation. For example, typing master@{2weeks} into the base dropdown menu compares the current master branch against the master branch as it was two weeks prior.
Here's an example of a comparison between two time periods.
  https://github.com/mxmoss/testGit/compare/master@{2weeks}...master 
  
  b) Between two specific dates?  
You can also specify a specific date to compare against. Date formatting must follow the ISO8601 standard, which is YYYY-MM-DD.
Here's an example comparing a branch from 07/04/2016 against that same branch a month later.
  https://github.com/mxmoss/testGit/compare/master@{2016-07-04}...master@{2016-08-04}  

  c) If one of them is the most recent, and the other is 2 revisions ago?  
As a shortcut, Git uses the ^ notation to mean "one commit prior."
You can use this notation to compare a single commit or branch against its immediate predecessors. 
For example, 96d29b7^^^^^ indicates five commits prior to 96d29b7, because there are five ^ marks. 
Typing 96d29b7^^^^^ in the base branch and 96d29b7 in the compare branch compares the five commits made before 96d29b7 with the 96d29b7 commit.
  This url shows a comparison between the current revision and three commits ago
  https://github.com/mxmoss/testGit/compare/master^^^...master  
  
  For more information, click this link: https://help.github.com/articles/comparing-commits-across-time/
  
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

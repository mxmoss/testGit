# testGit
This is a small repo of small files to try out the more unusual scenarios with git / github

### How can I commit to a dev branch, and once that passes testing then commit to master?
(Rather than committing all changes to the master branch)
There are two simple ways to merge the dev branch into the master.
1) Through GitHub
View the branch on Github  
https://github.com/mxmoss/testGit/tree/Dev  

Click [New pull Request]  
(Essentially https://github.com/mxmoss/testGit/pull/new/Dev )  

This initiates a pull request.  The pull request checks to see whether the two branches are able to merge. Write an reason for the pull request.

You will see something like this:  
"mxmoss wants to merge 1 commit into master from Dev"  
Click 'Merge Pull request'  
Click [Confirm merge]  

2) Merging via command line.  
You can perform a manual merge on the command line.
https://github.com/mxmoss/testGit.git  

```DOS
git fetch origin
git checkout -b Dev origin/Dev
git merge master
```
Step 2: Merge the changes and update on GitHub.
```DOS
git checkout master
git merge --no-ff Dev
git push origin master
```

### What's the easiest way to create a new repo based on existing code on my system?
I use GitHub desktop. With GitHub desktop, simply drag the directory with your code onto the GitHub client.
It will ask you where you want to create the repo. Accept all defaults. Bam! Repo created.

What about creating a repo from the command line?  
Nope: Outside of the API, there's no way to create a repo on GitHub via the command line.   
Instead: create a new repository on GitHub, then 
Change the current working directory to your local project.
and push to an existing repository (eg: WeirdOrConfusing) from the command line
```DOS
git remote add origin https://github.com/mxmoss/WeirdOrConfusing.git
git push -u origin master
```

### How can I show a web page from within my repo?
You have to use a third party service. Because of that, enterprise repos will not work with this solution.  
To view as a web page, pre-pend this to the URL to the file in github:  
```DOS
http://htmlpreview.github.com/?
```

For example:  
  http://htmlpreview.github.com/?https://github.com/mxmoss/testGit/blob/master/TestHTML.html
  
Alternatively, you could use GitHub pages to render the html 
(suggestion from [here:](http://stackoverflow.com/questions/8446218/how-to-see-an-html-page-on-github-as-a-normal-rendered-html-page-to-see-preview) )
#### Fork the repository to your account.
#### Clone it locally on your machine
#### Create a gh-pages branch (if one already exists, remove it and create a new one based off master).
#### Push the branch back to GitHub.
#### View the pages at http://username.github.com/repo`
In code:
```DOS
git clone git@github.com:username/repo.git
cd repo
git branch gh-pages
# Might need to do this first: git branch -D gh-pages
git push -u origin gh-pages # Push the new branch back to github
Go to http://username.github.com/repo
```

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

# testGit
Learning more about git
very small files to try out the weirder scenarios with git

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
This steps commits the change and adds a message explaining the change
```DOS
git commit -a -m "this is my commit message"
```

### I want to sync the remote GitHub repo with my local files
This command pushes the local changes to GitHub
```DOS
git push origin master
(it will prompt you for username & password)
```


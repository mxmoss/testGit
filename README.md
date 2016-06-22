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

And this steps will retrieve the repo "testGit" from my github account
  git clone https://github.com/mxmoss/testGit

### I want to make some changes to the local file
These steps will edit a file (assuming you've done part 1)
```DOS
cd testGit
notepad TestText.txt
(type in some info "this is a change by Manas")
Ctrl-S
Alt-File-eXit
```

### I want to see the difference between my local files and the repo
This command will show the differences
```DOS
git status
```

### I want to commit my changes to the local file
This steps commits the change and add a message explaining the change
```DOS
git commit -a -m "this is my commit message"
```

### I want to sync the remote GitHub repo with my local files
This command pushes the local changes to GitHub
```DOS
git push origin master
(it will prompt you for username & password)
```


# testGit
Learning more about git
very small files to try out the weirder scenarios with git

1) How do I get the files from repository?
Let's say you want to work on a repo locally on your Windows computer.
These steps will make a directory:

  Start | Run |Cmd
  mkdir \temp
  cd \temp

And this steps will retrieve the repo "testGit" from my github account
  git clone https://github.com/mxmoss/testGit

2) I want to make some changes to the local file
These steps will edit a file (assuming you've done part 1)
  cd testGit
  notepad TestText.txt
  (type in some info "this is a change by Manas")
  Ctrl-S
  Alt-File-eXit

3) I want to commit my changes to the local file
This steps commits the change and add a message explaining the change
  git commit -a -m "this is my commit message"

4) I want to sync the remote GitHub repo with my local files
This step pushes the local changes to GitHub
  git push origin master
  (it will prompt you for username & password)


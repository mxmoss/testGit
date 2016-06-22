# testGit
Learning more about git
very small files to try out the weirder scenarios with git

#1) How do I get the files from repository?<br/>
Let's say you want to work on a repo locally on your Windows computer. These steps will make a directory:<br/>
<ul>
<li>Start | Run |Cmd</li>
<li>mkdir \temp</li>
<li>cd \temp</li>
</ul>

And this steps will retrieve the repo "testGit" from my github account
  git clone https://github.com/mxmoss/testGit

2) I want to make some changes to the local file
These steps will edit a file (assuming you've done part 1)
  cd testGit
  notepad TestText.txt
  (type in some info "this is a change by Manas")
  Ctrl-S
  Alt-File-eXit

3) I want to see the difference between my local files and the repo
This step will show the differences
  git status

4) I want to commit my changes to the local file
This steps commits the change and add a message explaining the change
  git commit -a -m "this is my commit message"

5) I want to sync the remote GitHub repo with my local files
This step pushes the local changes to GitHub
  git push origin master
  (it will prompt you for username & password)


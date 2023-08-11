# Step 1 - (Create a myrepo directory):

**(mkdir)**
Used to create a new directory.

**(myrepo)**
The name of the directory you want to create

- mkdir myrepo
#
#
#
#
# Step 2 - (Go into the myrepo directory):

- cd myrepo
#
#
#
#
#
# Step 3 - (In this myrepo directory create a new local git repository using the git init command):

**(int)**
Create a new local repository using

- git init
#
#
#
#
#
#
# Step 4 - ( verify by doing a directory listing):

**(ls)**  
The command to list files and directories.

**(-la)**
'-l'option (long format) provides detailed information about each item, '-a' option (all) includes hidden  files and directories in the listing.

**(.git)**
This is the argument provided to the 'ls' command. It specifies the directory you want to list, which is  the '.git' directory in this case.

- ls -la .git
#
#
#
#
#
# Step 5 - (create an empty file):

**(touch)**
used to create or update file timestamps

- touch newfile
#
#
#
#
#
# Step 6 - (Add file "newfile" to the repo using the following):

- git add newfile
#
#
#
#
#
# Step 7 - (Before committing the changes, need to tell git who we are.):

**(git config)**
Used to configure various settings and options for Git. (sets your global user email and username for Git) 

**(--global)**
The flag indicates that this configuration is applied globally for all repositories on your system.

**(user.)**
Configuration key for the user's email and name.

- git config --global user.email "you@example.com"
- git config --global user.name "Your Name"
#
#
#
#
#
# Step 8 - (commit our changes):

**(git commit)**
the command to create a new commit. Commits are snapshots of changes made to the repository.

**(-m)**
'-m' flag stands for "message," and it is used to provide a brief description of the changes you are committing

- git commit -m "added newfile"
#
#
#
#
#
# Step 9 - (To make subsequent changes in the repo, create a new branch(my1stbranch) in the local repostitory):

**(git branch)**
The command to manage branches in Git.

- git branch my1stbranch
#
#
#
#
#
# Step 10 - (Check which branches our repo contains(Default 'master' branch will have an * next to it)):

- git branch
#
#
#
#
#
# Step 11 - (To work in the new branch(my1stbranch) issue, make it be the active branch):

**(git checkout)**
a command followed by the name of the branch(my1stbranch) you want to switch to, Git will update your working directory and switch the active branch to the specified branch "my1stbranch".

- git checkout my1stbranch
#
#
#
#
#
# Step 12 - (Verify that the new branch is now the active branch(the * is now next to the 'my1stbranch' indicating that it is now active)):

- git branch
#
#
#
#
#
# Step (9 and 11) - (AS a shortcut to creating branch(my1stbranch) using git branch and then making it active using 'git checkout'):

**(-b)**
'-b' flag is used to create a new branch. 

- git checkout -b my1stbranch
#
#
#
#
#
# Step 13 - (adding some text to 'newfile'):

**(echo)**
Used to display text or messages in the terminal

**(>> )**
'>>' operator is used to append the output of the preceding command (in this case, the echoed text) to a file named "newfile."

- echo 'Here is some text in my newfile.' >> newfile
#
#
#
#
#
# Step 14 - (Verify the text has been added):

**(cat)**
Used to display the contents of a file in the terminal

- cat newfile
#
#
#
#
#
# Step 15 - (Create another file):

- touch readme.md
#
#
#
#
#
# Step 16 - (Add it to the repo):

- git add readme.md
#
#
#
#
#
# Step 17 - (Verify the changes in our current branch):

- git status
#
#
#
#
#
# Step 18 - (A shortcut to adding all modifications and additions):

- git add *
#
#
#
#
#
# Step 19 - (Save them to the branch with a message indicating the changes):

- git commit -m "added readme.md modified newfile"
#
#
#
#
#
# Step 20 - (To get a history of recent commits):

- git log (To quit from the git log please type q)
#
#
#
#
#
# Step 21 - (Sometimes you may not fully test your changes before comitting them and may have undesirable consequences, you can back out your changes ):

**(HEAD)**
Refers to the most recent commit in the current branch. It represents the commit you want to revert.

**(--no-edit)**
This flag tells Git not to open the default text editor for you to modify the commit message. If you omit this flag, Git will open the editor for you to provide a commit message explaining the revert.

- git revert HEAD --no-edit
#
#
#
#
#
# Step 22 - (Create another file):

- touch goodfile
- git add goodfile
- git commit -m "added goodfile"
- git log
#
#
#
#
#
# Step 22 - (Make the 'master' branch active):

- git checkout master
#
#
#
#
#
# Step 22 - ( Merge the changes from 'my1stbranch' into 'master'):

- git merge my1stbranch
- git log (Check History)
#
#
#
#
#
# Step 22 - (Changes have been merged into the 'master' branch, the 'my1stbranch' can be deleted):

**(git branch)**
The command to manage branches in Git.

**(-d)**
'-d' flag is used to delete a branch

- git branch -d my1stbranch


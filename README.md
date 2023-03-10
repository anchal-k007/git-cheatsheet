# Git-Cheatsheet
This is my collection of git commands that I will use

### git init
Initialise a git repository in the folder that you are currently present in the terminal

### git add \<filenames\>
Add the files that will shift from the present working directory to the staging area

### git status
List all new or modified files that haven't yet been committed in the current git repository

### git restore --staged \<filenames\>
Remove the filenames from the staging area

### git commit -m "Your message"
Commit the changes that are present in the staging area. The commit has an associated hash value with it that uniquely identifies the commit

### git log -(number)
- number is optional
- Logs all the commits that have been made if number is not specified, else logs the latest (number) of commits that have been made on the present branch
- Sometimes when logging, the terminal may hang. Press q and press enter to exit

### git log --oneline
A summarised version of the log is shown

### git ls-files
- Returns the list of files that are present in the index aka staging area
- Once a file has been commited, it is very difficult to remove it from the index (atleast I still don't know how to do it, and the biteinteractive article says so)

### git checkout \<filename\>
- Undo all the changes that have been made to *filename* since the most recent commit
- Also shifts HEAD to point to that particular file

### git restore \<filename\>
- Undo all the changes that have been made to *filename* since the most recent commit

### git revert \<hashcode\>
- Haven't used this yet, so not so sure
- Reverts back all the changes that have been performed since the *hashcode commit*
- It changes the repository to the stage before the *hashcode commit* was made

### git branch
List all the branches that are currently present

### git branch \<branchname\>
Create a new branch with *branchname*

### git checkout \<branchname\>
Shift to the specified branchname

### git checkout -b \<branchname\>
A shortcut to create a new branch and shift onto it

### git branch -d \<branchname\>
- Delete the specified *branchname*
- Git does not allow to delete the branch you are currently on

### git branch -m \<old-branch\> \<new-branch\>
- Rename the *old-branch* to *new-branch*

### git branch -m \<new-branch\>
- Rename the current branch to *new-branch*

### git merge \<branchname\>
- Merge the specified \<branchname\> with the current branch
- If there are any conflicts, they will need to be solved first 
- If there are no conflicts, Vim editor will open in terminal on which we can write our commit message
- Type **:q!** to exit the Vim editor and commit the changes

### git remote add \<name\> \<url\>
- Create a new connection to a remote repository. After adding a remote, you???ll be able to use *name* as a convenient shortcut for *url* in other Git commands.
- *name* can be anything, but by convention it is set as **origin**
- *url* is the url of the github repository

### git push \<remote-name\> \<branch-name\> -u
- Push the specified branch to the the remote repository

### git push \<remote-name\> \<local-branch-name\>:\<remote-branch-name\> 
This pushes the *local-branch-name* to your *remote-name*, but it is renamed to *remote-branch-name*

### git clone \<url\>
Clones the remote repository onto our local folder

### git rev-parse --absolute-git-dir
Git will tell you the path, if any, to the .git repository that the current folder ???belongs??? to.

### git diff
Shows how the index differs from the working tree

### git diff --cached
Shows how the index differs from the most recent commit

### git checkout \<branchname\>^
- **^** is the relative reference operator
- Moves the head pointer to the parent of the *branchname*

### git checkout \<branchname\>~\<number\>
- **~** is again a relative reference operator that allows us to move *number* parents upwards of the specified branch 

### git branch -f \<branch1\> \<branch2\>
- Used to reassign the branches
- Moves by force, the _branch1_ to _branch2_
- _branch1_ and _branch2_ can both be relative referenced as well


******************************************************************************************************************************************************************



# Useful articles and resources relating to git
- [Picturing how git works](https://www.biteinteractive.com/picturing-git-conceptions-and-misconceptions/)
- [Learn git interactively](https://learngitbranching.js.org/)



# Important git commands

### Begineer level commands

- `git init` -> Powers your folder to be managed by git, and initialises a new empty repository. It also creates a .git folder that has all the relevant logic to manage versions of your project.

- Working Area -> There can be a bunch of files that are not currently handled by git. It means that changes done or to be done in those files are not managed by git yet. A file which is in working area is considered to be not in the staging area. When we do git status and we see abunch if untracked files then these are actually called to be in the working area.

- Staging area -> What all files are going to be part of the next version that we will create. This staging area is the place where git knows what changes will be done from the last version to the next version.

- Repository Area -> This area actually contains the details of all you previous registered version. And the files in this area, git already manages them and knows their version history.

- `git add <file>` -> moves file from working area to staging area

- `git rm --cached <file>` -> moves file back from staging area to working area

- commit -> Commit is a particular version of the project. It captures a snapshot of the project's staged changes and creates a version out of it.

- `git commit` -> registers staging changes to a commit.

- `git log` -> list downs all the commits of the repository. If you want to exit out of git log prompt press q.

- `git restore <file>` -> it removes all files changes from the staging area to be committed. This can be useful, if we did some dirty piece of code and now no more want it. Instead of deleting every change line by line, we can restore it or you can say restore last clean version of the file.

- `git restore --staged <file>` -> it removes file from changes from staging area to the working area. this only works if changes are in your staging area

- Diff between git rm and git restore ans: if you want to move the whole file back to the untracked state, then we do git rm, otherwise if we just want the changes to be moved in working area or staging area then we git restore.

- `git diff <commit1-id> <commit2-id>` -> gives the difference of all file changes between two commits

- `git commit -m "<your commit message>"` -> If we want to avoid opening a text editor like vim/nano to add commit message we can use this following command

- `git remote` -> list down all the remote connection names

- Remote connection -> It helps you to link two git repositories for uploading and downloading changes from each otherwise

- `git remote add <name of remote> <link of the remote>` : this command helps us to add a new link to the remote repo and give a name to it

- `git remote rm <name of remote>` : this command deletes a remote connection

- `git remote rename <oldname> <newname>` : this command remanes the remote connection

### Note: The name of the remote connection is always used to establish communication between the repos

- `git add <file1> <file2> <file3>` : this command will add multiple file changes together in the staging area

- `git add .`: this command will add all files from working repo to staging area.

- `git pull <remote name> <branch name>` : downloads latest changes from the branch of the mentioned remote in your local repo.
- these are the basic commands .............

### Recommended practice to do

           - make changes
           - git add <file>
           - git commit
           - git pull
           - git push

- Merge conflicts are a very common scenario
- To resolve merge conflict, we need to open up the conflicting file and choose one option or another.

  merge conflicts can occur if multiple people try to make changes to the same file, and then collaborate

### Git config
-  `git config --global user.name "<name>"`
-  `git config --global user.email "<email>"`
-  `git config --list`

### Git Clone
- `git clone <link>`

### Git add
- `git add .`
- `git add <file_Nmae`

### Git status 
- `git status`

### Git commit
- `git commit -m "message"`
- `git commit --amend` -> It lets us to combine staged changes with previous commit instead of creating an entirely new commit. 

### Command to add & commit
- `git commit -am "message"`

### Git log
- `git log`
- `git log --all`
- `git log --graph`
- `git log --all --decorate --oneline --graph`
- `git log --since="yesterday"`
- `git log --since="1 minute ago"`
- `git log --since=10.minute`
- `git log --grep=<word in commit>` -> to match substring
- `git --no-paper log`

### Git push
- `git push origin main` -> **origin** is the __name of remote__ server & **main** is the __branch name__
- `git push -u origin main` -> set to upstream

### Git tree
- `tree .git`
- To download git tree for windows check the article
- [dev commity article] (https://dev.to/flyingduck92/add-tree-to-git-bash-on-windows-10-1eb1) 

### Git Branch
- **Main** is the default branch
- `git branch` --> to check branch & Listing current branches
-  `git branch -M main` --> to rename main branch
-  `git branch <branch-name>` --> Making a new branch
-  `git checkout -b <branch-Name>` --> to create new branch
-  `git checkout <branch-Name>` --> Switching to a branch
-  `git push origin <branch-name>` --> Pushing the branch to Git
-  `git branch -d <branch-name>` --> to delete the branch

### Merge from branch to main
- `git diff <branch-name>` --> to compare commits,branches,files & more
- `git merge <branch-name>` --> to merge to branches
- perfer this article from stack over flow
(https://stackoverflow.com/questions/5601931/how-do-i-safely-merge-a-git-branch-into-master)

### Some other commands
- `git reflog`
- `git switch -`
- ## git stash
- `git stash`
- `git stash apply`
- `git stash list`
- `git stash show stash@{0}`
- `git stash --include-untracked --<file>`
- `git stash save "added" --include-untracked`
- ## cat
- `git cat-file -p <hashid>`
- `git cat-file -t <hashid>`
- `git checkout <hashid>`
- `cat <filename>`

### Tags 
Tags does not move with new commits
- `git tag <tagname>` --> Creating a tag
- `git tag -a v1.4` --> Annotated tags
- `git tag -a v1.4 -m "my version 1.4"` --> Annotated tags
- `git tag v1.4-lw` --> Lightweight tags
- `git tag` --> Listing tags
- `git tag -d v1` -->  Deleting tags

### Creating readme file
- [github-docs-article] (https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) 


  -This was made by Edara Vamsi..

| **Command**         | ADD FILES TO STAGGING AREA                                         |
| ------------------- | ------------------------------------------------------------------ |
| git add --a         | adding untracked/modified files working directory to staging area  |
| git add file1 file2 | Separate files with spaces to add multiple at once to staging area |
| git add .           | add all files at one time                                          |

2.  ADD FILES TO GIT REPO / COMMIT
    git commit -m " " ===> commitment on staged files/ add files to repository
    git commit –am ===> skip staging area adding file/ directly add to repository and commit
    git commit --amend ===> change commit and file/ redo

3.  GIT LOG
    git log ===> log all commit's
    git log --oneline ===> log only short commit ID and Message
    git log --pretty=oneline ===> log only full commit ID and Message
    git log -p ===> show all changes with the commit
    git log -p -2 ===> show given number of commits with all changes
    git log –stat ===> show details in a short in commit
    git reflog ===> all history with all branch and commit/HEAD
    git reflog show/expire/delete/exists fileName ===> all history with provide subcommand or file
    git reflog branchName@{one.week.ago} ===> access lost commits and not shown in git log with specific period

4.  GIT BRANCH VIEW
    git branch ===> view branches in repository
    git branch –v ===> view branches in repository with more information
    git branch -r ===> view remote branches

5.  GIT BRANCH CREATE AND DELETE
    git branch branchName ===> create new branch
    git branch -d branchName ===> delete branch

6.  GIT SWITCH TO BRANCH / COMMIT (DETACH HEAD) / TAG
    git switch branchName ===> switch one branch to another branch
    git switch -c branchName ===> create and switch (-c = create)
    git checkout branchName ===> switch one branch to another branch
    git checkout --track origin/branchName ===> switch remote branch
    git checkout commitID ===> directly switch HEAD through the commit
    git checkout HEAD~X ===> switch to before HEAD X no. commit
    git checkout origin/master ===> checkout these remote branch pointer
    git checkout tagName ===> switch to tag with detached HEAD
    git checkout branchName@{2.days.ago}

7.  GIT DIFFERENCE
    git diff ===> changes in our working directory/area
    git diff HEAD ===> changes in our working tree from last commit
    git diff --staged or --cached ===> changes in staging area form last commit
    git diff HEAD/--staged fileName ===> changes within specific file
    git diff branch1..branch2 ===> changes within two branches
    git diff commit1..commit2 ===> changes within two commit
    git diff branchName@{X} branchName@{yesterday}

8.  GIT STASH
    git stash ===> change branch without staging/adding unnecesary commit
    git stash pop ===> unstashed head tree/previous state
    git stash list ===> view all the stash list
    git stash apply ===> apply stashed data to other branch/merge content
    git stash apply stash@{x} ===> apply specific stash to branch
    git stash drop stash@{x} ===> delete specific stash
    git stash clear ===> clear all stash
    git stash -u ===> include untracked files in stash

9.  GIT RESTORE / UNDO FILE
    git restore fileName ===> restore modified file in previous state(uncommitted changes lost)
    git restore --source HEAD~X fileName ===> restore file to that commit
    git restore --staged fileName ===> unstage file from staging area
    git checkout HEAD/-- fileName ===> discard all changes to the last commit

10. GIT RESET / UNDO FILE
    git reset commitId ===> committed file add in working area and commit delete/undo file
    git reset --hard commitId ===> committed file and commit delete
    git revert commitId ===> create new revet commit/undo file

11. GIT REMOTE
    git remote -v ===> view any existing remotes in repo
    git remote add remoteName URL ===> adding new remote / remoteName = origin
    git remote rename oldRemoteName newRemoteName ===> rename remote name
    git remote remove remoteName ===> remove/delete remote/repo

12. GIT FETCH
    git fetch origin ===> fetch all changes/download from the origin remote repository to local
    git fetch origin branchName ===> fetch all changes from the specific branch to local

13. GIT PULL
    git pull origin branchName ===> fetch all the new changes and merge to the branch/workDir
    git pull ===> fetch changes from remote using your position/branch

14. GIT PUSH BRANCH / TAGS
    git push remoteName branchName ===> push branch to remote/github
    git push -u remoteName branchName ===> upstream branch to remote
    git push --tags ===> push all tags to remote at a once time

15. GIT FILE / FOLDER / REPO - DELETE / REMOVE
    rm -rf .git ===> delete git repository
    git rm -r -f fileName ===> force to delete file or folder
    git rm --cache file ===> untrack file

16. GIT CLONE
    git clone URLf ===> clone any website from github on local

17. GIT TAG [2.0.9 --> MAJOR.MINOR.PATCH] RELEASE
    git tag ===> view all tag in the repository
    git tag tagName ===> creating lightweight tag - name/label points to the commit
    git tag -a tagName ===> creating annotated tag - store extra meta data
    git tag -a tagName commitID ===> tag an older commit by providing the commit hash/ID
    git tag -f tagName ===> force to reuse tag that already created/referring to other commit
    git tag -l <!-- "*name*" --> ===> view all tag with inclueded provide name
    git tag -d tagName ===> delete any tag with the tag name
    patch release : They typically signify bug fixes and other changes that do not impact how the code is used
    minor release : signify that new features or functionality have been added, but the project is still backwards compatible
    major release : signify significant changes that is no longer backwards compatible. Features may be removed or changed substantially
    lightweight tags : They are just a name/label that points to a particular commit
    annotated tags : store extra meta data including the author's name and email, the date, and a tagging message

18. GIT REBASE
    git rebase branchName ===> cleaner project history and remove unnecessary merge commits
    git rebase -i HEAD~X ===> edit commits, add files, drop commits, etc.
    git rebase --skip ===> skip merge conflict/patch
    git rebase --abort ===> discard any merge changes/go to previous state

19. GIT BASIC
    git status ===> repository status check
    git init ===> repository create
    git mv ===> move or rename the file and directory
    git rm ===> remove any file
    git merge branchName ===> combine two branch
    git config --global alias.st status ===> get shortcut key for git

20. SSH KEY GENERATE
    1)ssh-keygen -t rsa -b 4096 -C "kembalikarabhi19@gmail.com"
    2)eval $(ssh-agent -s)
    3)ssh-add ~/.ssh/id_rsa
    4)tail ~/.ssh/id_rsa.pub

21. CLOSE VIM EDITOR
    1)i ===> add commit/changes
    2)escape
    3):qa ===> hit enter and out Vim
    4):q! ===> save all changes and out Vim
    5):qa! ===> abandone/delete all changes and out Vim

22. IGNORE ANY FILE FROM TRACKING
    1)create .gitignore file
    2)type ignored file name in .gitignore file
    3)if ignored file is already tracking then untrack this file
    4)add and commit .gitignore file in git repository

23. Main Porcelain Commands
    archive Create an archive of files from a named tree
    bisect Use binary search to find the commit that introduced a bug
    bundle Move objects and refs by archive
    checkout Switch branches or restore working tree files
    cherry-pick Apply the changes introduced by some existing commits
    citool Graphical alternative to git-commit
    clean Remove untracked files from the working tree
    describe Give an object a human readable name based on an available ref
    format-patch Prepare patches for e-mail submission
    gc Cleanup unnecessary files and optimize the local repo:

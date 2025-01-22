# git usage:-

>[!question]- **What is Git?**
> 1) Git is a **Software**.
> 2) Git is maintained by **Linux**.
> 3) Git is a **Command Line Tool**. (CMD)
> 4) Git is installed **Locally on the System**.
> 5) Git was first released in **2005**.
> 6) Git has no management **Feature**.

| No. | Substitude | Command Name |
| --- | ---------- | ------------ |
| 1)  | -v         | --version    |
| 2)  | -h         | --help       |

## These are common Git commands used in various situations:

| NO. | ------------------Git Commands------------------ | ---------- | ------------------------What Commands for Use------------------------ |
| --- | ------------------------------------------------ | ---------- | --------------------------------------------------------------------- |
| 01) | `git status                                   `  | ---------  | repository status check                                               |
| 02) | `git init                                     `  | ---------- | repository create                                                     |
| 03) | `git add --a                                  `  | ---------- | adding untracked/modified files working directory to staging area     |
| 04) | `git add file1 file2                          `  | ---------- | Separate files with spaces to add multiple at once to staging area    |
| 05) | `git add .                                    `  | ---------- | add all files at one time                                             |
| 06) | `git commit -m " "                            `  | ---------- | commitment on staged files/ add files to repository                   |
| 07) | `git commit -am                               `  | ---------- | skip staging area adding file/ directly add to repository and commit  |
| 08) | `git commit --amend                           `  | ---------- | change commit and file/ redo                                          |
| 09) | `git log                                      `  | ---------- | log all commit's                                                      |
| 10) | `git log --oneline                            `  | ---------- | log only short commit ID and Message                                  |
| 11) | `git log --pretty=oneline                     `  | ---------- | log only full commit ID and Message                                   |
| 12) | `git log -p                                   `  | ---------- | show all changes with the commit                                      |
| 13) | `git log -p -2                                `  | ---------- | show given number of commits with all changes                         |
| 14) | `git log --stat                               `  | ---------- | show details in a short in commit                                     |
| 15) | `rm -rf .git                                  `  | ---------- | delete git repository                                                 |
| 16) | `git rm -r -f fileName                        `  | ---------- | force to delete file or folder                                        |
| 17) | `git rm --cache file                          `  | ---------- | untracked file                                                        |
| 18) | `git branch                                   `  | ---------- | view branches in repository                                           |
| 19) | `git branch -v                                `  | ---------- | view branches in repository with more information                     |
| 20) | `git branch -r                                `  | ---------- | view remote branches                                                  |
| 21) | `git branch branchName                        `  | ---------- | create new branch                                                     |
| 22) | `git switch branchName                        `  | ---------- | switch one branch to another branch                                   |
| 23) | `git switch -c branchName                     `  | ---------- | create and switch (-c = create)                                       |
| 24) | `git checkout branchName                      `  | ---------- | switch one branch to another branch                                   |
| 25) | `git checkout --track origin/branchName       `  | ---------- | switch remote branch                                                  |
| 26) | `git checkout commitID                        `  | ---------- | directly switch HEAD through the commit                               |
| 27) | `git checkout HEAD~X                          `  | ---------- | switch to before HEAD X no. commit                                    |
| 28) | `git checkout HEAD/-- fileName                `  | ---------- | discard all changes to the last commit                                |
| 29) | `git checkout origin/master                   `  | ---------- | checkout these remote branch pointer                                  |
| 30) | `git merge branchName                         `  | ---------- | combine two branch                                                    |
| 31) | `git branch -d branchName                     `  | ---------- | delete branch                                                         |
| 32) | `git diff                                     `  | ---------- | changes in our working directory/area                                 |
| 33) | `git diff HEAD                                `  | ---------- | changes in our working tree from last commit                          |
| 34) | `git diff --staged or --cached                `  | ---------- | changes in staging area form last commit                              |
| 35) | `git diff HEAD/--staged fileName              `  | ---------- | changes within specific file                                          |
| 36) | `git diff branch1..branch2                    `  | ---------- | changes within two branches                                           |
| 37) | `git diff commit1..commit2                    `  | ---------- | changes within two commit                                             |
| 38) | `git stash                                    `  | ---------- | change branch without staging/adding unnecesary commit                |
| 39) | `git stash pop                                `  | ---------- | unstashed head tree/previous state                                    |
| 40) | `git stash list                               `  | ---------- | view all the stash list                                               |
| 41) | `git stash apply                              `  | ---------- | apply stashed data to other branch/merge content                      |
| 42) | `git stash apply stash@{x}                    `  | ---------- | apply specific stash to branch                                        |
| 43) | `git stash drop stash@{x}                     `  | ---------- | delete specific stash                                                 |
| 44) | `git stash clear                              `  | ---------- | clear all stash                                                       |
| 45) | `git stash -u                                 `  | ---------- | include untracked files in stash                                      |
| 46) | `git restore fileName                         `  | ---------- | restore modified file in previous state(uncommitted changes lost)     |
| 47) | `git restore --source HEAD~X fileName         `  | ---------- | restore file to that commit                                           |
| 48) | `git restore --staged fileName                `  | ---------- | unstage file from staging area                                        |
| 49) | `git reset commitId                           `  | ---------- | committed file add in working area and commit delete/undo file        |
| 50) | `git reset --hard commitId                    `  | ---------- | committed file and commit delete                                      |
| 51) | `git revert commitId                          `  | ---------- | create new revet commit/undo file                                     |
| 52) | `git clone URLf                               `  | ---------- | clone any website from github on local                                |
| 53) | `git remote -v                                `  | ---------- | view any existing remotes in repo                                     |
| 54) | `git remote add remoteName URL                `  | ---------- | adding new remote / remoteName = origin                               |
| 55) | `git remote rename oldRemoteName newRemoteName`  | ---------- | rename remote name                                                    |
| 56) | `git remote remove remoteName                 `  | ---------- | remove/delete remote/repo                                             |
| 57) | `git push remoteName branchName               `  | ---------- | push branch to remote/github                                          |
| 58) | `git fetch origin                             `  | ---------- | fetch all changes from the origin remote repository to local          |
| 59) | `git fetch origin branchName                  `  | ---------- | fetch all changes from the specific branch to local                   |
| 60) | `git pull origin branchName                   `  | ---------- | fetch all the new changes and merge to the branch/workDir             |
| 61) | `git pull                                     `  | ---------- | fetch changes from remote using your position/branch                  |
| 62) | `git tag                                      `  | ---------- | view all tag in the repository                                        |
| 63) | `git tag -l "_name_"                          `  | ---------- | view all tag with inclueded provide name                              |
| 64) | `git checkout tagName                         `  | ---------- | switch to tag with detached HEAD                                      |
| 65) | `git tag tagName                              `  | ---------- | creating lightweight tag - name/label points to the commit            |
| 66) | `git tag -a tagName                           `  | ---------- | creating annotated tag - store extra meta data                        |
| 67) | `git tag -f tagName                           `  | ---------- | force to reuse tag that already created/referring to other commit     |
| 68) | `git tag -d tagName                           `  | ---------- | delete any tag with the tag name                                      |
| 69) | `git push --tags                              `  | ---------- | push all tags to remote at a once time                                |
| 70) | `git reflog                                   `  | ---------- | show all history                                                      |
| 71) | `git reflog master@{one.week.ago}             `  | ---------- | access lost commits and not shown in git log                          |
| 72) | `git config --global alias.cmdSN cmdFN        `  | ---------- | set shortcut name for git command                                     |

<br>

## Here are some ways to exit Vim:

| Steps | Command   | What will do                                                                  |
| ----- | --------- | ----------------------------------------------------------------------------- |
| 1.    | `i      ` | add commit/changes                                                            |
| 2.    | `escape ` | out form editor                                                               |
| 1)    | `:q!    ` | Forces Vim to quit and discard any changes                                    |
| 6)    | `:qa!   ` | abandone/delete all changes and out Vim                                       |
| 2)    | `:wq    ` | Saves changes and exits Vim                                                   |
| 3)    | `ZZ     ` | Saves changes and exits Vim                                                   |
| 4)    | `:x     ` | Save and quit                                                                 |
| 5)    | `:cq    ` | Quit without saving and make Vim return non-zero error (i.e. exit with error) |
| 7)    | `:qa    ` | hit enter and out Vim                                                         |

IGNORE ANY FILE FROM TRACKING

1. create .gitignore file
2. type ignored file name in .gitignore file
3. if ignored file is already tracking then untrack this file
4. add and commit .gitignore file in git repository

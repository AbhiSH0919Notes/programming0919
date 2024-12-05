#### **1) GIT ADD FILES WORKING DIRECTORY TO STAGGING AREA**

**add untracked / modified files**

```
    git add --a
```

**add multiple files**

```
    git add file1 file2
```

**add all files at one time**

```
    git add .
```

#### **2) GIT ADD FILES STAGED AREA TO GIT REPO / COMMIT**

**commit msg**

```
    git commit -m " "
```

**skip staging area adding file/ directly add to repository and commit**

```
    git commit –am
```

**change commit and file/ redo**

```
    git commit --amend
```

#### **3) GIT LOG**

**log all commit's**

```
    git log
```

**log short commit ID and Message**

```
   git log --oneline
```

**log only full commit ID and Message**

```
    git log --pretty=oneline
```

**show all changes with the commit**

```
    git log -p
```

**show given number of commits with all changes**

```
    git log -p -2
```

**show details in a short in commit**

```
	git log –stat
```

**all history with all branch and commit/HEAD**

```
	git reflog
```

**all history with provide subcommand or file**

```
	git reflog show/expire/delete/exists fileName
```

**access lost commits and not shown in git log with specific period**

```
	git reflog branchName@{one.week.ago}
```

#### **4) GIT BRANCH VIEW**

**view branches in repository**

```
	git branch 
```

**view branches in repository with more information**

```
	 git branch –v
```

**view remote branches**

```
	  git branch -r
```

#### **5) GIT BRANCH CREATE AND DELETE**

**create new branch**

```
	git branch branchName
```

**delete branch**

```
	git branch -d branchName
```

#### **6) GIT SWITCH TO BRANCH / COMMIT (DETACH HEAD) / TAG**

**switch one branch to another branch**

```
    git switch branchName
```

**create and switch (-c = create)**

```
git switch -c branchName
```

**switch one branch to another branch**

```
    git checkout branchName
```

**switch remote branch**

```
    git checkout --track origin/branchName
```

**directly switch HEAD through the commit**

```
    git checkout commitID
```

**switch to before HEAD X no. commit**

```
    git checkout HEAD~X
```

**checkout these remote branch pointer**

```
    git checkout origin/master
```

**switch to tag with detached HEAD**

```
    git checkout tagName
```

**switch to other branch with X days ago first commit**

```
    git checkout branchName@{2.days.ago}
```
#### **7) GIT DIFFERENCE**

**Changes in our working directory/area**
```
git diff
git diff HEAD
```

Changes in staging area form last commit
```
git diff --staged / --cached
```

Changes within specific file
```
git diff HEAD / --staged fileName
```

Changes within tow branches or commit
```
git diff branchName..branchName
git diff commitName..commitName
git diff branchName@{X} branchName@{yesterday}
```

#### **8) GIT STASH Change branch without staging / don't need to add unnecessary commit**

**Stash files**
```
git stash
git stash -u
```

**Un-stash stashed files**
```
git stash pop
```

**View stashed list**
```
git stash list
```

**Apply stashed data to other branch or specific stash / merge content**
```
git stash apply
git stash apply stash@{X}
```

**Delete specific or clear all stash**
```
git stash drop stash@{X}
git stash clear
```










<h1 align="center"><img height="50" src="https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png" align="middle"/><br />Git-Notes</h1>
<p align="center">I like to maintain a cheatsheet of git commands which I frequently use. The repo contains the most used commands and a small info about them which will improve your productivity and save precious hours by randomly going through stackoverflow questions.<br /><br />Feel free to reach out to me! 😊 <br />
  <a href="https://www.instagram.com/bhavya_karia/">Instagram</a> || <a href="https://twitter.com/thebhavyakaria">Twitter</a> || <a href="https://www.linkedin.com/in/bhavya-karia-1b115a93/">LinkedIn</a> || <a href="https://bhavyakaria.github.io/">Blog</a>
 </p>


<h1 align="center">Contribution</h1>

<p align="center">This repository is contribution friendly😃. If you would like to improve or add some useful commands, your contribution is welcome!</p>

---

## Table Of Contents:

1. [Awesome place to learn git](#git_tutorials)
2. [Basic Terminologies](#basic_terminologies)
3. [Baisc Flow](#basic_flow)
4. [Git Branch](#git_branch_commands)
5. [Git Stash](#git_stash_commands)
6. [Miscellaneous](#miscellaneous)

<a name='git_tutorials'></a>
## Awesome places to learn git

1. [GitHub Learning Lab](https://lab.github.com/)
2. [Git Started with GitHub](https://www.udemy.com/course/git-started-with-github/)
3. [Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123)
4. [Atlassian Git Tutorial](https://www.atlassian.com/git)
5. [Lean Git Branching](https://learngitbranching.js.org/)

<a name='basic_terminologies'></a>
## Basic Terminologies

1. **git**: Git is a distributed version-control system for tracking changes in source code during software development.
2. **git clone**: To download an existing git repository on your local machine.
3. **git fetch**: It only downloads the new data from remote repository and does not integrate that data into working files.
4. **git pull**: It downloads the new data as well as merges it into the existing files.

<a name='basic_flow'></a>
## Basic flow

1. Adding git to a folder(Execute inside the project folder)<br />
```git init```

2. Adding and commiting project files<br />
```git add .```<br />
```git commit -m "commit message"```

3. Create a README.md file

4. Create a remote repository on Github/Gitlab/Bitbucket(Do not create README.md file here)

5. Linking your local repository to your remote repository<br />
```git remote add origin $URL_TO_YOUR_REMOTE_REPOSITORY```

6. Pushing local files to remote repository<br />
```git push origin master```

7. To fetch any changes made on remote repository to local repository<br />
```git pull origin master```

<a name='git_branch_commands'></a>
## Git Branch Commands

1. **Get list of branches on local**<br />
```git branch -a```

2. **Get list of branches on remote**<br />
```git branch -r```

3. **Create a branch**<br />
```git checkout -b $BRANCH_NAME```<br />
```git push origin $BRANCH_NAME```

4. **Get list of only local branches**<br />
```git branch -vv | cut -c 3- | awk '$3 !~/\[/ { print $1 }'```

5. **Display commit logs**<br />
```git log --oneline --graph --decorate --all```

6. **Rename a local branch**<br />
i. Renaming the current branch:<br />
```git branch -m $NEW_BRANCH_NAME```<br />
ii. Renaming some other branch:<br />
```git branch -m $OLD_BRANCH_NAME $NEW_BRANCH_NAME```<br />

7. **Rename a remote branch**<br />
i. First complete the above two steps.<br />
ii. Delete the old-name branch and push the new-name local branch:
```git push origin :$OLD_BRANCH_NAME $NEW_BRANCH_NAME```<br />
iii. Reset the upstream branch for new-name local branch
```git push origin -u $NEW_BRANCH_NAME```

8. **Delete a local branch**<br />
```git branch -d $BRANCH_NAME```<br />
```git branch -D $BRANCH_NAME```<br /><br />
-d stands for --delete, which will delete the local branch, only if you have already pushed and merged it with your remote branches.<br />
-D stands for --delete --force, which deletes the branch regardless of its push and merge status.

<a name='git_stash_commands'></a>
## Git Stash Commands

1. **Saving uncommited changes(both staged and unstaged) and making the working branch clean**<br />
```git stash```<br />

2. **Saving with a message**<br />
```git stash save $MESSAGE```<br />

3. **Checkout all the stash in your project**<br />
```git stash list```<br />

4. **Pasting the stash changes and remove it from list**<br />
```git stash pop```<br />

5. **Apply ths stash changes and also keep them in the list**<br />
```git stash apply```<br />

6. **Creating a branch from stash**<br />
```git stash branch $BRANCH_NAME```<br />

7. **Delete all your stash from the project**<br />
```git stash clear```<br />

8. **Remove a particular stash from the list**<br />
```git stash drop $STASH_ID```<br /> 


<a name='miscellaneous'></a>
## Miscellaneous

1. **Discarding unstaged changes**<br />
```git checkout -- .```

2. **Checkout conflict files**<br />
```git diff --name-status --diff-filter=U```



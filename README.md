# Git-Notes

## Table Of Contents:

1. [Awesome place to learn git](#git_tutorials)
2. [Basic Terminologies](#basic_terminologies)
3. [Baisc Flow](#basic_flow)
4. [Git Branch](#git_branch_commands)
5. [Miscellaneous](#miscellaneous)

<br />

<a name='git_tutorials'></a>
## Awesome places to learn git

1. [GitHub Learning Lab](https://lab.github.com/)
2. [Git Started with GitHub](https://www.udemy.com/course/git-started-with-github/)
3. [Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123)
4. [Atlassian Git Tutorial](https://www.atlassian.com/git)
5. [Lean Git Branching](https://learngitbranching.js.org/)

<br />

<a name='basic_terminologies'></a>
## Basic Terminologies

1. **git**: Git is a distributed version-control system for tracking changes in source code during software development.
2. **git clone**: To download an existing git repository on your local machine.
3. **git fetch**: It only downloads the new data from remote repository and does not integrate that data into working files.
4. **git pull**: It downloads the new data as well as merges it into the existing files.

<br />

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

<br />

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

<br />

<a name='miscellaneous'></a>
## Miscellaneous

1. **Discarding unstaged changes**<br />
```git checkout -- .```

2. **Checkout conflict files**<br />
```git diff --name-status --diff-filter=U```



# Git-Notes

### Awesome places to learn git

1. (GitHub Learning Lab)[https://lab.github.com/]
2. (Git Started with GitHub)[https://www.udemy.com/course/git-started-with-github/]
3. (Version Control with Git)[https://www.udacity.com/course/version-control-with-git--ud123]

### Basic Terminologies

1. **git**: Git is a distributed version-control system for tracking changes in source code during software development.
2. **git clone**: To download an existing git repository on your local machine.
3. **git fetch**: It only downloads the new data from remote repository and does not integrate that data into working files.
4. **git pull**: It downloads the new data as well as merges it into the existing files.

### Contains most commonly used git commands

#### Basic flow for creating a local git project and connecting it with a remote repository(Github | Gitlab | Bitbucket)

1. Adding git to a folder(Execute inside the project folder)

   ```git init```

2. Adding and commiting project files 

   ```git add .```<br />
   ```git commit -m "commit message"```

3. Create a README.md file

4. Create a remote repository on Github/Gitlab/Bitbucket(Do not create README.md file here)

5. Linking your local repository to your remote repository

   ```git remote add origin $URL_TO_YOUR_REMOTE_REPOSITORY```

6. Pushing local files to remote repository
  
   ```git push origin master```

7. To fetch any changes made on remote repository to local repository

   ```git pull origin master```


#### Get list of branches on local

```git branch -a```

#### Get list of branches on remote

```git branch -r```

#### Create a branch

```git checkout -b $BRANCH_NAME```<br />
```git push origin $BRANCH_NAME```

#### Display commit logs

```git log --oneline --graph --decorate --all```

#### Discarding unstaged changes

```git checkout -- .```

#### Checkout conflict files

```git diff --name-status --diff-filter=U```

#### Get list of only local branches

```git branch -vv | cut -c 3- | awk '$3 !~/\[/ { print $1 }'```


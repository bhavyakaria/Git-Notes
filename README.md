# Git-Notes
## Contains most commonly used git commands

### Basic flow for creating a local git project and connecting it with a remote repository(Github | Gitlab | Bitbucket)

1. Adding git to a folder(Execute inside the project folder)

   ```git init```

2. Adding and commiting project files 

   ```git add .```
   ```git commit -m "commit message"```

3. Create a README.md file

4. Create a remote repository on Github/Gitlab/Bitbucket(Do not create README.md file here)


### Get list of branches on local

```git branch -a```

### Get list of branches on remote

```git branch -r```

### Display commit logs

```git log --oneline --graph --decorate --all```

### Discarding unstaged changes

```git checkout -- .```

### Checkout conflict files

```git diff --name-status --diff-filter=U```

### Get list of only local branches

```git branch -vv | cut -c 3- | awk '$3 !~/\[/ { print $1 }'```


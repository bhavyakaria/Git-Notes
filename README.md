# Git-Notes
## Contains most commonly used git commands

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

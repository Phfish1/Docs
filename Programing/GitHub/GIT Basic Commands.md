### Save your progress

1. Initialize Git repository
``` git
$ git init
```

2. Add files to git repository(folder)
``` git
$ git add *
```

3. Commits what you added to your working branch `master`
``` git
$ git commit -m "COMMENT"
```

___

### See what you doing

See your commit status ++
``` git
$ git status
```

Logs everything you do. **Project History**
``` git
$ git log
```

___
# Working with branches
___

Shows you what branch you are in. And adds other branches if name is specified
``` git
$ git branch [new-branch]
```

Checkout/use other branches. Or refer to an older commit/save using the longest output from the `git log` command. eg(`$ git checkout fcba7c13aa6e714d4fd4e3cd5d01b28ece116e84`)
``` git
$ git checkout BRANCH
```

### Merging

Merges the Extra branch(BRANCH2) to the main/MASTER branch
``` git
$ git merge MASTER BRANCH2
```

### Reverting

Reverts a commit. eg(`343543f5a577ebf8d2802f8459e152900d5d1b54` removed file index.html.) "adds index.html" again 
``` git
$ git revert 343543f5a577ebf8d2802f8459e152900d5d1b54
```

___
# Upload it to GitHub
___

Hooks your repository to GitHub
``` git
$ git remote add origin https://github.com/USER/REPOSITORY.git
```

Pushes the branch **master** to the website hook of **origin**
``` git
$ git push -u origin master 
```
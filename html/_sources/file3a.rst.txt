Git Cheat Sheet
===============

*taken from https://gist.github.com/fogleman/*

This attempts to be a useful "cheat sheet" for git.  I'm just writing git recipes down here as I find and use them.

Getting Code
------------

**Clone a repository (GitHub)**
```
git clone git@github.com:username/repository.git
```

**Checkout a branch into your working tree**
```
git checkout branchname
```

Dealing with the Working Tree
-----------------------------
**Delete untracked files in your working tree**

```
git clean -f      # Remove untracked files
git clean -f -d   # Also directories
git clean -f -x   # Also ignored files
git clean -f -X   # Just ignored files
```

**Restore to the HEAD of your current branch**
This is a good way to abort a merge in progress
```
git reset --hard HEAD
```
**Restore a file from an old revision**
```
git checkout [commit_id] -- path/to/oldfile
```

Branches
--------
**Delete a local branch**
```
git branch -d branchname
```

**Push a new branch for the first time**
```
git push -u origin branchname
```

Tags
----
**Create an annotated tag**

Annotated tags are more rich than regular tags, and include date/author information.
```
git tag -a [tagname] -m "Tag Message..."
```
**Checkout a tag**
```
git checkout [tagname]
```

The History, and Logs
---------------------
**View the commit history, showing the status of files that changed**
```
git log --stat
```

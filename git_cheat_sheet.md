## Git Cheat sheet


### Some tools to have

Use Atom editor to preview Markdown files.

### Configuring Git

Make code changes more visible:

```
git config --global color.ui true
```

Merging code: you can install Meld: http://www.meldmerge.org/


### Use scenarios

#### Get files and update in remote master branch

The simplest way to use git, use this when you want to work alone directly in master.

- Getting files from a remote branch (first time). This will download the repo in your machine.
```
git clone <repo url>
```


- Update the branch in local repository, getting contents from remote. Go to the repository and then do:
```
git pull
```


- Change files in your local repo. Here you update your code.

- Add ALL changes to the commit. This adds all changes made to the next commit (commits are atomic), including file deletions.
```
git add -A
```

- Commit changes in the local repo.
```
git commit -m "updated"
```

to put a message
```
git commit --message "I worked a lot"
```

- Push to remote repo
```
git push
```

- And you can check the status of the repository doing:

git status





# Create repo local
```
git init

git add .gitignore
```


# create a branch and go to this branch
```
git branch mydevbranch

git checkout mydevbranch
```

# list branches (all)
```
git branch -a
```


# lists all files
```
git ls-tree --full-tree -r HEAD
```

# Get the commit log

This will get the last 2 commit entries

```
git log -2
```

# Get a specific version, copying to another location

Go to the repo misc and create a work tree in the same level
```
git worktree add ../misc2
```

```
git --work-tree=../misc2 checkout a06c1177df71e7ad36e8749c72007ef0a6fe9c98 -- .
```


#### Reference
http://kbroman.org/github_tutorial/pages/init.html
https://stackoverflow.com/questions/12370714/git-how-do-i-list-only-local-branches/12370765

https://stackoverflow.com/questions/16122234/how-to-commit-a-change-with-both-message-and-description-from-the-command-li

https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History

https://stackoverflow.com/questions/8533202/list-files-in-local-git-repo

https://coderwall.com/p/lz0uva/find-all-files-modified-between-commits-in-git

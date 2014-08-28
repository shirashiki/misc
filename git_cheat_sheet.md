## Git Cheat sheet

### Configuring Git

- Make code changes more visible:
`git config --global color.ui true`

### Use scenarios

#### Get files and update in remote master branch

The simplest way to use git, use this when you want to work alone directly in master.

- Update the branch in local repository, getting contents from remote.Go to the repository and then do:

`$ git pull`

- Change files in your local repo. Here you update your code.

- Add ALL changes to the commit. This adds all changes made to the next commit (commits are atomic), including file deletions.

`$ git add -A`

- Commit changes in the local repo.

`$ git commit -m 'This is a change comment'`

- Push to remote repo

`$ git push`

- And you can check the status of the repository doing:

$ git status

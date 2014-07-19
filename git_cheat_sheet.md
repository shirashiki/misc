# Git Cheat sheet

## Scenario 1: Changing directory to master branch of repository

Update the branch in local repository, getting contents from remote
Go to the repository and then do:
$ git pull

Then suppose you change files and want to commit them. First you do:
$ git add -A

This adds all changes made to the next commit (commits are atomic), including file deletions.

Now you can commit:
$ git commit -m 'This is a change comment'

Note you committed the local repository. In order to send changes, you need to push them:
$ git push


And lets do a merge

=======
And you can check the status of the repository doing
$ git status



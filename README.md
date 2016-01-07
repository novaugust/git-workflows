# git-workflows
A meetup on github workflows


## Commits

```
A basic summary of the commit and what it does

Close #1, Close #3, Ref #10
- other change i made
- some minor thing
- woohoo
```

- take advantage of GH features (close #1, etc)
- clean up your history (rebase... to one commit

## Issues

- whenever there's a problem
- close them ~~only~~ mostly via pull request

## Branches

- never commit to master
- always work on Branches
- `git checkout -b <branch_name>`

## Scenarios

### I solved a problem

- Great!!!!!
- there should be an issue for it
- squash down to one commit
  `git rebase -i` (for interactive)
  `git rebase -i HEAD~<# of commits>`
- push it up
- open a pull request

### I solved a problem, but wrong.

- `git commit --amend`

### I solved a problem, but someone else changed my code

IE, someone else made changes where i made changes... and the button
won't turn green.

- get caught up to master
  1. `git checkout master`
  2. `git pull upstream master`
  3. `git checkout <my_branch>`
  4. `git rebase master`

### I forgot to add tests

- see "i didn't solve the problem"


### Working on issues blocked on pull requests

- branch off your branch

#### Things go right
- you didn't need to change the original branch you branched off of
  (aka, you got it right the first time)
- rebase like normal (someone else changed the code problem)

#### Things go wrong

- you had to change the branch you branched from.
- temp branch dance with some cherry picking

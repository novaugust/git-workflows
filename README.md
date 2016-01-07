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

- great!!!!!
- there should be an issue for it
- squash down to one commit
  `git rebase -i` (for interactive)
  `git rebase -i HEAD~<# of commits>`
- push it up
- open a pull request

### I solved a problem, but wrong.

- `git commit --amend`

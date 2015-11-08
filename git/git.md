# Git

Merge creates a new commit with two parents

git add -p
git pull --rebase


# Git workflow
Git is a communication tool. A tool for communicating code with oneself and others.

One branch, usually master, that is always in a production ready state.
Never force push, change the workflow to avoid ever doing this.
Every commit should pass tests
Linear history: clean, easier to find bugs, merge code

Types of branches:
  feature
  bugfix
  hotfix
  refactor


branch -> work -> acceptance test/code review(CI server) -> merge into production/release branch


can use cherry pick or merge workflow


during rebase
local is master
remote is the branch being rebase on master

# Git

## Install Git (+ Git Bash)

https://git-scm.com/downloads

## Open Git Bash

Right mouse button in folder > open git bash

## Clone Repository

```bash
git clone [repolink]
```

## Git status

```bash
git status
```

## Pull Repository

```bash
git fetch
git pull
```

## Branch

Github:


Bash:
see all branches:
```bash
git branch --list
git branch -a
```

Local new branch
```bash
git branch [newbranch]
```

Remote new branch
```bash
git push origin [branch]
```

## Checkout to new branch
Change your local branch to another branch

## Fork

```bash
git fetch
git checkout [branch]
```

## Commit Changes

```bash
git add .
git commit -m "[message]"
git push
```
## Commit Message Standards

First Word | Meaning
--- | ---
`Added ...` | Created a capability e.g. feature, test, dependency.
`Updated ...` | Worked on or updated a capability e.g. feature, test, dependency.
`Fixed ...` | Fixed an issue e.g. bug, typo, accident, misstatement.
`Removed ...` | Removed a capability e.g. feature, test, dependency.
`Refactored ...` | A code change that MUST be just a refactoring.
`Reformatted ...` | Refactor of formatting, e.g. omit whitespace.
`Optimized ...` | Refactor of performance, e.g. speed up code.
`Documented ...` | Refactor of documentation, e.g. help files.

## Pull Request / Merge

## Fetch Upstream
# 1. Version control

## a. Git

- Commit: git commit -m "first commit"

- Push: local -> remote

- Pull: remote -> local

- Branch

## b. GitFlow

- 5 branchs:

+ Master: Contains stable code that has been released, only receives merges from release/* or hotfix/* branches.

+ Develop: Used for new feature development. All feature/* and hotfix/* branches are merged here once complete, when preparing for a release, a release/* branch is created from this.

+ Feature/*: Each feature/xxx branch is for developing a single new feature. Created from develop, and merged back into develop when done.

+ Release/*: Created from develop when preparing for a new release version. Used for final testing, minor bug fixes, updating version numbers and changelogs. After release, merged into both main and develop.

+ Hotfixes/*: Created directly from main to fix urgent issues in production. After fixing, merged back into both main and develop.

- Gitflow workflow
  
![](https://nvie.com/img/git-model@2x.png)

## c. Conventional commits 

A successful Git branching model: <type>(<scope>): <message>

- Popular types: feat, fix, docs, style, refactor, test, chore

- Scope: the part that describes the scope of the commit

- Git commit message lint: the process of checking and ensuring your commit message follows a Conventional commits. <Extension `Conventional Commits`>

# 2. System architecture

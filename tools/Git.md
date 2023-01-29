Git is an open source version control system, which supports your development tasks, especially in distributed code projects.

---
## Installation


## Configuration


## Using Git

The following commands can be helpful for working with `git`.






## Change GitHub default branch from master to main

### Step 1: create main branch locally, taking the history from master

The argument `-m` transfers all of the commit history

```bash
git branch -m master main
```

### Step 2: push the new local main branch to the remote repo (GitHub)

```bash
git push -u origin main
```


### Step 3: switch the current HEAD to the main branch

```bash
git symbolic-ref refs/remotes/origin/HEAD refs/remotes/origin/main
```


### Step 4: change the default branch on GitHub to main

https://docs.github.com/en/github/administering-a-repository/setting-the-default-branch

### Step 5: delete the master branch on the remote

```bash
git push origin --delete master
```
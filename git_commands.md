`git init` - Initializes a new Git repository in the current directory.

`git clone <repo-url>` - Creates a copy of a remote repository locally.

`git status` - Shows the status of changes in the working directory.

`git add <file>` - Stages a specific file for the next commit.

`git add .` - Stages all changes in the directory for commit.

`git commit -m "message"` - Commits staged changes with a message.

`git log` - Displays the commit history.

`git diff` - Shows changes between working directory and the index.

`git branch` - Lists all local branches.

`git branch <name>` - Creates a new branch.

`git checkout <branch>` - Switches to another branch.

`git checkout -b <branch>` - Creates and switches to a new branch.

`git merge <branch>` - Merges a branch into the current branch.

`git pull` - Fetches and merges changes from the remote repository.

`git push` - Pushes local commits to the remote repository.

`git push --set-upstream origin <new-local-branch-name>` - Creates a new branch from local to remote and push the commits.

`git reset <file>` - Unstages a file while retaining changes.

`git reset --hard` - Resets working directory and index to the last commit.

`git stash` - Temporarily shelves changes not ready to commit.

`git stash pop` - Applies stashed changes and removes them from stash list.

`git remote -v` - Displays the remote URL(s) associated with the repository.

`git config --global user.name "Your Name"` - Sets global Git username.

`git config --global user.email "email@example.com"` - Sets global Git email.

### Advance level

`git reflog` - Shows a log of all references (branch HEAD movements), including rebased or reset commits.

`git cherry-pick <commit>` - Applies the changes from a specific commit on top of your current branch.

`git rebase <branch>` - Reapplies commits from your current branch on top of another (used to linearize history).

`git rebase -i HEAD~<n>` - Interactively modify (squash, edit, drop) the last n commits.

`git stash list` - Lists all stashed changes.

`git stash apply <stash>` - Applies a specific stash without deleting it.

`git stash drop <stash>` - Deletes a specific stash entry.

`git clean -fd` - Removes untracked files and directories (⚠️ destructive).

`git remote add <name> <url>` - Adds a new remote repository.

`git remote remove <name>` - Removes a remote.

`git fetch origin <branch>` - Fetches a specific branch from the remote.

`git revert <commit>` - Creates a new commit that reverses the specified commit (safe undo).

`git bisect start` - Begins a binary search to find the commit that introduced a bug.

`git submodule add <repo-url> <path>` - Adds a Git submodule to your repo.

`git submodule update --init` - Initializes and updates all submodules.

`git blame <file>` - Shows who made each change line-by-line in a file.

`git archive --format=zip HEAD > code.zip` - Creates a zip archive of the current repository state.

`git shortlog -sn` - Summarizes commit count per contributor.

`git tag -a <tag> -m "msg"` - Creates an annotated tag with a message.

`git push origin --tags` - Pushes all tags to the remote repository.


### Here's your step-by-step DevOps-ready guide to:

✅ Clone a GitHub repo into VS Code,

✅ Create a local branch,

✅ Work on it,

✅ Push changes back to GitHub on the new branch.

`git clone <repo-url>`

`cd repo-name`

`git checkout -b feature/my-new-branch`

`git add .`

`git commit -m "My changes"`

`git push -u origin feature/my-new-branch`


# Git Scenarios with Commands

### Undo local changes to a file
```bash
git checkout -- filename
```

### Undo a commit that hasn’t been pushed
```bash
git reset --soft HEAD~1
```

### Undo a pushed commit safely (create a reverse commit)
```bash
git revert <commit-hash>
```

### Delete a local branch
```bash
git branch -d feature/old-branch
```

### Delete a remote branch
```bash
git push origin --delete feature/old-branch
```

### See who changed a specific line in a file
```bash
git blame filename
```

### See all commits on a branch
```bash
git log --oneline
```

### Switch back to main/master
```bash
git checkout main
```

### Test a bug fix without losing current work
```bash
git stash
# do your fix
git stash pop
```

### Link your local repo to a new remote
```bash
git remote add origin https://github.com/user/repo.git
```

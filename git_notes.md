# Notes about getting started with git and Github as a junior developer

## Terminology:

- **Origin**: The primary remote repository. It's the default name Git gives to the server you cloned from.
- **Remote**: The version of your project hosted on a server somewhere.
- **Branch**: A parallel version of a repository. It is contained within the repository but does not affect the primary or main branch.
- **Clone**: To make a copy of a repository on your local computer.
- **Pull**: Fetching in changes from the remote repository.
- **Pull Request**: The action of validating a code change and merging it into the branch of a codebase.
- **Fork**: A personal copy of another user’s repository that lives on your account. Changes don’t affect the original.
- **Merge**: Combining a branch’s changes into the main branch.
- **HEAD**: A pointer to the current branch reference, i.e., the last commit.
- **Upstream**: If you clone a repository from a location, that location is set to be the “upstream”.
- **Tag**: A pointer to a specific commit.
- **Checkout**: The act of switching between files/commits/branches.
- **Stash**: Saves changes you don’t want to commit immediately.
- **Rebase**: The process of moving/combining a sequence of commits into a new base commit. It's used to integrate changes from one branch into another.

## Commands:

### Setting Up and Configuring Repositories

- **`git remote add origin https://github.com/user/repo.git`**: Add a new remote repository to your local Git repository to associate your local Git repo with a remote repo.

- **`git remote set-url origin git@github.com:user/repo.git`**: If the URL/username of an existing repository has changed and you want to update it, or you want to switch from HTTPS to SSH.

- **`ssh -T git@github.com`**: Check SSH authentication.

- **`git init`**: Initialize a new Git repository.

- **`git config --global init.defaultBranch main`**: Set the default branch name for new repositories.


### Working with Branches

- **`git branch`**: List all the branches.

- **`git branch <branchname>`**: Create a new branch.

- **`git switch <branchname>`**: Switch to a branch.

- **`git switch -c <branchname>`**: Create and switch to a new branch.

- **`git branch -d <branchname>`**: Delete a branch.

- **`git branch -m <newbranchname>`**: Rename a branch.

- **`git branch -M <newbranchname>`**: Rename a branch even if the new branch name already exists.

- **`git branch -r`**: List remote branches.

- **`git branch -a`**: List both local and remote branches.

### Updating and Publishing Changes

- **`git add .`**: Stage all changes in the directory.

- **`git commit -m 'commit msg'`**: Commit the staged changes with a message.

- **`git push -u origin main`**: Push changes to the remote repository and set the upstream for your current branch. In the future, you can simply use `git push` or `git pull` without specifying the branch, and Git will know `origin main`.

- **`git pull --rebase origin main`**: Fetch the changes from the remote and rebase your current branch on top of the remote main branch.

### Miscellaneous

- **`git remote -v`**: Check the remote repository URL.

- **`git fetch origin`**: Update your local repository with changes from the remote without merging them into your current branch.

- **`git merge <branchname>`**: Integrate changes from another branch into the main branch.

- **`git merge --abort`**: Stop the merge process.

- **`git stash`**: Temporarily shelves changes so you can work on a different task.

- **`git stash pop`**: Applies stashed changes back to your working directory.

- **`git revert <commit>`**: Creates a new commit that undoes the changes made in a specific commit.

- **`git reset`**: Resets your index and working directory to the state of a specific commit. Use with caution.

- **`git rebase -i <commit>`**: Start an interactive rebase session to modify commits from a specific point.

### Enhancing Workflow with Git

- **`git status`**: Shows the status of changes as untracked, modified, or staged.
- **`git log`**: Displays the commit history for the current branch, showing the author, date, and commit message.
- **`git diff`**: Shows the differences between your working directory and the index (staged changes) or between any two commits.
- **`git show <commit>`**: Displays metadata and content changes of the specified commit.
- **`git fetch --all`**: Fetches changes from all remote repositories and branches.
- **`git pull --all`**: Fetches changes from all branches from the remote repository and merges them into the current branch.
- **`git push --all`**: Pushes all local branches to the remote repository.
- **`git reset --hard <commit>`**: Resets the current branch to the specified commit, discarding all changes in the working directory and index.
- **`git reset --soft <commit>`**: Moves the current branch to the specified commit, but leaves your working directory and index (staged changes) as they were.
- **`git stash list`**: Lists all stashed changes.
- **`git stash apply`**: Applies the most recently stashed changes without removing them from the stash list.
- **`git stash drop`**: Removes the most recent stash from the stash list.
- **`git tag -a <tagname> -m "message"`**: Creates an annotated tag with a message.
- **`git tag`**: Lists all tags.
- **`git show <tag>`**: Shows the commit that a tag is pointing to along with the tag message.


### GitHub CLI (`gh`)

- **`gh repo create my-new-repo --public --description "My new repository"`**: Create a new repository on GitHub from the command line.
- **`gh pr list`**: Lists pull requests in the current repository.
- **`gh pr checkout <pr-number>`**: Checks out a pull request locally for review or testing.
- **`gh pr create`**: Creates a new pull request.
- **`gh pr merge <pr-number>`**: Merges a pull request.
- **`gh issue create`**: Creates a new issue in the current repository.
- **`gh issue list`**: Lists issues in the current repository.
- **`gh issue view <issue-number>`**: Views details of the specified issue.




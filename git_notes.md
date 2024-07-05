# Git Terminology and Commands

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

- **`git checkout <branchname>`**: Switch to a branch.

- **`git checkout -b <branchname>`**: Create and switch to a new branch.

- **`git branch -d <branchname>`**: Delete a branch.

- **`git branch -m <newbranchname>`**: Rename a branch.

- **`git branch -M <newbranchname>`**: Rename a branch even if the new branch name already exists.

- **`git branch -r`**: List remote branches.

- **`git branch -a`**: List both local and remote branches.

### Updating and Publishing Changes

- **`git add .`**: Stage all changes in the directory.

- **`git commit -m “commit msg”`**: Commit the staged changes with a message.

- **`git push -u origin main`**: Push changes to the remote repository and set the upstream for your current branch. In the future, you can simply use `git push` or `git pull` without specifying the branch, and Git will know `origin main`.

- **`git pull —rebase origin main`**: Fetch the changes from the remote and rebase your current branch on top of the remote main branch.

### Miscellaneous

- **`git remote -v`**: Check the remote repository URL.

- **`git fetch origin`**: Update your local repository with changes from the remote without merging them into your current branch.

- **`git merge <branchname>`**: Integrate changes from another branch into the main branch.

- **`git merge —abort`**: Stop the merge process.

### GitHub CLI (`gh`)

- **`gh repo create my-new-repo --public --description "My new repository"`**: Create a new repository on GitHub from the command line.
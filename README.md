# Learning Git and Github

# Git Workflow

The typical Git workflow involves three main areas:

1. Local (Working Directory)

- This is where your files live on your local machine. It's the directory you're working in, where you make changes to your code, documents, etc.
- Add, edit, or delete files.

2. Staging Area

- A temporary area where Git records your changes before you commit them (preview of next commit).
- You "stage" your changes using git add, which tells Git to include those changes in the next commit.

3. Repository

- The permanent store of your project. It's where all the committed changes are stored, tracked, and managed.
- You commit your changes (with git commit), which moves them from the staging area to the repository.

# Commands

## **Basic Commands**

**`git status`**
- Show current changes.
- Use `-s` for compact output.

**`git add`**
- Stage files (e.g., `git add .` to stage all changes).
- Be cautious with `.` as it stages everything recursively.

**`git commit -m "message"`**
- Commit staged changes with a message.
- Use `git commit -am "message"` to skip staging for modified files.

**`git rm <file>`**
- Remove file from working directory and staging.
- Use `--cached` to only remove it from Git, not locally.

**`git mv <source> <destination>`**
- Rename or move a file.

**`git restore --staged <file>`**
- Unstage a file.
- `--source=HEAD~#` restores from a specific commit.

**`git clean -f`**
- Delete untracked files or directories.

**`git ls-files`**
- List all tracked files (staged and committed).

**`git diff`**
- Show changes between working directory and staging.
- Use `--staged` to see changes between staging and last commit.

**`git difftool`**
- Use an external diff tool (after setup).

**`git log`**
- Show commit history.
- `--oneline` shows a summary per commit.

**`git show <hash>`**
- Show details of a specific commit.
- Use `HEAD~#` to show commits prior to the latest.

## **Branching Commands**

**`git branch <name>`**
- Create a new branch.
- Use `-m <old> <new>` to rename, and `-d <branch>` to delete.

**`git checkout <branch>`**
- Switch to another branch.
- Use `-b <branch>` to create and switch, and `--track <remote>/<branch>` to track a remote branch.

**`git switch <branch>`**
- Preferred method to switch branches (since Git 2.23).
- `-c <branch>` to create and switch, `--track` to track remote.

**`git push`**
- Upload commits to remote.
- `-u origin <branch>` to set up tracking.
- Delete remote branch with: `git push origin --delete <branch>`.

**`git pull`**
- Fetch and merge remote changes into the current branch.

**`git merge <branch>`**
- Merge another branch into your current branch.

**`git rebase <branch>`**
- Reapply your commits on top of another branch for cleaner history (linear).

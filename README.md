
# Git Cheat Sheet

Welcome to the Git Cheat Sheet! This guide covers essential Git commands and concepts, helping you manage your code repositories effectively.

---

## 1. Git Configuration

### Git Config
- Set the name:
  ```sh
  $ git config --global user.name "User name"
  ```
- Set the email:
  ```sh
  $ git config --global user.email "himanshudubey481@gmail.com"
  ```
- Set the default editor:
  ```sh
  $ git config --global core.editor Vim
  ```
- Check the settings:
  ```sh
  $ git config -list
  ```

### Git Alias
Set up an alias for each command:
- Checkout:
  ```sh
  $ git config --global alias.co checkout
  ```
- Branch:
  ```sh
  $ git config --global alias.br branch
  ```
- Commit:
  ```sh
  $ git config --global alias.ci commit
  ```
- Status:
  ```sh
  $ git config --global alias.st status
  ```

---

## 2. Starting a Project

### Git Init
Create a local repository:
  ```sh
  $ git init <Repo Name>
  ```

### Git Clone
Make a local copy of the server repository:
  ```sh
  $ git clone <remote Url>
  ```

---

## 3. Local Changes

### Git Add
Add a file to the staging (Index) area:
  ```sh
  $ git add <Filename>
  ```
Add all files of a repo to the staging (Index) area:
  ```sh
  $ git add *
  ```

### Git Commit
Record or snapshot the file permanently in the version history with a message:
  ```sh
  $ git commit -m "Commit Message"
  ```

---

## 4. Track Changes

### Git Diff
Track the changes that have not been staged:
  ```sh
  $ git diff
  ```
Track the changes that have been staged but not committed:
  ```sh
  $ git diff --staged
  ```
Track the changes after committing a file:
  ```sh
  $ git diff HEAD
  ```
Track the changes between two commits:
  ```sh
  $ git diff <commit1-sha> <commit2-sha>
  ```
Git Diff Branches:
  ```sh
  $ git diff <branch1> <branch2>
  ```

### Git Status
Display the state of the working directory and the staging area:
  ```sh
  $ git status
  ```

### Git Show
Show objects:
  ```sh
  $ git show <options> <objects>
  ```

---

## 5. Commit History

### Git Log
Display the most recent commits and the status of the head:
  ```sh
  $ git log
  ```
Display the output as one commit per line:
  ```sh
  $ git log --oneline
  ```
Display the files that have been modified:
  ```sh
  $ git log --stat
  ```
Display the modified files with location:
  ```sh
  $ git log -p
  ```

### Git Blame
Display the modification on each line of a file:
  ```sh
  $ git blame <file name>
  ```

---

## 6. Ignoring Files

### .gitignore
Specify intentionally untracked files that Git should ignore:
- Create .gitignore:
  ```sh
  $ touch .gitignore
  ```
- List the ignored files:
  ```sh
  $ git ls-files -i --exclude-standard
  ```

---

## 7. Branching

### Git Branch
- Create a branch:
  ```sh
  $ git branch <branch name>
  ```
- List branches:
  ```sh
  $ git branch --list
  ```
- Delete a branch:
  ```sh
  $ git branch -d <branch name>
  ```
- Delete a remote branch:
  ```sh
  $ git push origin --delete <branch name>
  ```
- Rename a branch:
  ```sh
  $ git branch -m <old branch name> <new branch name>
  ```

### Git Checkout
- Switch to a particular branch:
  ```sh
  $ git checkout <branch name>
  ```
- Create a new branch and switch to it:
  ```sh
  $ git checkout -b <branch name>
  ```
- Checkout a remote branch:
  ```sh
  $ git checkout <remote branch>
  ```

### Git Stash
- Stash current work:
  ```sh
  $ git stash
  ```
- Save stashes with a message:
  ```sh
  $ git stash save "<Stashing Message>"
  ```
- Check the stored stashes:
  ```sh
  $ git stash list
  ```
- Re-apply the changes that you just stashed:
  ```sh
  $ git stash apply
  ```
- Track the stashes and their changes:
  ```sh
  $ git stash show
  ```
- Re-apply the previous commits:
  ```sh
  $ git stash pop
  ```
- Delete the most recent stash from the queue:
  ```sh
  $ git stash drop
  ```
- Delete all the available stashes at once:
  ```sh
  $ git stash clear
  ```
- Stash work on a separate branch:
  ```sh
  $ git stash branch <branch name>
  ```

### Git Cherry-pick
Apply the changes introduced by some existing commit:
  ```sh
  $ git cherry-pick <commit id>
  ```

---

## 8. Merging

### Git Merge
- Merge the branches:
  ```sh
  $ git merge <branch name>
  ```
- Merge the specified commit to the currently active branch:
  ```sh
  $ git merge <commit>
  ```

### Git Rebase
- Apply a sequence of commits from distinct branches into a final commit:
  ```sh
  $ git rebase <branch name>
  ```
- Continue the rebasing process:
  ```sh
  $ git rebase --continue
  ```
- Abort the rebasing process:
  ```sh
  $ git rebase --skip
  ```

### Git Interactive Rebase
Allow various operations like edit, rewrite, reorder, and more on existing commits:
  ```sh
  $ git rebase -i
  ```

---

## 9. Remote

### Git Remote
- Check the configuration of the remote server:
  ```sh
  $ git remote -v
  ```
- Add a remote for the repository:
  ```sh
  $ git remote add <short name> <remote URL>
  ```
- Fetch the data from the remote server:
  ```sh
  $ git fetch <Remote>
  ```
- Remove a remote connection from the repository:
  ```sh
  $ git remote rm <destination>
  ```
- Rename the remote server:
  ```sh
  $ git remote rename <old name> <new name>
  ```
- Show additional information about a particular remote:
  ```sh
  $ git remote show <remote>
  ```
- Change remote:
  ```sh
  $ git remote set-url <remote name> <new URL>
  ```

### Git Origin Master
- Push data to the remote server:
  ```sh
  $ git push origin master
  ```
- Pull data from the remote server:
  ```sh
  $ git pull origin master
  ```

---

## 10. Pushing Updates

### Git Push
- Push data to the remote server:
  ```sh
  $ git push origin master
  ```
- Force push data:
  ```sh
  $ git push <remote> <branch> -f
  ```
- Delete a remote branch by push command:
  ```sh
  $ git push origin --delete <branch>
  ```

---

## 11. Pulling Updates

### Git Pull
- Pull the data from the server:
  ```sh
  $ git pull origin master
  ```
- Pull a remote branch:
  ```sh
  $ git pull <remote branch URL>
  ```

### Git Fetch
- Download branches and tags from one or more repositories:
  ```sh
  $ git fetch <repository URL>
  ```
- Fetch a specific branch:
  ```sh
  $ git fetch <branch URL> <branch name>
  ```
- Fetch all the branches simultaneously:
  ```sh
  $ git fetch --all
  ```
- Synchronize the local repository:
  ```sh
  $ git fetch origin
  ```

---

## 12. Undo Changes

### Git Revert
- Undo the changes:
  ```sh
  $ git revert
  ```
- Revert a particular commit:
  ```sh
  $ git revert <commit-ish>
  ```

### Git Reset
- Reset the changes:
  ```sh
  $ git reset --hard
  ```
  ```sh
  $ git reset --soft
  ```
  ```sh
  $ git reset --mixed
  ```

---

## 13. Removing Files

### Git Rm
- Remove the files from the working tree and from the index:
  ```sh
  $ git rm <file name>
  ```
- Remove files from Git but keep the files in your local repository:
  ```sh
  $ git rm --cached <file name>
  ```

---

Created by: **Barath kumar**

Feel free to contribute and improve this cheat sheet by creating pull requests or opening issues.

---

Happy Gitting!

---

*Note: The commands and concepts listed here are essential for working with Git. For comprehensive usage and additional options, refer to the [Git

 documentation](https://git-scm.com/doc).*

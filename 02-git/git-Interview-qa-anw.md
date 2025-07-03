# Git Interview Questions and Answers

## Beginner Level

**Q1: What is Git?**  
A1: Git is a distributed version control system that helps developers manage and track changes to their codebase. It allows multiple developers to work on a project simultaneously and facilitates collaboration by providing features such as branching, merging, and conflict resolution.

**Q2: What is a repository in Git?**  
A2: A repository, often referred to as a "repo," is a central location where Git stores all the files and directories of a project, along with their complete history. It contains the entire version history of the project, including all the commits and branches.

**Q3: How do you create a new Git repository?**  
A3: To create a new Git repository, you can navigate to the desired directory in your terminal and use the command `git init`. This command initializes a new empty Git repository in the current directory.

**Q4: What is the difference between Git and GitHub?**  
A4: Git is a version control system, while GitHub is a web-based hosting service for Git repositories. Git is the technology that allows you to manage and track changes in your codebase, whereas GitHub provides a platform to store, collaborate, and share Git repositories with others.

**Q5: What is the purpose of the "git clone" command?**  
A5: The `git clone` command is used to create a local copy of a remote Git repository. It downloads the entire repository, including all its files, commit history, and branches, to your local machine.

**Q6: How do you commit changes in Git?**  
A6: To commit changes in Git, you need to follow these steps:
1. Use the command `git add <filename>` to stage the changes you want to include in the commit.
2. Use the command `git commit -m "Commit message"` to create a new commit with the staged changes. The commit message should provide a brief description of the changes.

**Q7: What is the difference between "git pull" and "git fetch"?**  
A7:  
- `git pull` is a combination of two commands: `git fetch` and `git merge`. It fetches the latest changes from the remote repository and automatically merges them with the local branch.  
- `git fetch` only downloads the latest changes from the remote repository, but it doesn't automatically merge them. It updates the remote-tracking branches, allowing you to review the changes before merging.

**Q8: How do you resolve merge conflicts in Git?**  
A8: When a merge conflict occurs, it means that Git is unable to automatically merge the changes from different branches. To resolve the conflict, you need to manually edit the conflicting files to choose the desired changes. After resolving the conflicts, you can use the `git add` command to stage the changes, followed by `git commit` to complete the merge.

**Q9: How do you revert a commit in Git?**  
A9: To revert a commit in Git, you can use the `git revert` command followed by the commit hash of the commit you want to revert. This command creates a new commit that undoes the changes introduced by the specified commit, effectively reverting it.

**Q10: How do you push changes to a remote Git repository?**  
A10: To push changes to a remote Git repository, you can use the `git push` command followed by the name of the remote repository and the branch you want to push. For example, `git push origin main` pushes the local commits to the "main" branch of the remote repository named "origin."

> These are just a few common Git interview questions for beginners. Remember to practice using Git commands and workflows to strengthen your understanding of version control and collaboration with Git.

---

## Intermediate Level

**Q1: What is the difference between a branch and a tag in Git?**  
A1: In Git, a branch is a lightweight movable pointer to a specific commit. It allows for parallel development and isolates changes from each other. Developers can create new branches to work on new features or bug fixes. On the other hand, a tag is a reference to a specific commit that is used to mark a significant point in the project's history, such as a release or a stable version.

**Q2: How do you merge two branches in Git?**  
A2: To merge two branches in Git, you typically follow these steps:  
1. Switch to the branch where you want to merge changes (e.g., `git checkout branch-to-merge-into`).  
2. Run the command `git merge branch-to-merge-from`. This merges the changes from the specified branch into the current branch.  
3. Resolve any merge conflicts, if they occur.  
4. Commit the merge changes using `git commit`.

**Q3: What is the purpose of "git rebase"?**  
A3: Git rebase is a command used to integrate changes from one branch onto another by moving or combining commits. It is an alternative to merging and allows for a cleaner commit history. With rebase, you can apply a series of commits from one branch onto another, resulting in a linear commit history.

**Q4: How do you undo the most recent commit in Git?**  
A4:  
- You can use the command `git revert HEAD` to create a new commit that undoes the changes introduced by the last commit.  
- Alternatively, you can use `git reset HEAD~1` to move the branch pointer back one commit, effectively removing the last commit. This operation discards the commit and any changes associated with it.

**Q5: What is the "git stash" command used for?**  
A5: The `git stash` command allows you to temporarily save changes that are not ready to be committed yet. It's useful when you need to switch to a different branch or apply a hotfix but don't want to commit incomplete work. You can later retrieve the changes from the stash using `git stash apply` or `git stash pop`.

**Q6: How do you revert a file to a previous commit in Git?**  
A6: To revert a file to a previous commit in Git, you can use the command `git checkout <commit-hash> -- <file>`. This command replaces the content of the specified file with the version from the given commit. It effectively discards the changes made to the file since that commit.

**Q7: What is the purpose of the "git cherry-pick" command?**  
A7: The `git cherry-pick` command is used to apply a specific commit from one branch onto another branch. It allows you to select individual commits and apply them to a different branch, without merging the entire branch. Cherry-picking is useful when you want to selectively apply changes from one branch to another.

**Q8: How do you delete a branch in Git?**  
A8: To delete a branch in Git, you can use the command `git branch -d <branch-name>`. This deletes the specified branch locally. If the branch has not been merged, you can use `git branch -D <branch-name>` to force delete it. To delete a remote branch, you can use `git push origin --delete <branch-name>`.

**Q9: How do you view the commit history in Git?**  
A9: You can use the command `git log` to view the commit history in Git.

---

## Advanced Level

**Q1: What is Git rebase, and when would you use it?**  
A1: Git rebase is a command used to modify the commit history of a branch. It allows you to move, combine, or edit commits. You would use `git rebase` when you want to:  
- Incorporate changes from one branch onto another with a linear commit history.  
- Squash multiple commits into a single commit for a cleaner history.  
- Edit or reorder commits to improve readability or resolve conflicts.

**Q2: What is the difference between `git pull --rebase` and `git pull`?**  
A2:  
- `git pull --rebase` combines the `git fetch` and `git rebase` commands. It downloads the latest changes from the remote repository and then replays your local commits on top of the updated branch, resulting in a linear commit history.  
- `git pull` also combines `git fetch` and `git merge`. It downloads the latest changes and merges them into the current branch, creating a merge commit if necessary.

**Q3: How do you squash multiple commits into a single commit?**  
A3: To squash multiple commits into a single commit, you can use the interactive rebase feature:  
- Run `git rebase -i HEAD~n`, where `n` is the number of commits you want to squash.  
- In the interactive rebase editor, change "pick" to "squash" (or "s") for the commits you want to squash.  
- Save and exit the editor. Git will combine the selected commits into one and prompt you to provide a new commit message.

**Q4: What is the "git reflog" command used for?**  
A4: The `git reflog` command shows a log of all reference changes in your repository, including branch checkouts, commits, resets, and other operations. It is helpful for recovering lost commits or branches, as it provides a history of recent operations even if branch references have been deleted.

**Q5: How do you set up Git hooks?**  
A5: Git hooks are scripts that can be executed automatically before or after certain Git events, such as commits or pushes. To set up Git hooks:  
- Navigate to the `.git/hooks` directory in your repository.  
- Rename the hook you want to use (e.g., `pre-commit.sample`) to remove the `.sample` extension.  
- Customize the hook script by adding your desired commands or actions in the corresponding file.

**Q6: What is the purpose of the "git bisect" command?**  
A6: The `git bisect` command helps in finding the specific commit that introduced a bug or regression in your codebase. It performs a binary search through the commit history, automatically checking out different points in time and allowing you to mark commits as good or bad until the faulty commit is identified.

**Q7: How do you sign commits and tags in Git?**  
A7: Git supports commit and tag signing using GPG (GNU Privacy Guard) to verify the authenticity and integrity of commits and tags. To sign commits and tags:  
- Configure Git to use your GPG key: `git config --global user.signingkey <key-id>`.  
- Sign commits: `git commit -S -m "Commit message"`.  
- Sign tags: `git tag -s <tag-name>`.

**Q8: What are Git submodules?**  
A8: Git submodules allow you to include a separate Git repository as a subdirectory within your main repository. Submodules are useful when you want to include external dependencies or reuse code from other repositories while keeping them separate and manageable as individual repositories.

**Q9: How do you set up a Git server?**  
A9: There are various ways to set up a Git server, such as using GitLab, Bitbucket, or hosting your own Git server. For self-hosted Git servers, you can use software like Gitolite, Gitea, or GitLab Community Edition to manage and provide Git hosting capabilities.

**Q10: How can you recover a deleted commit in Git?**  
A10: If a commit has been deleted or lost, you can use the `git reflog` command to find the commit's reference and recover it. Once you identify the commit hash, you can create a new branch or use `git cherry-pick` to apply the changes from the recovered commit to the appropriate branch.

> These advanced-level Git interview questions cover topics that require a deeper understanding of Git's features and workflows. Keep practicing and exploring Git to enhance your proficiency with version control.

---

## Scenario-Based Questions

### Scenario 1
**John and Sarah are working on a project together using Git. John made some changes to a file, committed them, and pushed to the remote repository. Now Sarah wants to update her local repository with John's changes. How can Sarah do this?**

**Answer:**  
Sarah can update her local repository with John's changes by running the following command:  
```
git pull
```
This command fetches the changes from the remote repository and merges them into Sarah's current branch.

---

### Scenario 2
**Alice has made some changes to a file and committed them locally. However, she realized that she made a mistake and wants to undo the last commit. How can she do this?**

**Answer:**  
Alice can undo the last commit by using the following command:  
```
git reset HEAD~1
```
This command moves the branch pointer one commit behind, effectively removing the last commit. The changes made in that commit will still be present in Alice's working directory, allowing her to make the necessary corrections.

---

### Scenario 3
**Mark is working on a feature branch for a long-running project. However, he wants to switch to a different branch to work on a critical bug fix. What should Mark do to switch branches without losing his changes?**

**Answer:**  
To switch branches without losing his changes, Mark should first commit his changes on the current branch using the following commands:  
```
git add .
git commit -m "Save work in progress"
```
Then, he can switch to the desired branch using:  
```
git checkout <branch-name>
```
Once he completes the bug fix, he can switch back to the feature branch and continue his work.

---

### Scenario 4
**Emma wants to see the history of commits for a particular file in the repository. How can she do that?**

**Answer:**  
Emma can view the history of commits for a specific file by running:  
```
git log <file-name>
```
This command displays the commit history related to the specified file, showing the commit hash, author, date, and commit message for each commit.

---

### Scenario 5
**You've made some changes to a file in your local Git repository and realized that those changes were incorrect. What should you do to discard those changes and revert the file to its previous state?**

**Answer:**  
To discard the changes and revert the file to its previous state, use:  
```
git checkout -- <file>
```
This command will replace the current changes in the file with the last committed version, discarding the incorrect changes.

---

### Scenario 6
**You are working on a feature branch in Git, and you realize that some of the changes you made are incorrect and need to be removed. How can you selectively remove specific commits from your branch history?**

**Answer:**  
You can use the git rebase command with the interactive mode to remove specific commits from your branch history. Run:  
```
git rebase -i <commit>
```
where `<commit>` is the commit before the first commit you want to remove. In the interactive mode, you can delete or squash the commits you don't need. Save the file and exit the editor to apply the changes.

---

### Scenario 7
**You have been working on a local branch in Git and want to make it available to others by pushing it to a remote repository. However, you don't want to push all the commits in the branch. How can you push only selected commits to the remote repository?**

**Answer:**  
You can use the git cherry-pick command to pick specific commits and apply them to another branch. First, create a new branch from your current branch using:  
```
git branch <new-branch-name>
```
Then, use:  
```
git cherry-pick <commit>
```
for each commit you want to include in the new branch. Finally, push the new branch to the remote repository using:  
```
git push origin <new-branch-name>
```

---

### Scenario 8
**You have made some changes in your local branch and want to update it with the latest changes from the remote branch. However, you don't want to lose your local changes. What is the recommended approach to incorporate the remote changes while keeping your local changes intact?**

**Answer:**  
You can use the git stash command to temporarily save your local changes. Run:  
```
git stash
git pull
git stash apply
```
This sequence will stash your changes, update your branch, and reapply your local changes.

---

### Scenario 9
**You are collaborating with a team on a Git repository, and someone accidentally pushes sensitive information, such as API keys, to the remote repository. How can you remove those sensitive files from the repository history?**

**Answer:**  
To remove sensitive files from the repository history, you can use git filter-branch. Run:  
```
git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch <file-path>' --prune-empty --tag-name-filter cat -- --all
```
where `<file-path>` is the path to the sensitive file. Inform your team to rebase their work on the updated history.

---

### Scenario 10
**You have made a mistake in a commit message and want to modify it. How can you change the commit message of the most recent commit?**

**Answer:**  
Run:  
```
git commit --amend
```
Edit the message, save, and exit the editor. The commit message will be updated.

---

### Scenario 11
**You are working on a new feature branch, and you realize that some of the changes you made in a commit should have been in a separate commit. How would you split the commit?**

**Answer:**  
To split a commit into separate commits, use interactive rebase:  
1. Run `git rebase -i HEAD~n`, where `n` is the number of commits you want to modify, including the commit you want to split.  
2. In the rebase editor, change "pick" to "edit" for the commit you want to split.  
3. Save and exit. Git will stop at the commit.  
4. Use `git reset HEAD^` to unstage changes.  
5. Use `git add` and `git commit` to create new commits.  
6. Run `git rebase --continue` to resume.

---

### Scenario 12
**You accidentally committed a sensitive file that should not be included in the repository. How would you remove it from Git history?**

**Answer:**  
1. Backup the sensitive file.  
2. Run:  
   ```
   git filter-branch --tree-filter 'rm -f path/to/sensitive/file' -- --all
   ```
3. Wait for completion.  
4. Run `git push --force` to update the remote.  
5. Ask your team to update their local repositories.

---

### Scenario 13
**You need to collaborate with another developer on a new feature. How would you set up and manage a collaborative workflow using Git?**

**Answer:**  
1. Create a shared remote repository and give access to the other developer.  
2. Each developer clones the remote repository.  
3. Create a new branch for the feature.  
4. Develop, commit, and push regularly.  
5. Use pull/merge requests for review and merging.  
6. Resolve conflicts if any.  
7. Merge the feature branch into main or appropriate branch.  
8. Delete the feature branch after merging.  
9. Regularly fetch and pull changes from remote.

---

### Scenario 14
**You accidentally pushed a commit to the wrong branch. How would you revert that commit and apply it to the correct branch?**

**Answer:**  
1. Identify the commit hash.  
2. Checkout the correct branch.  
3. Run `git cherry-pick <commit-hash>`.  
4. Resolve any conflicts, commit changes.  
5. Optionally delete the wrong branch if not needed.

---

### Scenario 15
**You are working on a project with multiple contributors, and you accidentally merged a feature branch with a bug into the main branch. How would you revert the merge and fix the bug?**

**Answer:**  
1. Identify the merge commit hash.  
2. Checkout main branch.  
3. Run `git revert -m 1 <commit-hash>`.  
4. Resolve conflicts, commit, and push.

---

### Scenario 16
**You are working on a long-lived feature branch, and you want to keep it up to date with the changes in the main branch. How would you incorporate the latest changes from the main branch into your feature branch?**

**Answer:**  
1. Commit or stash any changes.  
2. Checkout main and pull latest.  
3. Checkout your feature branch.  
4. Run `git merge main`.  
5. Resolve conflicts and commit.  
6. Apply stashed changes if any.

---

## GIT Commands

1. `git init`: Initialize a new Git repository.  
   Example: `git init`

2. `git clone`: Clone a remote repository to your local machine.  
   Example: `git clone https://github.com/user/repo.git`

3. `git add`: Add files or changes to the staging area.  
   Example: `git add file.txt`

4. `git commit`: Commit the staged changes to the repository.  
   Example: `git commit -m "Commit message"`

5. `git status`: Show the current status of the repository.  
   Example: `git status`

6. `git log`: View the commit history.  
   Example: `git log`

7. `git diff`: Show the differences between files or commits.  
   Example: `git diff file.txt`

8. `git branch`: List, create, or delete branches.  
   Example: `git branch branchname`

9. `git checkout`: Switch to a different branch.  
   Example: `git checkout branchname`

10. `git merge`: Merge changes from one branch into another.  
    Example: `git merge branchname`

11. `git remote`: Manage remote repositories.  
    Example: `git remote add origin https://github.com/user/repo.git`

12. `git push`: Push local changes to a remote repository.  
    Example: `git push origin branchname`

13. `git pull`: Fetch and merge changes from a remote repository.  
    Example: `git pull origin branchname`

14. `git fetch`: Fetch changes from a remote repository.  
    Example: `git fetch origin`

15. `git stash`: Save changes that are not ready to be committed.  
    Example: `git stash`

16. `git stash pop`: Apply the most recent stash and remove it from the stash list.  
    Example: `git stash pop`

17. `git reset`: Reset the repository to a previous commit.  
    Example: `git reset commit_hash`

18. `git revert`: Create a new commit that undoes a previous commit.  
    Example: `git revert commit_hash`

19. `git tag`: Create and manage tags for marking specific points in history.  
    Example: `git tag v1.0.0`

20. `git remote -v`: View the URLs of the remote repositories.  
    Example: `git remote -v`

21. `git config`: Set or get repository options.  
    Example: `git config --global user.name "Your Name"`

22. `git show`: Show the details of a specific commit.  
    Example: `git show commit_hash`

23. `git cherry-pick`: Apply a specific commit from one branch to another.  
    Example: `git cherry-pick commit_hash`

24. `git rebase`: Reapply commits on top of another base commit.  
    Example: `git rebase branchname`

25. `git blame`: Show who changed which lines in a file.  
    Example: `git blame file.txt`

26. `git remote add`: Add a new remote repository.  
    Example: `git remote add origin https://github.com/user/repo.git`

27. `git remote remove`: Remove a remote repository.  
    Example: `git remote remove origin`

28. `git log --oneline`: Show the commit history in a condensed format.  
    Example: `git log --oneline`

29. `git log --graph`: Show the commit history in a graphical representation.  
    Example: `git log --graph`

30. `git log --author`: Show the commit history by a specific author.  
    Example: `git log --author "John Doe"`

31. `git blame`: Show who changed which lines in a file.  
    Example: `git blame file.txt`

32. `git branch -d`: Delete a branch.  
    Example: `git branch -d branchname`

33. `git branch -m`: Rename a branch.  
    Example: `git branch -m new_branchname`

34. `git show-branch`: Show branches and their commits.  
    Example: `git show-branch`

35. `git clean`: Remove untracked files from the working directory.  
    Example: `git clean -f`

36. `git remote prune`: Remove remote-tracking branches that no longer exist on the remote.  
    Example: `git remote prune origin`

37. `git log --grep`: Show the commit history that matches a specific pattern.  
    Example: `git log --grep "bug fix"`

38. `git log --since`: Show the commit history since a specific date.  
    Example: `git log --since "2022-01-01"`

39. `git log --until`: Show the commit history until a specific date.  
    Example: `git log --until "2022-12-31"`

40. `git bisect`: Find the commit that introduced a bug using binary search.  
    Example: `git bisect start`

41. `git reflog`: Show a log of all reference changes in the repository.  
    Example: `git reflog`

42. `git remote show`: Show information about a remote repository.  
    Example: `git remote show origin`

43. `git revert --no-commit`: Revert changes but do not create a new commit.  
    Example: `git revert --no-commit commit_hash`

44. `git reset --hard`: Discard all changes and reset the repository to a specific commit.  
    Example: `git reset --hard commit_hash`

45. `git config --global alias`: Set up an alias for a Git command.  
    Example: `git config --global alias.ci commit`

46. `git archive`: Create a tar or zip archive of a Git repository.  
    Example: `git archive --format=zip --output=archive.zip master`

47. `git submodule`: Manage Git submodules within a repository.  
    Example: `git submodule add https://github.com/user/repo.git`

48. `git clean -n`: Dry run of git clean to preview files that will be removed.  
    Example: `git clean -n`

49. `git log --follow`: Show the commit history of a renamed file.  
    Example: `git log --follow file.txt`

50. `git show-branch --all`: Show the commit history of all branches.  
    Example: `git show-branch --all`
# Question  
What is the difference between `git fork` and `git clone`, and when would you use each?

### 📝 Short Explanation  
This question is often asked to check if you understand collaboration workflows in Git — especially how open-source and team projects. Many developers confuse `fork` and `clone`, so it helps to clarify the purpose and use cases of both.

## ✅ Answer  
- **`git fork`** creates a **copy of a repository on your GitHub (or GitLab, etc.) account**, letting you propose changes without write access to the original repo.
- **`git clone`** creates a **local copy of any Git repository** (your own or someone else’s) on your machine for development.

### 📘 Detailed Explanation  
When you **fork** a repository on GitHub, you're telling the platform:  
> "I want a separate version of this repository in my own GitHub account."

This is especially useful for contributing to open-source and team projects where you don't have direct write access to the main repository. You fork the repo, make changes in your fork, and then create a **pull request** to propose those changes to the original project.

On the other hand, **`git clone`** is used to **download a repository (forked or original) to your local development machine**. This is what actually gives you the codebase to work with.

Here’s how you’d typically use both:
1. **Fork** the repo on GitHub (creates a copy under your GitHub username).
2. **Clone** your fork locally using:  
   ```bash
   git clone https://github.com/your-username/the-repo.git
   ```

> So: **Fork = GitHub-level action**, **Clone = Local machine-level action**.


## Question  
Explain a scenario where you used `git fork` instead of `git clone`. Why was forking necessary?

## ✅ Answer  
I used `git fork` when I contributed to a DevOps project in my org on GitHub. Since I didn’t have write access to the original repository, I forked it into my GitHub account, made changes, and then created a pull request from my fork to the upstream repo.

### 📘 Detailed Explanation  
In this scenario, the original repository belonged to an organization. I wanted to fix a bug in their Helm chart setup for Kubernetes deployments. Because I didn’t have contributor rights to push directly, I used the **Fork** button on GitHub to create a personal copy of the repository under my own GitHub username.

From there:
1. I cloned **my fork** to my local system:
   ```bash
   git clone https://github.com/my-username/devops-helm-project.git
   ```
2. Created a new branch, made the fix, committed the changes.
3. Pushed the branch to **my fork**:
   ```bash
   git push origin bugfix-helm-values
   ```
4. Finally, I submitted a **pull request** to the original repository.

Using `git clone` directly on the upstream repo wouldn't have helped because I couldn’t push changes or open a PR without a fork. So, **forking gave me independence and write access on my own terms**, while still contributing back to the main project.

---
# Git Fork in Action

Please watch the Udemy video for this question. No additional information is required.## Question  
What is the difference between `git fetch` and `git pull`, and when would you use each?

### 📝 Short Explanation  
This question checks if you understand how Git handles remote updates. Many developers use `git pull` out of habit but don’t realize that it’s a combination of two actions — which `git fetch` separates for more control.

## ✅ Answer  
- `git fetch` retrieves the latest changes from the remote repository **without merging** them into your current branch.
- `git pull` does the same as `fetch` but **also automatically merges** the changes into your current branch.

### 📘 Detailed Explanation  
When you run `git fetch`, you’re asking Git to contact the remote (like GitHub) and download any changes (new commits, branches, tags) — **but not apply them** to your working directory.

```bash
git fetch origin
```

This is useful when:
- You want to see what others have pushed
- You're preparing for a manual merge or rebase
- You want to avoid surprise changes to your working branch

With `git pull`, you're doing this **plus** merging the changes into your current branch in one step:

```bash
git pull origin main
```

That’s shorthand for:
```bash
git fetch origin
git merge origin/main
```

While `git pull` is faster, it can cause **unintended merges** if you’re not ready. That’s why many teams prefer doing `fetch` first, reviewing the changes, and then merging or rebasing manually.

> Summary:  
> Use `git fetch` when you want control.  
> Use `git pull` when you’re ready to sync changes directly.

---
# Git Fetch vs Git Pull Demo

Please watch the Udemy video for this question. No additional information is required.## Question  
Which command do you use more often — `git fetch` or `git pull`, and why?

### 📝 Short Explanation  
This question explores your Git workflow habits and whether you prefer a manual or automated approach to syncing changes from a remote repository.

## ✅ Answer  
I mostly use `git pull` because it streamlines my workflow by fetching and merging remote changes in one step. It’s convenient for staying up to date quickly, especially when collaborating in fast-moving branches.

### 📘 Detailed Explanation  
`git pull` is essentially a shortcut that performs both a `git fetch` and a `git merge`. Instead of running two separate commands, I prefer to use:

```bash
git pull origin main
```

This makes my routine faster and keeps my local branch synchronized with the remote without extra steps. It's particularly useful when:
- I’m working alone or in a small team where merge conflicts are rare
- I'm contributing to a feature branch that others aren’t modifying
- I want to frequently pull in the latest changes to test or deploy updates

Of course, I stay cautious by committing or stashing local changes before pulling to avoid conflicts or interrupted workflows. And if I suspect major upstream changes or want a closer look, I’ll temporarily switch to `git fetch`.

But for my day-to-day development, especially in active branches, `git pull` keeps things fast and simple — and that makes it my go-to.

---
## Question  
What is the difference between `git rebase` and `git merge`? When would you use each?

### 📝 Short Explanation  
This question evaluates your understanding of how Git manages branch history and collaboration. It’s a common topic in interviews because both commands integrate changes from one branch to another — but they do it in very different ways.

## ✅ Answer  
- `git merge` integrates changes by creating a new merge commit, preserving the history of both branches.
- `git rebase` moves your branch on top of another, rewriting commit history to create a linear sequence.

### 📘 Detailed Explanation  
Let’s say you have two branches:
- `main`
- `feature` (branched off earlier from `main`)

#### 👉 Using `git merge`:
```bash
git checkout feature
git merge main
```

This pulls changes from `main` into `feature` and creates a **merge commit**, like this:
```
A---B---C (main)
     \
      D---E---F (feature)
             \
              G (merge commit)
```

**Pros:**
- Preserves full history and context
- Safer in teams: no history rewriting
- Good for long-lived shared branches

**Cons:**
- History becomes messy with many merge commits
- Harder to trace linear commit flow

---

#### 👉 Using `git rebase`:
```bash
git checkout feature
git rebase main
```

This **re-applies your commits on top of the latest `main`**, like this:
```
A---B---C (main)
             \
              D'---E'---F' (rebased feature)
```

**Pros:**
- Clean, linear history
- Easier to `git log` and `git bisect`
- Preferred before merging short-lived branches into main

**Cons:**
- Rewrites commit history
- Risky if already pushed and others have based work on it
- Not ideal for shared/public branches

---

### 🧠 When to Use What

| Use `merge` when...            | Use `rebase` when...                  |
|-------------------------------|---------------------------------------|
| You're collaborating on shared branches | You're working alone or before a PR merge |
| You want to preserve commit context     | You want a clean, linear history          |
| History safety is a concern             | You're cleaning up before pushing         |

> Summary:  
> Use `merge` to combine, use `rebase` to simplify.

---

![Alt text](./images/git-merge-vs-rebase.png)

# Merge vs Rebase Practical

Please watch the Udemy video for this question. No additional information is required.# Merge vs Rebase Short Explanation

## ✅ Answer  
- `git merge` integrates changes by creating a new merge commit, preserving the history of both branches.
- `git rebase` moves your branch on top of another, rewriting commit history to create a linear sequence.## Question  
Explain the Git branching strategy you used in your company. Align it with the open-source branching strategy followed by Kubernetes.

### 📝 Short Explanation  
This question explores how you organize your Git workflow in a collaborative environment — especially in large codebases. Kubernetes, like many open-source projects, uses a clean and scalable branching strategy.

## ✅ Answer  
In my company, we followed a well-structured Git branching model similar to the Kubernetes project's workflow. Our strategy centered around four key branches:

- `main` – the default and stable development branch  
- `feature/*` – for all new features and enhancements  
- `release/*` – for preparing and testing production releases  
- `hotfix/*` – for urgent bug fixes or patches to production

This helped us maintain stability while enabling parallel development and quick recovery from issues.

### 📘 Detailed Explanation  

#### 🔹 `main` branch
- Equivalent to `master` or `main` in Kubernetes.
- Represents the **latest development state** — stable but evolving.
- All feature branches are branched off from here.
- Protected with branch rules and mandatory code reviews.

> Developers do not commit directly to `main`. All changes go through pull requests.

---

#### 🔹 `feature/*` branches
- Used for individual features or enhancements.
- Named like `feature/login-api` or `feature/cleanup-metrics`.
- Created from `main`.
- Developers work independently and raise PRs when done.

> We squash commits before merging to keep the history clean.

---

#### 🔹 `release/*` branches
- Cut from `main` when preparing for a release, e.g., `release/1.4`.
- Only allows **bug fixes, performance improvements, and docs**.
- CI pipelines run regression tests and validations here.
- Used for staging deployments and QA approvals.

> Kubernetes also creates release branches (e.g., `release-1.28`) to stabilize features after code freeze.

---

#### 🔹 `hotfix/*` branches
- Created from the latest release tag or `main`, based on urgency.
- Used when we need to fix critical bugs directly on production without waiting for the next release cycle.
- After fixing and testing, changes are merged back to both `main` and the relevant `release/*` branch.

> This ensures the fix is available in both the short term and future releases.

---

### ✅ Benefits of this Strategy:
- Supports **parallel development** and **safe releases**
- Keeps `main` clean and always deployable
- Makes it easy to trace features and bug fixes
- Aligns well with CI/CD automation and changelog generation

---

> By following this branching strategy, we maintained agility without compromising stability — which is critical in both enterprise and open-source scale environments like Kubernetes.

---
## Question  
Explain three challenges you faced while using Git in your work experience.

### 📝 Short Explanation  
This question is aimed at evaluating real-world Git usage and how well you’ve handled common pain points like collaboration, history management, and contribution workflows. It gives the interviewer insight into how deeply you've worked with Git in a team setting.

## ✅ Answer  
1. **Merge Conflicts During Pulls**  
   I used to rely heavily on `git pull` without checking what changes others had pushed. This led to merge conflicts, especially in fast-moving branches. Eventually, I switched to using `git fetch` followed by a manual `merge` or `rebase`, which gave me more control over how I integrated changes.

2. **Messy Commit History with Frequent Merges**  
   Early in my career, I used `git merge` frequently while working on long-lived feature branches. It cluttered the history with multiple merge commits, making it difficult to follow the actual changes. I learned to use `git rebase` (before pushing) to create a clean, linear history — especially before opening pull requests.

3. **Confusion Between Fork and Clone in Open-Source Work**  
   When I first started contributing to open-source, I cloned repositories directly and couldn’t push my changes. I realized I should’ve used `git fork` to create my own copy of the repo on GitHub. After forking, I was able to push changes to my own version and submit pull requests to the original repository.

### 📘 Detailed Explanation  
These challenges reflect how Git is powerful but not always beginner-friendly:
- **Merge conflicts** are a common problem in collaborative teams. Using `git fetch` and reviewing changes before merging helped me avoid surprise conflicts.
- **Messy commit history** can make debugging or code reviews painful. Switching to `rebase` in local branches before pushing made the history easier for teammates to follow.
- **Forking confusion** taught me about GitHub’s collaboration model. Understanding when to fork vs when to clone was key to contributing effectively to open-source.

---
## Question  
Explain a recent challenge you faced with Git and how you addressed it.

### 📝 Short Explanation  
This question is intended to assess your experience with Git at scale — especially around collaborative processes and governance. It’s an opportunity to demonstrate how you bring structure to complex codebases across teams.

## ✅ Answer  
A recent challenge I faced was implementing a consistent Git branching strategy across 100+ repositories used by multiple teams in my organization. Each team followed their own style — some had `main/dev`, others used `master/feature`, and a few used no long-lived branches at all. This inconsistency made CI/CD pipelines error-prone, releases chaotic, and collaboration difficult.

To solve this, we standardized on a lightweight **trunk-based branching strategy** with well-defined rules around `main`, `release/*`, and `feature/*` branches — and rolled it out in phases across teams.

### 📘 Detailed Explanation  
At a company-wide level, multiple teams were independently managing Git repos, and the lack of a unified branching approach caused several issues:
- CI pipelines were failing due to missing expected branches like `main` or `release`.
- Some teams rebased public branches, which broke collaborators' work.
- Merge conflicts were common in integration environments.
- Releases were often delayed due to confusion about which branch was production-ready.

Here’s how I addressed it:

#### ✅ Step 1: Analyze the current state
- Audited all repositories using automation (GitHub/GitLab APIs).
- Documented the branching models and naming conventions each team used.

#### ✅ Step 2: Design a unified strategy
- Proposed a **trunk-based development** model:
  - `main` → always production-ready
  - `release/x.y` → for stabilization and hotfixes
  - `feature/*` → short-lived, rebased before merge
- Outlined rules for using `merge`, `rebase`, and protection policies.

#### ✅ Step 3: Rollout with tooling & education
- Created templates (starter repos) with the correct branch structure.
- Set up default branch protections and PR requirements using GitHub Actions and branch policies.
- Ran onboarding sessions and created a lightweight Git handbook tailored to our strategy.

#### ✅ Step 4: Iterate with feedback
- Incorporated feedback from platform, dev, and QA teams.
- Adjusted the policy to allow for temporary exceptions during migration.

---

The result was:
- 95%+ repos aligned within 2 months.
- CI/CD pipeline reliability improved significantly.
- Teams were clearer on how and when to branch or merge.
- It became easier to onboard new developers and automate release workflows.

---
## Question  
How do you handle merge conflicts in Git?

### 📝 Short Explanation  
Merge conflicts are a common part of collaborative Git workflows. This question is meant to test how calmly and effectively you resolve conflicts and whether you understand why they occur.

## ✅ Answer  
When I encounter a merge conflict, I pause to understand which files are affected, examine the conflicting changes, and manually resolve them using a visual diff tool or editor. Once resolved, I mark the conflicts as resolved, stage the changes, and complete the merge or rebase.

### 📘 Detailed Explanation  
Merge conflicts usually happen when:
- Two branches modify the same lines in a file
- One branch deletes a file the other modifies
- A rebase applies commits that overlap with existing changes

Here’s how I handle them:

#### 🔍 Step 1: Identify the conflict
Git clearly indicates the files with conflicts during a `git merge` or `git rebase`:
```bash
Auto-merging app.py  
CONFLICT (content): Merge conflict in app.py  
```

#### 🛠️ Step 2: Open and resolve the conflict
Conflicted files contain markers like:
```diff
<<<<<<< HEAD
print("Hello from main")
=======
print("Hello from feature-branch")
>>>>>>> feature-branch
```

I manually edit the file to reflect the correct final code, based on the intended logic. Sometimes I use tools like:
- `git diff` to understand the changes
- Visual Studio Code or GitKraken for visual resolution

#### ✅ Step 3: Mark as resolved
Once edited:
```bash
git add app.py
```

Then complete the merge:
```bash
git commit         # if using merge
# or
git rebase --continue  # if using rebase
```

> Merge conflicts aren’t errors — they’re just Git asking you to make a decision. Handling them well is part of being a collaborative engineer.

---
## Question  
What are `ours` and `theirs` strategies in Git merges? How and when are they used?

### 📝 Short Explanation  
This question checks whether you understand how to control merge behavior during conflicts — especially in tricky cases like rollbacks, overrides, or integration branches.

## ✅ Answer  
- **`ours`** strategy favors **your current branch’s changes**, even if the other branch has different content.
- **`theirs`** isn't directly available as a merge strategy but can be used during conflict resolution in a rebase or a manual merge to **accept incoming changes over yours**.

### 📘 Detailed Explanation  

#### 🧩 `ours` Strategy (as a Git merge strategy)
When running a merge, you can tell Git:
> “Even though we’re merging, if there’s a conflict — pick my current branch’s version.”

Used like this:
```bash
git merge -s ours feature-branch
```

🧠 **Important:** This does *not* mean it merges and keeps both sets of changes. It **pretends to merge** but **keeps only your current branch's content**, marking the merge as done.

📌 **Use cases:**
- When rolling back a hotfix and keeping current stable state
- When merging a long-dead branch just to close it but keep your branch's state intact

---

#### 🧩 `theirs` Strategy (used manually during conflicts)
There is **no `-s theirs` strategy** at the command line merge level.

However, when resolving a conflict manually, you can choose the **incoming branch's changes** using:
```bash
git checkout --theirs conflicted_file.txt
git add conflicted_file.txt
```

This tells Git:
> “For this conflicted file, discard my local version and use the version from the branch I’m merging in.”

📌 **Use cases:**
- When the incoming changes are definitely correct
- During `git rebase` when resolving repetitive or well-understood conflicts

---

### 🧠 Summary Table

| Strategy  | Behavior                                      | Use When...                                             |
|-----------|-----------------------------------------------|----------------------------------------------------------|
| `ours`    | Keeps **current branch’s** content             | You want to keep your version, discard the incoming one |
| `theirs`  | Keeps **incoming branch’s** content            | You want to override with the other branch’s changes    |

---
## Question  
Have you ever used Git tags? If yes, why?

### 📝 Short Explanation  
This question checks if you're familiar with versioning and release practices in Git. Tags are an important part of marking stable points in history — especially in CI/CD pipelines and production deployments.

## ✅ Answer  
Yes, I’ve used Git tags primarily to mark release versions of our applications. It helps track which commit corresponds to a production deployment, and makes it easier to roll back or audit changes when needed.

### 📘 Detailed Explanation  
In one of my recent projects, we followed a simple release process where every stable build that passed all stages in our CI/CD pipeline was tagged with a version number — like `v1.0.3`.

I used annotated tags to add context:

```bash
git tag -a v1.0.3 -m "Release version 1.0.3 with critical bug fixes"
git push origin v1.0.3
```

These tags were then picked up by Jenkins and used as part of the deployment name — so we always knew what version was running in production.

#### 🔍 Why Git Tags Are Useful:
- 🎯 **Marking release points:** Helps indicate stable or milestone commits
- 🔄 **Rollback support:** Easily check out a tag to return to a known good state
- 🧪 **Versioned builds:** Many CI systems trigger builds based on tags
- 🔖 **Consistent releases:** Tags act like bookmarks for deployments or patch notes

> In summary: I use Git tags to improve visibility, traceability, and control in software releases — they’re lightweight, powerful, and essential in production workflows.

---
## Question  
How do you combine multiple commits into a single commit in Git?

### 📝 Short Explanation  
This question is meant to evaluate your understanding of Git history manipulation — especially around commit hygiene, squashing, and preparing a clean pull request.

## ✅ Answer  
I use **interactive rebase** to squash multiple commits into a single, meaningful commit before pushing my changes. This helps in keeping the Git history clean and easy to read.

### 📘 Detailed Explanation  
Let’s say I made 4 commits while working on a single feature:

```bash
git log --oneline
abc123 Fix typo  
def456 Add input validation  
ghi789 Update error message  
jkl012 Initial work on login form  
```

Before pushing or raising a PR, I might want to **combine them into a single commit** that says something like:  
`Add login form with validation and error handling`

#### ✅ Here’s how I do it:

```bash
git rebase -i HEAD~4
```

This opens an editor with the last 4 commits:
```text
pick jkl012 Initial work on login form
pick ghi789 Update error message
pick def456 Add input validation
pick abc123 Fix typo
```

I change all but the first `pick` to `squash` or `s`:
```text
pick jkl012 Initial work on login form
squash ghi789 Update error message
squash def456 Add input validation
squash abc123 Fix typo
```

Then I write a new commit message when prompted, save, and exit.

Finally:
```bash
git push origin branch-name --force
```

> Note: You only force-push if the commits were already pushed to remote. Otherwise, a normal push is fine.

---

### 🧠 Why This Is Useful  
- Keeps Git history clean and easier to understand
- Combines all related changes into one atomic commit
- Helpful for reviewers and future debugging
- Commonly used before merging a feature branch into `main`

> This is often referred to as **squashing commits**, and it's a best practice when preparing PRs or fixing review feedback across multiple small commits.

---
## Question  
Explain 10 Git commands that you use on a day-to-day basis. What are they used for?

### 📝 Short Explanation  
This question evaluates your hands-on comfort with Git. It's meant to uncover whether you just follow the basics or actually use Git effectively for version control and collaboration.

## ✅ Answer  
Here are 10 Git commands I use regularly and what I use them for:

---

### 1. `git clone`
```bash
git clone https://github.com/org/repo.git
```
📦 Used to create a local copy of a remote repository when starting a new task or joining a project.

---

### 2. `git status`
```bash
git status
```
🧭 Shows the current state of the working directory — what’s staged, unstaged, and untracked.

---

### 3. `git add`
```bash
git add file.py
git add .
```
📝 Stages changes before committing. I use this before `git commit` to mark files I want to include.

---

### 4. `git commit`
```bash
git commit -m "Fix login bug"
```
💾 Saves a snapshot of the staged changes with a message describing the purpose.

---

### 5. `git push`
```bash
git push origin feature-branch
```
🚀 Uploads local commits to the remote repository, usually after a commit or merge.

---

### 6. `git pull`
```bash
git pull origin main
```
🔄 Fetches changes from the remote and merges them into the current branch — helps keep in sync with team updates.

---

### 7. `git fetch`
```bash
git fetch origin
```
📥 Downloads changes from the remote without merging — I use this when I want to review changes before integrating.

---

### 8. `git branch`
```bash
git branch
git branch feature/login
```
🌿 Lists all branches or creates a new one. Branching is the foundation of my feature workflows.

---

### 9. `git checkout`
```bash
git checkout main
git checkout -b hotfix/typo
```
🧳 Switches between branches or creates and switches in one go. I use this constantly during development.

---

### 10. `git rebase`
```bash
git rebase main
```
📚 Re-applies commits from one branch on top of another. Useful for maintaining a clean commit history before merging.

---
## Question  
I want to ignore pushing changes to a specific file in Git. How can I do it?

### 📝 Short Explanation  
This question tests your understanding of how Git tracks files, how `.gitignore` works, and how to prevent accidental pushes of sensitive or local configuration files.

## ✅ Answer  
To ignore future changes to a tracked file, I use the `assume-unchanged` flag. This tells Git to stop checking the file for changes, even though it's still in the repo.

```bash
git update-index --assume-unchanged path/to/your/file
```

### 📘 Detailed Explanation  
There are two main scenarios when you don’t want a file to be pushed:

---

### ✅ 1. If the file is **already tracked**, and you want Git to **stop tracking changes**:

Use:
```bash
git update-index --assume-unchanged file.txt
```

This keeps the file in the repo, but Git will act like it hasn’t changed — useful for config files that differ by environment.

🔁 To undo this and start tracking again:
```bash
git update-index --no-assume-unchanged file.txt
```

📌 Common use cases:
- `.env` files with local credentials
- `settings.json` or editor-specific config
- Scripts that are tweaked temporarily

---

### 🚫 2. If the file should never be tracked:

Add it to `.gitignore` **before** committing it:
```
# .gitignore
.env
*.log
```

This works **only for untracked files**. If it’s already committed once, `.gitignore` won’t help unless you untrack it first:

```bash
git rm --cached file.txt
echo file.txt >> .gitignore
```

Then:
```bash
git commit -m "Stop tracking file.txt"
```

---

### ⚠️ Note:
`assume-unchanged` is a **local-only** flag. It won’t prevent others from seeing changes or pushing the file. It’s a lightweight trick, but not a security mechanism.

> Summary:  
> Use `.gitignore` for new/untracked files.  
> Use `assume-unchanged` for tracked files you don’t want to accidentally push.

---
## Question  
What is the purpose of the `.git` folder in a Git repository?

### 📝 Short Explanation  
This question checks your foundational understanding of how Git works internally. The `.git` directory is the backbone of any Git repository.

## ✅ Answer  
The `.git` folder contains all the metadata, configuration, and object database Git needs to manage version control. It is what transforms an ordinary directory into a Git repository.

### 📘 Detailed Explanation  

When you run:
```bash
git init
```
Git creates a hidden directory called `.git/` in the root of your project. This folder stores everything Git needs to track versions, branches, commits, and configurations.

Here’s what it typically contains:

#### 🗂️ Key Contents of `.git/`:

- **`HEAD`**  
  A reference to the current checked-out branch. It tells Git “where you are” in the repo.

- **`config`**  
  Local repository settings like remote URLs, user info, aliases, etc.

- **`objects/`**  
  The actual content of your codebase — all commits, trees, and blobs are stored here in a compressed format.

- **`refs/`**  
  Contains references to all branches and tags (like `refs/heads/main` or `refs/tags/v1.0.0`).

- **`logs/`**  
  Records of updates to refs (used for debugging and recovery, e.g., with `git reflog`).

- **`index`**  
  The staging area — where files go after `git add` and before `git commit`.

---

### 🔐 Why It’s Important:
- Without the `.git` folder, your project is no longer a Git repository.
- If you delete or corrupt it, Git can no longer track changes.
- If you copy the `.git` folder into another directory, you essentially clone the repo without using a remote.

---

### ⚠️ Common Pitfall:
Developers sometimes accidentally delete the `.git` folder when cleaning up, which **removes all Git history** — not just local changes.

> Summary:  
> The `.git` directory is the internal database and control center of your repository. It contains everything Git needs to version, compare, and manage your project effectively.

---
## Question  
Can you restore a deleted `.git` folder?

### 📝 Short Explanation  
This question evaluates your knowledge of Git internals and backup strategies. Accidentally deleting the `.git` directory wipes out version control history — unless you have a fallback.

## ✅ Answer  
No, you cannot restore a deleted `.git` folder **on your own** unless you have:
- A backup of the folder (manual or automated), or
- A remote copy of the repository (e.g., on GitHub or GitLab)

### 📘 Detailed Explanation  

The `.git/` folder is the **heart of the Git repo** — it contains:
- All your commits
- Branch info
- Tags
- Staging data
- Remote config

If you delete it:
```bash
rm -rf .git
```
Your project becomes a regular directory with no version history.

---

### ✅ Recovery Options:

#### Option 1: You have a remote (like GitHub)

If the repo was pushed earlier:
```bash
# Move existing code out
mkdir backup && mv * backup/

# Clone fresh repo
git clone https://github.com/your/repo.git

# Move your untracked files back in
mv backup/* repo/
```

Then you can `git add`, `commit`, and `push` any uncommitted changes.

---

#### Option 2: You have a backup of the `.git` folder

If you made a backup (e.g., `.git.bak`), you can restore it:

```bash
mv .git.bak .git
git status
```

You’re back in business with full history and branches intact.

---

#### Option 3: Try file recovery tools *(low chance)*

If the `.git` folder was recently deleted and not overwritten, tools like `extundelete` or `recuva` **might** recover parts of it — but success is rare and not reliable.

---

### 🧠 Best Practices to Prevent This:

- Push frequently to a remote.
- Enable automatic backups or snapshot tools.
- Avoid using `rm -rf` without double-checking.
- Use Git GUIs or IDEs to reduce chances of accidental deletion.

> Summary:  
> Once `.git` is gone and you have no remote or backup, your project loses its entire Git history. The safest way to recover is to clone from the remote and reapply any local, uncommitted changes manually.

---
## Question  
A teammate accidentally committed a Kubernetes Secret (base64 encoded) to Git. What should you do?

### 📝 Short Explanation  
This scenario tests how you respond to a security breach and how well you understand Git history rewriting, sensitive data handling, and Kubernetes secrets management.

## ✅ Answer  
Immediately remove the secret from the Git history using tools like `git filter-repo` or `BFG`, rotate the compromised secret, and enforce better secret management policies (e.g., use sealed secrets or external secret stores).

### 📘 Detailed Explanation  

When a Kubernetes Secret (even base64-encoded) is committed to Git, it becomes publicly visible to:
- Everyone with repo access
- Anyone who forked or cloned the repo before removal
- CI/CD systems that fetch the repo

### 🛠️ Step-by-Step Response:

---

#### ✅ Step 1: Rotate the compromised secret  
Whether it’s an API key, database password, or token — assume it’s compromised.

- Create a new secret value (e.g., generate a new DB password or token).
- Update the Kubernetes Secret:
  ```bash
  kubectl create secret generic my-secret --from-literal=password=newpassword --dry-run=client -o yaml | kubectl apply -f -
  ```
- Update any workloads consuming the old secret.

---

#### ✅ Step 2: Remove the secret from Git history  
Base64 encoding is **not encryption**. Anyone can decode it.

If it was recently committed:
```bash
git reset HEAD~1
git restore --staged secret.yaml
rm secret.yaml
git commit -m "Remove secret from repo"
```

But this only removes it from the latest commit. To fully remove it from **entire history**:

Use [`git filter-repo`](https://github.com/newren/git-filter-repo) (preferred over `filter-branch`):
```bash
git filter-repo --path secret.yaml --invert-paths
```

Or use **BFG Repo-Cleaner**:
```bash
bfg --delete-files secret.yaml
```

Then force-push:
```bash
git push --force
```

> Everyone with clones will need to re-clone or follow special instructions to realign their history.

---

#### ✅ Step 3: Prevent it from happening again  
- Add sensitive files to `.gitignore`
  ```
  secrets.yaml
  *.key
  ```
- Use tools like [git-secrets](https://github.com/awslabs/git-secrets) or [pre-commit](https://pre-commit.com/) to scan commits for secrets.
- Educate team members that **Kubernetes Secrets are not encrypted by default in Git**, even though they look scrambled (base64).

---

### 🚫 Why This Matters  
Hardcoded secrets in Git are one of the most common security missteps. Even private repos can be compromised. This situation reflects your ability to respond quickly, contain damage, and improve team practices.

> Summary:  
> Rotate → Remove → Recommit safely → Enforce policies.

---

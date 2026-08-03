# What is branch?

Basically is is an independent and isolated workspace from copy of another branch to build features or fix bugs or experiment without altering the main codebase from copied branch.

So it's a parallel development, collaboration, and code organization whiteout affecting the main, master or other branch. It acts abstraction for the edit/stage/commit process and each branch maintains its own commit history.

Every repository have main or master branch when you initialize a new Git repository. This is the default branch.

[Learn Git Branching](https://learngitbranching.js.org/) is the most visual and interactive way to learn Git on the web. You'll be challenged with exciting levels, given step-by-step demonstrations of powerful features, and maybe even have a bit of fun along the way.



# Branch VS Fork VS Clone
- A branch must exist inside a single repository.
- A fork basically is a new copy of the entire repository in source control account like GitHub. The developer have the full control over the newly copied codebase and can contribute to the Git repository that was forked. 
- A clone download a repository to your computer but the developer can sync their copy of the codebase.

# Creating new branch or switch
To create new Git branch **``git checkout -b <branch-name>``**.

To switch to a branch **``git switch -c <branch-name>``**

**Example**
```bash
# Ensure you have the latest changes from your default branch (e.g., main or master) before creating a new one.
git checkout main
git pull origin main

# Create and switch to the branch
git checkout -b feature-your-branch-name

# Publish the branch to the remote server
git push -u origin feature-your-branch-name
```

# Visualize branching and merging graphically in Git

Using the terminal with built-in commands, editor extensions, or dedicated visual applications you can graphically visualize branches and merges in Git.
**``git log --graph --all --oneline --decorate``**
- **``--graph``:** draws a tree graph with ASCII art of the branches.
- **``--all``:** shows all branches.
- **``--oneline``:** summarizes each commit on a single line.
- **``--decorate``:** displays the names of the branches and associated tags.

# Merge 
To merge a branch in Git, the standard process is to access the target branch (usually the primary or master branch) and pull the changes from the secondary branch.

**Example**
```bash
# Incorporate the changes from your secondary branch (e.g., feature-your-branch-name) into the current branch.
git merge feature-your-branch-name

# Update the remote repository with the result of the merge.
git push origin main
```

# GitHub (Pull Request)
A Pull Request (PR) is a GitHub tool used to propose changes to a project and ask someone to review them before they are integrated into the main code. Before performing the merge, the code is discussed and tested; only after it is approved is the merge executed.

1. Create a branch, make changes to the code, and push it to GitHub.
1. On GitHub, you click "New Pull Request" to compare your branch with the main branch (e.g., main).
1. The reviewer, teammates, managers or stakeholders review the changes, leave comments, suggest corrections, and test the code.
1. After resolving doubts and correcting any errors, the code is approved.
1. The Pull Request is closed, and the changes are merged into the main branch.

**so, why Pull Request?**
- Prevents code with errors from being sent directly to the production version.
- Allows multiple programmers to discuss the best solution to a problem.
- Creates a visual and documented record of why each change was made.

# Docs
- [Git Branching - Branches in a Nutshell](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)
- [Git Branching - Basic Branching and Merging](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)
- [Git Branching - Branch Management](https://git-scm.com/book/en/v2/Git-Branching-Branch-Management)
- [Git Branching - Branching Workflows](https://git-scm.com/book/en/v2/Git-Branching-Branching-Workflows)
- [Git Branching - Remote Branches](https://git-scm.com/book/en/v2/Git-Branching-Remote-Branches)


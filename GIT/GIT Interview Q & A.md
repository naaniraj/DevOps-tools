#### Q1. What is Git and how does it work in DevOps?
A: Git is a distributed version control system used to track code changes. In DevOps,
it enables collaboration among teams, supports CI/CD by integrating with tools like Jenkins,
and maintains complete version history. Developers can work offline and later sync changes using push/pull.


#### Q2. What is the difference between Git and GitHub?
A:Git is a tool to manage code versioning locally and remotely.

GitHub is a cloud-based platform to host Git repositories with additional collaboration features (issues, pull requests, actions).

#### Q3. What is a Git branch, and why is it used?
A: A branch is an independent line of development. It allows developers to work on features or
fixes in isolation before merging them into the main codebase.

#### Q4. How do you resolve a Git merge conflict?
A: When two branches modify the same line of code, Git can’t auto-merge.
You resolve conflicts by manually editing the conflicted file(s), marking the correct code, then committing the resolved version.

#### Q5. What is the difference between git merge and git rebase?
A:merge keeps the history of both branches.
rebase rewrites the history by placing your changes on top of another branch for a cleaner linear history.

#### Q6. Explain the working area, staging area, and repository.
A:Working directory: Where you make changes
Staging area: Where changes are prepared (git add)
Repository: Where changes are committed (git commit)

#### Q7. What does .gitignore do?
A: It tells Git which files/folders to ignore while tracking (e.g., node_modules, *.log, *.env).

#### Q8. What is a Pull Request in GitHub?
A: It is a request to merge one branch into another. Others can review, comment, and approve before merging.

#### Q9. How do you clone a remote repository?
A: Using the command:
git clone https://lnkd.in/

#### Q10. How do you revert a commit?
A:To undo last commit: git revert <commit-id>
To hard reset to a previous state: git reset --hard <commit-id>

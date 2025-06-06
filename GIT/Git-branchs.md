✅Git Branches
****************
* a branch represent a independent line of a development
* the git branch commands can lets you create,list,rename,and delete brancheas.
* the default branch name in git is "MASTER"

✅Common Git Branch Commands
************************************
1. Create & Switch Branches
   
       git branch [branch-name] – Create a new branch
       git checkout [branch-name] – Switch to an existing branch
       git checkout -b [branch-name] – Create & switch to a new branch

2. View Branches
   
       git branch – Show all local branches
       git branch -r – Show all remote branches
       git branch -a – Show both local & remote branches

3. Merge Branches
   
       git checkout main – Switch to the main branch
       git merge [branch-name] – Merge another branch into the main branch

4. Delete Branches
   
        git branch -d [branch-name] – Delete a branch (only if merged)
        git branch -D [branch-name] – Force delete a branch

5. Push & Pull Remote Branches
   
       git push origin [branch-name] – Push a branch to a remote repository
       git pull origin [branch-name] – Fetch & merge changes from a remote branch

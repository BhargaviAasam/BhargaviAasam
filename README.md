- 👋 Hi, I’m @BhargaviAasam
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
BhargaviAasam/BhargaviAasam is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
Getting & Creating Projects
Command	Description
git init	Initialize a local Git repository
git clone ssh://git@github.com/[username]/[repository-name].git	Create a local copy of a remote repository


Basic Snapshotting
Command	Description
git status	Check status
git add [file-name.txt]	Add a file to the staging area
git add -A	Add all new and changed files to the staging area
git commit -m "[commit message]"	Commit changes
git rm -r [file-name.txt]	Remove a file (or folder)


Branching & Merging
Command	Description
git branch	List branches (the asterisk denotes the current branch)
git branch -a	List all branches (local and remote)
git branch [branch name]	Create a new branch
git branch -d [branch name]	Delete a branch
git push origin --delete [branch name]	Delete a remote branch
git checkout -b [branch name]	Create a new branch and switch to it
git checkout -b [branch name] origin/[branch name]	Clone a remote branch and switch to it
git branch -m [old branch name] [new branch name]	Rename a local branch
git checkout [branch name]	Switch to a branch
git checkout -	Switch to the branch last checked out
git checkout -- [file-name.txt]	Discard changes to a file
git merge [branch name]	Merge a branch into the active branch
git merge [source branch] [target branch]	Merge a branch into a target branch
git stash	Stash changes in a dirty working directory
git stash clear	Remove all stashed entries


Sharing & Updating Projects
Command	Description
git push origin [branch name]	Push a branch to your remote repository
git push -u origin [branch name]	Push changes to remote repository (and remember the branch)
git push	Push changes to remote repository (remembered branch)
git push origin --delete [branch name]	Delete a remote branch
git pull	Update local repository to the newest commit
git pull origin [branch name]	Pull changes from remote repository
git remote add origin ssh://git@github.com/[username]/[repository-name].git	Add a remote repository
git remote set-url origin ssh://git@github.com/[username]/[repository-name].git	Set a repository's origin branch to SSH


Inspection & Comparison
Command	Description
git log	View changes
git log --summary	View changes (detailed)
git log --oneline	View changes (briefly)
git diff [source branch] [target branch]	Preview changes before merging


 -------squashing all commits into one---------
 1.git rebase -i HEAD~14--->squashing commits
 2.git push -f
 --------stashing---
 git reset --soft HEAD~1
 git status
 git stash
 git log -5


 git log -5---> to see commits
 git remote add bedrock https://github.wsgc.com/eCommerce-Bedrock/dp-baselogic.git --->adding remote branch
 git remote -v
 git fetch --all
 git pull
 git checkout HIM-783
 git reset --hard bedrock/release 
  git statsh list
  git stash pop-->adding staged coommiit to new branch
   git add *
   git commit -m "HIM-783-reserve flag added"
   git push
   git log -5
   git checkout bedrock/release-2.6.27.x
   git checkout -b HIM-783-Review
   git reset --hard bedrock/release-2.6.27.x
   git push -f
   git cherry-pick 3a283ae3b49d96bdbaa69e5dc8b8a01ffb3ca53d
   git push -f
   

------hard reset process-------------
   -------origin/develop against bedrock/release----------
  git remote add bedrock https://github.wsgc.com/eCommerce-Bedrock/dp-baselogic.git --->adding remote      branch
 git remote -v
 git fetch --all
 git pull
 git reset --hard bedrock/release 
 git push -f origin develop

-------------cherry-pick process-----------
git cherry-pick ${commit-hash}
Resolve all conflicts
git add .
git cherry-pick --continue
git push -f



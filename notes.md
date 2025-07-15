# GIT and GITHUB :-

## GIT :-

Version Control System (VCS) is a tool that helps track all the changes made in the code. Git is a VCS which is free to use, open source, popular, fast and scalable.  

1. Tracking :-  
   * It helps track the history of any project or tool built. It also helps to get back to previous commit of the program if required.
   * It also helps track who made what changes.
  
2. Collaborations :-  
   * It helps to collaborate where many can work on same project by allotting respective branches to each person to work independently and allow to integrate them to the main branch in the later stages by creating pull requests.
   * It helps a senior developer to resolve merge conflicts and decide which changes to be accepted and merged.

---

## GITHUB :-

* GitHub is a website that allows developers to store and manage their work using Git.  
* It also allows developers to even make changes directly or implement the changes made on the local system onto the website.  
* All the work is organised well in folder-like Repositories (repos, in short).  
* It also allows to copy and paste the work of another developer and make desired changes in it.  
* README.md is file that gives information of the project built, how to use, what's name of it, what's the use of it etc.
* **PROCESS** :-  

1. Pull required repo from GitHub to VS Code.
2. Make required changes.
3. Save the changes.
4. Add them onto stage.
5. Commit it.
6. Push it back to GitHub.

   Majorly could be shortened as a two step process - Add and Commit. But when changes are done directly on GitHub, single step is involved that is Commit.

---

### Working on GitHub :-

* Every commit has a commit message that tells what is being changed.
* Basic HTML or Markdown can be used to edit READMEs.
* Create your first repo say apnacollege-demo.

---

### Setting up Git :-

* VS Code
* Git Bash
* Command prompt where we check for Git version : git --version

---

### Configuring Git :-

Open Git Bash and follow the steps :

1. *git config --global user.name "GitHub's username"*
2. *git config --global user.email "GitHub account's email"*
3. *git config --list* (to check the above info which is stored in credential helper of Git)

Here, 'global' : all the changes are made on the git by same email id.  
'local' : changes in one or few repos on git by different email id.  
Tild (~) denotes the root directry of the local system.

---

### Basic commands :-

1. Clone : Cloning (copying) a repo from remote (GitHub) on the local system (Laptop).  
*git clone link* (here link should be HTTPS link of that repo on GitHub).  
**Cloning is preferrable to be done using HTTPS link only. SSH link can be used during pushing a particular repo back from local to remote after desired changes.**  

2. Status : Displays the state of code, whether it is untracked, modified, staged (added), committed.  
*git status* (up to date - all the code currently on loacl is as same as remote).  
**Three types of git status:**

   * Untracked : New files that git haven't tracked yet.
   * Modified : Files with changes that git haven't tracked yet.
   * Staged/Added : File is ready to be committed.

3. Add : Adds new and changed files onto staging area.  
*git add file.name* - to stage single file.  
*git add .* - to stage all changed and new files.

4. Commit : Records the change permanently.
*git commit -m "commit message"*

5. Push : Upload local repo content onto remote repo.
*git push origin main* - push repo into that particular repo's that particular branch from which we cloned it onto VSCode. Here we have cloned it from apna college repo from main branch. Here origin is nothing but the repo from which we cloned that is apna college from github.

All these above commands were generally for that repo that is first created on remote platform and then cloned into local system. But when we start a new project from local sytem first, then desire to push it to remote, we use init command to first initialise the git into that repo and then use the above commands with init's commands.
6. Init : used to create, manage and initialise the git into new repo created on local system first.  
The following are the steps to follow:

* *git init* - to initialise git into new repo.  
* *git remote add origin (link)* - to connect the repo on remote to this paricular local repo. For this you copy the HTTPS or SSH link of that repo and make it as origin for this local repo created on local system.  
* *git remote -v* - to verify remote.  
* *git branch* - to check branch.  
* *git branch -M main* - to rename branch. Now the branch name is changed from master to main.  
* *git push origin main*.  
* *git push -u origin main* - here -u means upstream. Use this for first push into that particular repo, from next pushes, just use *git push* to push.

## WORKFLOW TO BE FOLLOWED :-

Create repo on GitHub ---> Clone it to local ---> Make desired changes ---> Add it to the stage ---> Commit it ---> Push it back to remote.

---

## Git Branches :-

Since many developers will be working on different parts of same project, they make a copy of the main branch's work and start continuing working on it. Later when their work is completed, they can merge these into main branch by creating pull requests.

---

### Branch commands :-

* *git branch*  
* *git branch -M main* - to rename branch.  
* *git checkout (branch name)* - to navigate from current branch to the branch stated in the command.  
* *git checkout -b (new branch's name)* - to create new branch.  
* *git branch -d (branch name to be deleted)* - to delete the branch.  

**Make sure to not be in respective branch which is desired to be deleted. Suppose you want to delete a branch named feature 1, then you should navigate to any other branch other than feature 1 to delete it.**  

### Merging Code :-

-> Way 1 :-

* *git diff (branch name with which you want to merge)* - to see the difference in current branch and the branch desired to be merged.  
* *git merge (branch name with which you want to merge)*.

-> Way 2 :-

* Create Pull Request.  

**After creating pull requests and merged after solving all the merge conflicts, we use PULL command to get the changes of merging reflected in local system from remote.**

### --> Pull command :-  

used to fetch and download the content of a repo from remote to update the local repo to match the content.  
*git pull origin main* - to pull the main branch's content onto local after the merges of many branches. This command can be used for other branches too.

### Solving MERGE CONFLICTS :-  

If the same line of code is different either within the branches to be merged or with the main branch, we use any of the following ways to solve them.

* PULL REQUESTS  
* Use the merge command : *git merge (branch name)* - If accept the current change, means accepting the branch's change in which we currently are in, If accept the incoming change means accepting the changes made by incoming merger of a branch, If accept both means, it adds the incoming changed line of code below the current branch's line of code.

### Undoing changes :-

Case 1. Staged changes :- Changes added but not yet committed.  
*git reset (file name)* - if want reset in specific file.  
*git reset* - if want reset in all files.

Case 2. Committed changes :- For 1 commit.  
*git reset HEAD~1* - to just reset only one commit, that is to get back a commit before.

Case 3. Committed changes :- For too many commits.  
First use *git log* to see the history of commits with respective hashes.  

*git reset (commit hash)* - to just get back to that commit preserving those commits which we jumped before. Say if i jump from current commit to 5 commits before, now using this command, i am still having all those 5 commits in local system using which i can go back and forth. But if i want to even delete them from system, use,  
*git reset --hard (commit hash)*

### Fork :-

A fork is a new repo that shares code and visibility settings with original "upstream' repo. Fork is a rough copy. Basically it's used to create a copy of whole work or code from other's account into my account and make desired changes and create PRs to merge it to main branch from where we copied it. This is highly used during **OSS CONTRIBUTIONS**.

-- X -- X -- X -- X -- X -- X -- X -- X -- X -- X -- X -- X -- X -- X -- X -- X -- X -- X -- X --

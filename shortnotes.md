# Git and GitHub :-  

Git : Version control system that provides platform and tools to access and make changes in codes and projects.  
GitHub : It is a website where developers manage and store the codes and projects.

## Work flow :-  

1. **If repo created on GitHub first** :  

* Clone the repo to local : *git clone (link of that repo)*
* Make desired changes
* Add it to local : *git add .*
* Commit it to local : *git commit -m "commit message"*
* Push it to remote : *git push -u origin main* - if to push this repo to 'origin' named github account and 'main' named branch in that repo.

2. **If repo is created on local first** :

* Create a repo on GitHub in name as same as the folder/repo has on local and Copy the ssh link of that repo, make sure to not initialise this with README.md
* Initialise the local repo with git : *git init*
* Connect this repo with the repo on local : *git remote add origin (link copied)*
* Cross check the repo added : *git remote -v*
* Make desired changes, add and commit them.
* Push it to remote

3. **During contributions on the repos of organisations:** :

* Fork their repo onto your GitHub account
* Clone this whole repo onto your local
* Make changes
* Push it back to your github
* create pull requests on github

During the contribution, to keep your changes made cloned repo of original organisation who's name is 'upstream' (keep it different from 'origin') up to date, you have to frequently keep pulling the updates directly from the organisation's original repo. For that,  

* Add the organisation's original repo's remote link to keep pulling the updates frequently : *git remote add upstream (link of that original repo)*
* To pull updates : *git pull upstream main* - this adds or removes the changes made in original repo by other contributors who's change's pull requests are accepted by organisation
* Push the changes overally made by you and also the updates you had pulled to your account : *git push -u origin main*
* Create pull requests on the original repo to get a merger of your changes into theirs

# Git Notes
## Creating a git repository
- create a the project repository in gitlab/github e.g: **project-name**
- create the project folder with name **project-name**
- open terminal and run
```php
 cd project-name
```
- run the following commands
```php
git init
```
- run and check the folders adding to git repository
```php
 git status  
```
> Note: In Laravel project remove ****vendor**** from **.gitignore** file for adding vendor to the repository
```php
git add README.md
git commit -m "initial commit"
```
- copy the repository url from gitlab/github e.g : **https://github.com/username/project-name.git**
- then run 
```php
git remote add origin https://github.com/username/project-name.git 
```
- run 
```php
git push -u origin master
```
- then enter your username and password for github/gitlab
## Creating git branches
- For listing all available branches 
```php
git branch
```
- creating a new branch 
```php
git branch branch-name
```
- switching to a specific branch 
```php
git checkout branch-name
```
- pushing a local branch to github/gitlab 
```php
git push -u origin branch-name
```
- merging a branch into **master branch**
```php
git checkout master
```
- then,
```php
git merge branch-name
```
- Delete a branch locally     
```php
git branch -d branch-name
```
- Delete a branch remotely 
```php
git push -u origin --delete branch-name
```
### Adding description to git branches
- switch to the specified branch using 
```php
git checkout branch-name
```
- For a single line description:
```php
git config branch.branch-name.description "enter your description here"
```
- For viewing single line description 
```php
git config branch.branch-name.description
```
- For multiline description, for editing and viewing
```php
git branch --edit-description
```
## Pull a remote branches
- first run
```php
git pull
```
- then run run
```php
git branch
```
- which shows only the **master branch**
- if we run 
```php
git branch -a
```
- output like this
```php
* master
  remotes/origin/HEAD
  remotes/origin/master
  remotes/origin/branch-name-1
  remotes/origin/branch-name-2
```
-   If you just want to take a quick peek at an upstream branch, you can check it out directly:
```php
git checkout origin/branch-name-1
```
- But if you want to work on that branch, you'll need to create a local tracking branch which is done automatically by:
```php
git checkout branch-name-1
```
- and you will see
```php
Branch experimental set up to track remote branch experimental from origin.
Switched to a new branch 'branch-name-1'
```
- Now, if you look at your local branches, this is what you'll see:
```php
git branchgit branch
```
- you will see
```php
* branch-name-1
  master

```



# Git Notes
## Creating a git repository
- create a the project repository in gitlab/github e.g: **project-name**
- create the project folder with name **project-name**
- open terminal and run `cd project-name`
- run the following commands
- `git init`
- run `git status`  and check the folders adding to git repository
> Note: In Laravel project remove ****vendor**** from **.gitignore** file for adding vendor to the repository
- `git add README.md`
- `git commit -m "initial commit"`
- copy the repository url from gitlab/github e.g : **https://github.com/username/project-name.git**
- then run `git remote add origin https://github.com/username/project-name.git` 
- run `git push -u origin master`
- then enter your username and password for github/gitlab
## Creating git branches
- For listing all available branches `git branch`
- creating a new branch `git branch branch-name`
- switching to a specific branch `git checkout branch-name`
- pushing a local branch to github/gitlab `git push -u origin branch-name`
- merging a branch into **master branch**
    `git checkout master`
    `git merge branch-name`
- Delete a branch locally     `git branch -d branch-name`
- Delete a branch remotely `git push -u origin --delete branch-name`
### Adding description to git branches
- switch to the specified branch using `git checkout branch-name`
- For a single line description:
        `git config branch.branch-name.description "enter your description here"`
- For viewing single line description 
        `git config branch.branch-name.description`
- For multiline description, for editing and viewing
        `git branch --edit-description`




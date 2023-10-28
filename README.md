# GitHub CheatSheet
## Basic GH Commands
* Clone a GitHub repository

```
git clone https://github.com/username/repo_name.git
```

* Assume you have a project `gitty-project` you would like to add to github. Here are the steps

(i) Initialize a git repo

```
git init
```

(ii) Add all files to git staging area

```
git remote add origin https://github.com/username/gitty-project.git
```
(iii) 
```
git add .
```
(iv)
Confirm that it has been added to the git staging area

```
git status
```
(v)
Commit your changes witth a message `initial commit`

```
git commit -m "initial commit"
```
(vi)
Push your changes to the upstream origin `master` the `main` github repo `gitty-project`

```
git push -u origin master
```

* Pull the latest commit to the staging area github

```
git pull
```

* Pull the latest commit from GitHub main/master and replace changes on the HDD

```
git reset --hard origin/master
```

* Revert the last 5 commits

```
git reset --hard HEAD~5
```

`NOTE!!!`: If you have already pushed to a remote, you will get a fast-forward error because your local history diverges from the remote history.
`THEREFORE:`To fix this error and push your changes to the remote, use:

```
git push -f
```

`NOTE!!!` However, use git push --force with extreme caution because it can result in lost work if you are not careful.

## Create a GitHub Repository using Git CLI
create a repository interactively
```
gh repo create
```
create a `public repo` called my-project and clones the same version to local storage
```
gh repo create my-project --public --clone
```
create a `private repo` called my-project and clones the same version to local storage
```
gh repo create my-project --private --clone
```
create a `remote repository` from the `current directory`
```
gh repo create my-project --private --source=. --remote=upstream
```
`NOTE:` The commands above will `only` work in the `terminal` if you have installed `Git CLI` 

## Working with GitHub Branches

Creates a github branch

```
git branch <yourBranchName>
```

Creates a branch and switches to that branch immediately

```
git checkout -b <yourBranchName>
```

List github branches

```
git branch -a
```

Delete a branch

```
git branch --delete <branchName>
```

Rename a local branch

```
git branch -m <oldBranchName> <newBranchName>
```

Switch to a branch

```
git checkout <branchName>
```

## Working with GH Pull-Requests
* First you need to install Github CLI
* Install and set up in your Windows O.S
* Restart your terminal and write down the following command.

Use `gh pr` to create the pull request 
```
gh pr create --base master --head <yourBranchNameHere> --title <yourTitleHere> --body <yourBodyTextHere
```

Use `gh pr list` to list how many pull requests that are there in a repository
```
gh pr list
```

This command will list all of the open pull requests in the current repository.
You can also filter the results by state, author, assignee, and other criteria. 
For example, to list all of the closed pull requests in the current repository, 
you would use the following command:

```
gh pr list --state closed
```

You can also use the gh pr view command to open the pull request in a web browser.
To do this, simply add the --web flag to the command. For example:
```
gh pr view 123 --web
```


To merge a pull request in GitHub using the GitHub CLI, you can use the following command:
```
gh pr merge
```
## Working with GH LFS (Large File System)  
Initialise and `install` `git lfs`
```
git lfs install 
```

Track specific file types `(e.g., *.png, *.jpg, *.mp4)`
```
git lfs track "*.png" "*.jpg" "*.mp4"
```

```
git remote add origin https://github.com/yourUsername/nameOftheProject.git
```
```
git lfs push --all origin main

```

```
git add .
```
```
git commit -m "Add Git LFS tracking info"
```
```
git remote add origin https://github.com/yourUsername/nameOftheProject.git
```



Use `amend` to change the commit message

```
git commit --amend
```

Remove a file from the Git Staging area

```
git rm --cached "fileName"
```

Adds any file with a `.html` extension

```
git add *.html
```

Configure git staging and pushing to your GitHub account

```
git config --global user.name "your_github_username"
git config --global user.email "your_email"
```

Creates a file named `.gitignore`. 
NOTE: This command is a very special command and it is used to create a file and be able to exempt
it not to be able to be pushed to the github central repository. Like /node-modules. 
```
touch .gitignore
```

Clone a project in an organization in GitHub

```
git clone https://username@github.com/org_name/repo_name.git
```

Switching Remote URL's from `SSH` to `HTTPS`

```
git remote set-url origin https://github.com/username/repo.git
```

verify that remote URL has changed

```
git remote -v
```

Switching Remote URL's from `HTTPS` to `SSH`

```
git remote set-url origin git@github.com:username/repo.git
```

Clear Git Remote origin

```
git remote remove origin
```

Instead of removing then reading again: You can instead use this command.

```
git remote set-url origin https://github.com/username/repo.git
```

Check if the file in your folder is up to date with the Local Repository

```
git remote update
```

Tells you whether the branch you are tracking is ahead, behind or has diverged

```
git status -uno
```

If you want to erase your `whole history` and `start over` again.

```
rm -rf .git
```

If you want to remove `both files` and `history`

```
rm -rf *
```

git fetch downloads the latest from remote without trying to merge or rebase anything.
Then the git reset resets the master branch to what you just fetched. The --hard option
Changes all the files in your working tree to match the files in origin/master

```
git fetch -all
git reset --hard origin/master
```

Add the first remote repo

```
git remote add -f [first_repo] [link_to_first_repo]
```

```
git merge --allow-unrelated-histories [first_repo]/master
```

Create a sub directory and move all first_repo files to it.

```
mkdir [first_repo]
mv * [first_repo]
git add .
git commit -m "Move first_repo files to first_repo directory"
```

Add the second remote repository

```
git remote add -f [second_repo] [link_to_second_repo]
```

Fix any merge conflicts and complete the merge as follows

```
git merge --continue
```

`SOLVED!:` Please `MOVE` or `REMOVE` them before merge error `SOLVED`

```
git clean -dxf
git pull origin master
```

`Remove` the `.git` hidden folder from the git repo

```
rm -rf .git
```

Disable GitHub `popups`

```
git config --global credential.modalPrompt false
```

Add GitHub `large-file-system`

```
git lfs install
```

`STEPS`

1. Clone the GitHub repo `git clone https://github.com/NickBwalley/repo.git`
2. Create a branch and switch to it `git checkout -b newBranch`
3. `git add .`
4. `git commit -m "initial commit"`
5. `git push origin newBranch`
6. `git remote add upstream https://github.com/NickBwalley/repo.git`
7. `git rebase upstream/master` # add changes to your local existing work.

## CLI Useful Features

creating a file from the terminal `windows-CLI`

```
touch "filename.html"
```

creating a file from the terminal `linux-CLI`

```
sudo nano "filename.html"
```

Install a package_name.deb command

```
sudo dpkg -i package_name.deb
```

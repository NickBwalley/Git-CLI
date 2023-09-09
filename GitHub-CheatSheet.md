# GitHub CheatSheet

## Basic Github Commands

1. To perform a github clone

```
git clone https://github.com/username/repo_name.git
```

2. Assume you have a project `gitty-project` you would like to add to github. Here are the steps

```
git init #initializes a local git repository
git add <filename> #adds the file to index
git add . #adds all files in the gitty-project
git status
git commit -m "initial commit"
git push -u origin master #pushes to the upstream master file
```

3. Creating a branch and commit to that branch

creates a github branch

```
git branch <branchname>
```

creates a branch and switches to that branch immediately

```
git checkout -b <branchname>
```

List github branches

```
git branch -a
```

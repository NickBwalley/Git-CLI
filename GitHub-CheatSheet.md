# GitHub CheatSheet

### Basic GitHub Commands

To perform a github clone

```
git clone https://github.com/username/repo_name.git
```

1. Assume you have a project `gitty-project` you would like to add to github. Here are the steps

Initialize a git repo

```
git init
```

Add all files to the git staging area

```
git add .
```

Confirm that it has been added to the git staging area

```
git status
```

Commit your changes witth a message `initial commit`

```
git commit -m "initial commit"
```

Push your changes to `main` github repo `gitty-project`

```
git push -u origin master
```

### Working with GitHub Branches

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

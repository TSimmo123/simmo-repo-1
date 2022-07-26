# Git

## What is Git?

Git is a distributed version-control system for tracking changes in source code during software development.

It is designed for cooridnating work betwween programmers, but it can be used to track changes in any set of files.

## What is GitHub?

GitHub is a provider of Internet hosting for software development and version control using Git. It provides access control and several collaboration features such as bug tracking, featture requests, task management, continuous integration and wikis for every project.

## The Basic Git Commands

| Command        | Description                                        |
|----------------|----------------------------------------------------|
| `git clone`    | Clone/Download a repository into a local directory |
| `git branch`   | List, create, or delete branches                   |
| `git add`      | Add file contents to the index                     |
| `git commit`   | Record changes to the repository                   |
| `git status`   | Show the working tree status                       |
| `git log`      | Show commit logs                                   |
| `git checkout` | Switch branches or restore working tree files      |
| `git pull`     | Fetch changes from a remote repository             |
| `git push`     | Push recorded changes to a remote repository       |

## Git Commands In Use

Create a new branch with -b

```bash
> git checkout -b <branchName>
```

Delete the branch with -d

```bash
> git branch -d <branchName>
```

We use the . to add all files to the repo.

```bash
> git add .
```

We use -m to add a commit message.

```bash
> git commit -m "Commit Message"
```
# EthBuilders Curriculum Support

## Table of Contents

<!-- TOC -->

- [EthBuilders Curriculum Support](#ethbuilders-curriculum-support)
  - [Table of Contents](#table-of-contents)
  - [Project Contact Info](#project-contact-info)
    - [Anthony A (Organizer | Developer)](#anthony-a-organizer--developer)
    - [Edward Amor (Developer)](#edward-amor-developer)
  - [Common Commands](#common-commands)
    - [Bash Terminal](#bash-terminal)
    - [Git](#git)
    - [Yarn | NPM](#yarn--npm)
  - [Set Up Instructions](#set-up-instructions)
    - [macOS and Linux Setup](#macos-and-linux-setup)
    - [Windows Setup](#windows-setup)
  - [Accesssing Command Line](#accesssing-command-line)
    - [Via macOS](#via-macos)
    - [Via Windows](#via-windows)
  - [General Resources and Links](#general-resources-and-links)
    - [Git / Github](#git--github)

<!-- /TOC -->

## Project Contact Info

[Join our Slack](http://bit.ly/NYC-Blockchain-Devs-Join-Slack)

### Anthony A (Organizer | Developer)

- Github: [@tesla809](https://github.com/tesla809)
- Slack: `@Anthony_Albertorio_NEVER_ASKS_FOR_COIN `

### Edward Amor (Developer)

- Github: [@skellet0r](https://github.com/skellet0r)
- Slack: `@Edward Amor`

## Common Commands

### Bash Terminal

**Information**
Hint: The more you use these commands, the easier they will become.

- print working directory - show your current absolute directory path \
  `pwd`
- list documents in directory  \
  `ls`
- list ALL including hidden ones (like .gitignore or .env)  \
  `ls -a`
- create a new file  \
  `touch <FILENAME>`
- remove file. Note: file is immediately deleted and does not go to trash bin  \
  `rm <FILENAME>`
- create a new directory  \
  `mkdir <NAME>`
- go directly to computer's root  \
  `cd`
- stay in same directory \
  `cd ./`
- go up one directory \
  `cd ../`
- go up two directories. Note continue to add `../` to go up 1 directory \
  `cd ../../`
- move file to new directory \
  `mv <FILENAME> <NEW DIRECTORY>`
- rename file \
  `mv <OLD FILENAME> <NEW FILENAME>`

**Bonus**
- remove an empty directory  \
- `rmdir <NAME>`
- remove non-empty directory  \
  **DO IT VIA GUI to avoid costly mistakes**
- display file in terminal \
  `cat <FILENAME>`
- see the command's manual \
  `man <COMMAND>`
- exit program - like man or cat \
  `q`

### Git

**Information**

- Show the working tree status
  `git status`
- show the current HEAD and its ancestry
  `git log`
- show the current HEAD and its ancestry with formatting
  `git log --pretty=format:"%h %s" --graph`
- show an ordered list of the commits that HEAD has pointed to (a local undo history for your repo - [reference](https://stackoverflow.com/questions/17857723/whats-the-difference-between-git-reflog-and-log))
  `git reflog`
- show all branches
  `git branch -a`
- list remote repositories
  `git remote -v`
- show line-by-line changes in your branch compared to master
  `git diff`

**Make Changes**

- Create new branch to make changes
  `git checkout -b <branch>`
- Checkout branch to make changes
  `git checkout <branch>`
- Change file name
  `git mv <old-file> <new-file>`
- Delete file
  `git rm <file>`

**Commit Changes**

- Make changes to the file
  `atom <filename>` _(or text editor of your choice)_
- Add a single file with changes
  `git add <filename>`
- Add all files with changes
  `git add -A`
- Commit the change with a message
  `git commit -m "Commit Message"`
  See [CONTRIBUTING.MD](../CONTRIBUTING.MD) for style guide on how to format commits.
- Add all files and commit the change in one command
  `git commit -am "Commit Message"`
- Modify last commit message
  `git commit --amend`
- Push change to repository (on Github)
  `git push origin`

**Update the Repo**

- Setting an upstream repository
  `git remote add upstream <clone-link>`
- Check out the master branch
  `git checkout master`
- Fetch branch from the upstream repository
  `git fetch upstream <branch>`
- Rebase changes from the upstream repository
  `git rebase upstream/<branch>`
- Push changes to the origin repository
  `git push origin`

**Delete Branch**

- Delete the branch from origin
  `git push origin -d <branch>`
- Delete the branch from local
  `git branch -d <branch>`

### Yarn | NPM

[Full list of yarn commands](https://classic.yarnpkg.com/en/docs/cli/)
[Full list of npm commands](https://docs.npmjs.com/cli/v6/commands)

`yarn install` \
`npm i`

- Install all node modules
- [Yarn - more info](https://classic.yarnpkg.com/en/docs/cli/install)
- [npm - more info](https://docs.npmjs.com/cli/v6/commands/npm-install)

`yarn add <package-name>` \
`npm install <package-name>`

- Installs a package and any packages that it depends on
- [Yarn - more info](https://classic.yarnpkg.com/en/docs/cli/add)
- [npm - more info](https://docs.npmjs.com/cli/v6/commands/npm-install)

`yarn remove <package-name>` \
`npm uninstall <package-name>`

- Removes an unused package from your current package.json
- [Yarn - more info](https://classic.yarnpkg.com/en/docs/cli/remove)
- [npm - more info](https://docs.npmjs.com/cli/v6/commands/npm-uninstall)

`yarn init` \
`npm init`

- Initializes the development of a package.
- [Yarn - more info](https://classic.yarnpkg.com/en/docs/cli/init)
- [npm - more info](https://docs.npmjs.com/cli/v6/commands/npm-init)

`yarn upgrade <package-name>@<verision>` \
`npm update <package-name>@<verision>`

- Upgrades packages to their latest version based on the specified range
- [Yarn - more info](https://classic.yarnpkg.com/en/docs/cli/upgrade)
- [npm - more info](https://docs.npmjs.com/cli/v6/commands/npm-update)

## Set Up Instructions

### macOS and Linux Setup

The Bash based terminal already comes pre-installed with UNIX based systems like macOS and Linux, so there is nothing to set up.

### Windows Setup

TBD

## Accesssing Command Line

### Via macOS

1. Hold down Spacebar + Command for Spotlight search
2. Type `Terminal`
3. Enter
4. Voila!

Place the terminal link where you find best to access.

### Via Windows

TBD

## General Resources and Links

### Git / Github

**Git Resources**

- Git Offical Docs: [Git Command Reference](https://git-scm.com/doc)
- Git Tower: [Learn Version Control with Git](https://www.git-tower.com/learn/git/ebook/en/command-line/introduction)
- Git Tower: [What is a rebase in Git?](https://www.git-tower.com/learn/git/glossary/rebase)
- Git Tower: [`rebase` as an alternative to `merge`](https://www.git-tower.com/learn/git/ebook/en/desktop-gui/advanced-topics/rebase#start)
- Atlassian: [Overview of `rebase`](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase)
- Github Help: [How to use `rebase`](https://help.github.com/en/github/using-git/using-git-rebase-on-the-command-line)
- [Learning Git Branching](https://learngitbranching.js.org/?locale=en_US)
- [A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/)
- [Oh Shit, Git!?!](https://ohshitgit.com/) with real problems and solutions

> ⚠️ 👀 **WARNING:**
> You should use rebase only for squashing YOUR local commits prior to a pull request. DO NOT ever rebase commits that have already been published to master. This will rewrite our public project's history. This applies to maintainers of the project.

**Github Workflow Resources**

- Github Guides: [Understanding the GitHub flow](https://guides.github.com/introduction/flow/)
- [GitHub Standard Fork & Pull Request Workflow (Chaser324)](https://gist.github.com/Chaser324/ce0505fbed06b947d962)
- Digital Ocean: [How To Create a Pull Request on GitHub](https://www.digitalocean.com/community/tutorials/how-to-create-a-pull-request-on-github)
- Mozilla Servo: [Beginner's guide to rebasing and squashing](https://github.com/servo/servo/wiki/Beginner's-guide-to-rebasing-and-squashing)
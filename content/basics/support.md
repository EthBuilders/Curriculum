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
      - [Show Directory Information](#show-directory-information)
      - [Navigate Directories](#navigate-directories)
      - [Manipulate Files](#manipulate-files)
      - [Display Files](#display-files)
    - [Git](#git)
      - [Git Information](#git-information)
      - [Make Changes](#make-changes)
      - [Commit Changes](#commit-changes)
      - [Update the Repo](#update-the-repo)
      - [Delete Branch](#delete-branch)
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

#### Show Directory Information

- `pwd`  - print working directory - show your current absolute directory path

- `ls`  - list documents in directory

- `ls -a`  - list ALL including hidden ones (like .gitignore or .env)

#### Navigate Directories

- `cd` - go directly to computer's root

- `cd ./` - stay in same directory

- `cd ../` - go up one directory

- `cd ../../` - go up two directories. Note continue to add `../` to go up 1 directory

#### Manipulate Files

- `touch <FILENAME>` - create a new file

- `rm <FILENAME>` - remove file. Note: file is immediately deleted and does not go to trash bin

- `mkdir <NAME>` - create a new directory

- `mv <FILENAME> <NEW DIRECTORY>` - move file to new directory

- `mv <OLD FILENAME> <NEW FILENAME>` - rename file

- `rmdir <NAME>` - remove an empty directory

- **DO IT VIA GUI to avoid costly mistakes** - remove non-empty directory

#### Display Files

- `cat <FILENAME>` - display file in terminal
- `man <COMMAND>` - see the command's manual
- `q` - exit program - like man or cat

### Git

#### Git Information

- `git status` - Show the working tree status

- `git log`- show the current HEAD and its ancestry

- `git log --pretty=format:"%h %s" --graph` - show the current HEAD and its ancestry with formatting

- `git reflog`- show an ordered list of the commits that HEAD has pointed to (a local undo history for your repo - [reference](https://stackoverflow.com/questions/17857723/whats-the-difference-between-git-reflog-and-log))

- `git branch -a` - show all branches

- `git remote -v` - list remote repositories

- `git diff`- show line-by-line changes in your branch compared to master

#### Make Changes

- `git checkout -b <branch>`- Create new branch to make changes

- `git checkout <branch>`- Checkout branch to make changes

- `git mv <old-file> <new-file>`- Change file name

- `git rm <file>`- Delete file

#### Commit Changes

- `atom <filename>` _(or text editor of your choice)_ - Make changes to the file

- `git add <filename>` - Add a single file with changes

- `git add -A` - Add all files with changes

- `git commit -m "Commit Message"` - Commit the change with a message

- `git commit -am "Commit Message"` - Add all files and commit the change in one command

- `git commit --amend` - Modify last commit message

- `git push origin` - Push change to repository (on Github)

#### Update the Repo

- `git remote add upstream <clone-link>` - Setting an upstream repository

- `git checkout master` - Check out the master branch

- `git fetch upstream <branch>` - Fetch branch from the upstream repository

- `git rebase upstream/<branch>` - Rebase changes from the upstream repository

- `git push origin` - Push changes to the origin repository

#### Delete Branch

- `git push origin -d <branch>` - Delete the branch from origin

- `git branch -d <branch>` - Delete the branch from local

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
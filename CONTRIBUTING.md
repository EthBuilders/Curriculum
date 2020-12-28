# Contributing to EthBuilders

## Table of Contents

<!-- TOC -->

- [Contributing to EthBuilders](#contributing-to-ethbuilders)
  - [Table of Contents](#table-of-contents)
  - [About the Project](#about-the-project)
    - [Project Values](#project-values)
    - [Townhall Meetings](#townhall-meetings)
    - [Project Leads and Contact Info](#project-leads-and-contact-info)
  - [How to Contribute](#how-to-contribute)
    - [Reporting Bugs](#reporting-bugs)
    - [Suggesting Features / Enhancements](#suggesting-features--enhancements)
    - [Picking up an Issue](#picking-up-an-issue)
    - [Contributing Code](#contributing-code)
    - [Staying Up to Date](#staying-up-to-date)
  - [Style Guides](#style-guides)
    - [Naming Git Branches](#naming-git-branches)
    - [Creating Git Commit Messages](#creating-git-commit-messages)
    - [Front End Style Guide](#front-end-style-guide)
  - [Getting Support](#getting-support)

<!-- /TOC -->

## About the Project

❤️ By the community, for the community. ❤️

We are building an open-source curriculum to help the community learn and build on Ethereum and related technologies.

Check out our [EthBuilders](https://www.meetup.com/ethbuilders/) meetup.

### Project Values

Our mission is to develop social good through technology. We value initiative, collaboration, experimentation, and integrity.

We are a welcoming, warm, and collaborative group of people from all over the world! Here you can experiment and take chances.

To FAIL is to make your **First Attempt In Learning**, and we are here to help. We encourage developers to learn new concepts and best practices while collaborating on a project that is scaling to help anyone learn and build on Ethereum.

### Townhall Meetings

We hold weekly townhall meetings on Mondays, from 6:30pm EST to 8:30pm EST.

The typical agenda is:

1. The Team Lead will give an update
2. Discuss project roadmap
3. Discuss project deadlines
4. Discuss action items for current goals
5. Time for community feedback and questions
6. Ethereum and DeFi weekly Update
7. Community presentation on a topic
8. Q&A Session

If you have any questions or need any additional information, please discuss it with the team [on our slack.](http://bit.ly/NYC-Blockchain-Devs-Join-Slack)

### Project Leads and Contact Info

More information can be found in the [support.md file](./support.md#project-leads-and-contact-info).

## How to Contribute

### Reporting Bugs

This section guides you through submitting a bug report for a EthBuilders Curriculum repository. Bugs are tracked as [Github Issues](https://guides.github.com/features/issues/) and when creating a new issue you will choose from a template that gives you guidelines on what information to provide.

Following these guidelines helps maintainers and the community understand your report, reproduce the behavior, and find related reports (if applicable).

**Before creating a bug report**, please check the list below as you might find out that you don't need to create one.

- **Check the README** for a list of common questions, abstracts, concerns, etc.
- **Search the ISSUES** to see if the problem has already been reported. If it has **and the issue is still open**, add a comment to the existing issue instead of opening a new one.

> **Note:** If you find a **Closed** issue that seems like it is the same thing that you are experiencing, **open a new issue** and include a link to the closed issue in the body of your new one.

**When you are creating a bug report**, please include as many details as possible and fill out the required issue template. The information it asks for helps us resolve issues faster. Use the outline in the issue template to explain the problem and include additional details for maintainers.

### Suggesting Features / Enhancements

This section guides you through submitting a feature request for the EthBuilders Curriculum, including completely new features, documents, lessons or minor improvements to existing functionality. Feature requests are tracked as [Github Issues](https://guides.github.com/features/issues/) and when creating a new issue you will choose from a template that gives you guidelines on what information to provide.

Following these guidelines helps maintainers and the community understand your suggestion and find related suggestions.

**Before creating a feature request**, please **search the ISSUES** to see if the feature has already been requested. If it has **and the issue is still open**, add a comment to the existing issue instead of opening a new one.

> **Note:** If you find a **Closed** issue that seems like it is the same thing that you are experiencing, **open a new issue** and include a link to the closed issue in the body of your new one.

**When you are creating a feature request**, please include as many details as possible and fill out the required issue template. The information it asks for helps us resolve issues faster. Use the outline in the issue template to explain the feature and include additional details for maintainers.

### Picking up an Issue

If you wish to contribute to an issue, look through the Issues tab of the related repository and find one labeled **Help Wanted.** These are issues that we are actively looking for participation in.

To pick up an issue, add a comment saying "I'm on it", and the Help Wanted label will be removed and you will be assigned to the issue.

### Contributing Code

This section describes how our workflow operates so that you can contribute code in a way that scales with a growing team and product.

This represents a standard way that many open source projects operate, and more information including terminology and helpful commands can be found in the [support.md](./support.md) file.

> ⚠️ **Please do not clone directly from our main repository.** This will point your local repo's [origin](https://www.git-tower.com/learn/git/glossary/origin) to our main repo, and you will not have write access. Doing so will eventually cause an error when attempting to push your changes.

**When you are first setting up the repository**, follow the steps below to ensure that your changes can be merged into the project.

1. [Fork the repository](https://help.github.com/en/github/getting-started-with-github/fork-a-repo), which creates a copy of the repository under your github account to submit changes to.
2. [Clone the forked repository](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository) to your computer using the **Clone or download** button and the address from github.
   e.g. `git clone https://github.com/YOUR_USERNAME/Curriculum.git`
3. Change the working directory to your cloned project.
   Mac/Linux: `cd ./Curriculum`
   Windows: `cd .\Curriculum`
4. [Add a remote](https://help.github.com/en/github/using-git/adding-a-remote) link to our project repository in order to track changes. \
  HTTPS: `git remote add upstream https://github.com/EthBuilders/Curriculum.git` \
  or \
  SSH: `git remote add upstream git@github.com:EthBuilders/Curriculum.git`

> **Pro tip:** If you prefer to [use SSH on Github](https://help.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh), remember to update the links above to the SSH versions!

1. [Create and checkout new branch](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-branches) in your local project to start making changes.
   e.g. `git checkout -b <branch-name>`
   _Note: the `-b` is only required when first creating the branch (combines `git checkout` and `git branch`)_
2. If working on the section specifically, review the documentation before adding any changes you intend to make.
3. Make changes in your local project, including adding files or updating existing code.
4. Add the changed files and create a commit message describing the changes.
   e.g. `git add README.md` or `git add -A` for all changed files
   e.g. `git commit -m "update table of contents in readme"`
   _Note: more information on [writing a good commit message](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) can be found in the linked article_
5. Continue with 6 and 7 above until all changes are complete.

**When the changes are complete and you are ready to submit them to our project**, please follow the additional steps below.

10. Check that all of your submissions follow the relevant [Style Guides](#style-guides).
11. Push the changes to the origin repository on Github (your fork).
    `git push -u origin <branch-name>`
    _Note: the `-u` is only required when first pushing a new branch to the origin (your fork)._
12. On github, [submit the pull request (PR)](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests) to the upstream repository when changes are complete.
13. Follow all of the instructions in the [Pull Request Template - TBD]().

### Staying Up to Date

**It is important to always work from the most up to date code in our repository.** Before making any changes, always be sure that your local repository contains the most recent changes from the upstream repository (our project).

To update your local repository, follow the steps below.

1. Check what branch you are currently working on.
   `git status`
2. Check out the master branch of your local repository.
   `git checkout master`
3. Fetch changes from the upstream master repository (ours).
   `git fetch upstream master`
4. Rebase the changes from the upstream master respository into your local repository.
   `git rebase upstream/master`
5. Check out a new branch to make and submit changes, following the procedures in [Contributing Code](#contributing-code) starting from Step 5.

## Style Guides

### Naming Git Branches

**Use the branch naming structure of "verb/intent"**, and examples are listed below. This helps make branch names easier to read, understand, and follow for the project maintainers.

```
update/resource-list
feat/omni-auth
fix/auth-flow
```

### Creating Git Commit Messages

**Keep git commit messages short, simple, and informative**, ideally under 50 characters.

**Write commit messages in the imperative**, using "fix bug" and not "fixed bug" or "fixes bug". This convention matches up with commit messages generated by commands like `git merge` and `git revert`.

`git commit -m "update contributing.md with new sections"`

### Front End Style Guide

📝 TBD

## Getting Support

**We are here to help!** If you have questions or run into issues, please reach out to us on [our slack](http://bit.ly/NYC-Blockchain-Devs-Join-Slack).

We also have some [support documentation](SUPPORT.md) on common commands, common terminology, the general workflow, and a list of useful resources covering each topic above.

_If you made it to the end of this document, thank you, and we look forward to working with you and seeing your submissions!_

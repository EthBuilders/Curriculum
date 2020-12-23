# Open Source Collaboration

Before learning about the tools used for Open Source Collaboration, it's best
you get an idea of why they exist in the first place, and what exactly open source
means. The best place to start when learning about Open Source ofcourse would be the
source, pun possibly intended. The *Open Source Initiative* (a.k.a OSI) is a
non-profit corporation which is mission-bound to educate, advocate for, and build
bridges within the open source community. The OSI defines what Open Source is very 
clearly in the OSD (Open Source Definition) as, not just access to source code but
also about 9 other criteria.

Below are the 10 criteria taken from the [OSD](https://opensource.org/docs/osd):

1. Free Redistribution
   - No restriction of any party from selling or giving away the software as a component of an aggregate software distribution
   - Licensing shall not require a royalty or other fee
2. Source Code
   - The program must include source code, and must allow distribution in source code as well as compiled form
   - Deliberately obfuscated source code is not allowed
   - Intermediate forms such as the output of a preprocessor or translator are not allowed
3. Derived Works
   - The license must allow modifications and derived works, and must allow them to be distributed under the same terms as the license 
4. Integrity of The Author's Source Code
   - The license may require derived works to carry a different name or version number from the original software
   -  Must explicitly permit distribution of software built from modified source code
5. No Discrimination Against Persons or Groups
   -  Must not discriminate against any person or group of persons
6. No Discrimination Against Fields of Endeavor
   - Must not restrict anyone from making use of the program in a specific field of endeavor 
7. Distribution of License
   - The rights attached to the program must apply to all to whom the program is redistributed without the need for execution of an additional license by those parties 
8. License Must Not Be Specific to a Product
   - The rights attached to the program must not depend on the program's being part of a particular software distribution
   - All parties to whom the program is redistributed should have the same rights as those that are granted in conjunction with the original software distribution
9.  License Must Not Restrict Other Software
    - The license must not place restrictions on other software that is distributed along with the licensed software
    - Must not insist that all other programs distributed on the same medium must be open-source software
10. License Must Be Technology-Neutral
    - No provision of the license may be predicated on any individual technology or style of interface

Overall, participating in the Open Source ecosystem is quite simple but it is predicated on one simple rule. **Always add a license to your work**.
Adding a license allows others to comfortably contribute/use/modify your project without fear as it protects contributors and users.
Businesses and savvy developers won’t touch a project without this protection. Choosing a license isn't that tough either thanks to tools like
[choosealicense.com](https://choosealicense.com/), which helps you select a license that fits your project/needs.

Now, there exists a litany of tools used for open source collaboration, but to start the best thing to learn first is about Source Code Management (SCM) tools.
One of the biggest and most well known SCM tools is Git, and its use cases go far beyond just regular software development. It can be applied in many
different areas and businesses to simplify collaboration.

## Git

Git is a version control system (VCS), in a nutshell, git kind of works like the save functionality in a Microsoft Word document, except git is on steroids.
Unlike your regular word document which only keeps a single version of your document (the one which you saved), git keeps the entire history of saves you made to your document/project.
And better yet, git allows you to move around in that history like you're a time traveler (if you ever need to be), without much complication. The real benefit to using git however,
comes with the fact that it allows you to collaborate efficiently with other people/maintainers/contributors, even though you aren't working at the same time, in the same place, or
maybe don't even have access to the internet. Before I get ahead of myself, what is a VCS (version control system)?

> Version control systems are software tools that help software teams manage changes to source code over time.
> Version control software keeps track of every modification to the code in a special kind of database.
> If a mistake is made, developers can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption to all team members.  
> \- [Atlassian](https://www.atlassian.com/git/tutorials/what-is-version-control)

So onto the nitty-gritty and let's learn some basic git functionality to get you started.

### The Basics

When starting out with git, there really is only a few commands you need to know. For the purposes of this mini-tutorial I'm assuming you have a basic
understanding of how to use a shell. I highly recommend you take a brief moment to refresh yourself, or do some mini-practice ([Cheat Sheet](https://gist.github.com/cferdinandi/ef665330286fd5d7127d)).

The nine basic commands you'll need to know are:

- `git config`
  - A convenience function that is used to set Git configuration values on a global or local project level
- `git clone`
  - Clones a repository into a newly created directory
- `git checkout`
  - Updates files in the working tree to match the version in the index or the specified tree
    - Don't worry too much about knowing what the working tree, index, or staging are just yet, although you're more than welcome to take a deep dive
- `git status`
  - Displays paths that have differences between the index file and the current HEAD commit
- `git add`
  - This command updates the index using the current content found in the working tree
- `git commit`
  - Create a new commit containing the current contents of the index and the given log message describing the changes
- `git merge`
  - Incorporates changes from the named commits (since the time their histories diverged from the current branch) into the current branch
- `git pull`
  - Incorporates changes from a remote repository into the current branch
- `git push`
  - Updates remote refs using local refs, while sending objects necessary to complete the given refs.

The best way to learn is through doing so follow along below to get up and running. The only requirements are that you have git, bash (or zsh/fish), a text editor, and internet.

#### Walkthrough

> Note: In the code blocks below user commands are denoted by the '$' prefacing the line. If a line is prefaced by a '#' it requires super user (root) access.
> Always take caution when running commands, especially those that require super user access, as they have the potential to damage your system.  
> The main take away: ALWAYS UNDERSTAND WHAT A COMMAND DOES BEFORE USING IT!

**Step 1**: If you've never used git before you'll have to do some setup. This is only necessary the first time you install git, afterwards you'll be fine.

```bash
$ git config --global user.name '[*Enter your name here*]'
$ git config --global user.email '[*Enter your email here*]'
```

Note: These commands setup your global identity when using git, when you work on a project it lets you and others keep track of what you did. Therefore
your name and email will be available to anyone who can clone the repository.

**Step 2**: Time to clone a repository, in our case we'll just clone this one you're reading from (how meta).

```bash
$ git clone https://github.com/EthBuilders/Curriculum.git git-walkthrough
$ cd git-walkthrough
```

Congrats! You're on your way, and now have officially cloned a repository.

**Step 3**: Time to make sure you know how to move between branches.

Branches in git, are kind of like separate ... well separate branches on a tree. Branches typically have the same roots, but they can go in separate directions and that's okay.
One key thing to remember when collaborating with others, and especially with git, is to keep your master/main branch ready and bug free. This means you should almost always
work on a separate branch, and then combine your work when you are finished.

```bash
$ git checkout -b new-branch  # this command will only work if 'new-branch' doesn't exist, it creates a 'new-branch' and then switches to it
$ git checkout master  # this switches back to the master branch
$ git checkout new-branch  # this switches back to the new-branch
```

**Step 4**: Checking for changes is simple, and you should always constantly run `git status` to see what has been updated by you.

```bash
$ git status
```

Great job, it doesn't look like anything is modified but that's alright we'll change that shortly.

**Step 5**: Adding some changes

```bash
$ echo 'Hello world! My first git addition' > file.txt
$ git status
```

Your `git status` command should now return some more info telling you there is a new untracked file. Awesome now let's add it.

```bash
$ git add file.txt
```

**Step 6**: Time to commit, which takes your work and definitively saves it in the project history.

```bash
$ git commit -m 'My first commit'  # typically you'll use git-commit without the '-m' flag, but for simplicity this'll do
```

You've now contributed to the history of the project, but wait no one will ever know if it's just on your computer.

**Step 7**: Time to merge your changes back onto the master branch. Remember this is where everything that is ready and good to go belongs.

```bash
$ git checkout master  # switch back to the master branch
$ git merge new-branch  # merges the changes from new-branch into the master branch
```

Now both branches are equal and have the same history. BTW you can check out the history of the project by running `git log`.

**Step 8**: Always look before you leap, I think that's the saying. Either way it's a good habit to check for any changes made by your peers first
before pushing your changes.

```bash
$ git pull
```

Essentially in a nutshell, this command will sync your local copy of the repository with what's in the cloud (or wherever your repo is stored)

**Step 9**: Last but certainly not least. For projects/repos you're allowed to make changes to this command will work. If you don't I think it'll fail.
You should always check the repositories contributing guidlines to see any rules they may have. 

```bash
$ git push  # send your changes
```

There you go, you've essentially just learned the basic git workflow that many people use daily. Honestly you can go far with just knowing these nine (ten if you include `git log`) commands.
It's always recommended that you pick up some more along the way, but definitely get comfortable with these nine since they're the crux of using git, and you'll use them 99% of the time.

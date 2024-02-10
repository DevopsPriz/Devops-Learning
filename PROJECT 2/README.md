# INITIALIZING A GIT REPOSITORY AND MAKING COMMITS (GIT PROJECT)

## GIT

Git is a distributed version control system (VCS). Git is a DevOps tool used for source code management. Linus Torvalds created Git in 2005 for the development of the Linux kernel.
 
Git essentially addresses the issues of efficiently exchanging code and monitoring changes made to source code.

This version control system is free and open-source, and effective for handling small to very large projects. 

Multiple developers can collaborate on non-linear development by using Git, which is used to track changes in the source code. 

Other technologies, such as SVN, were available before Git to address this issue.

Some difficulties were raised by the way SVN solved this problem. There is a central source code repository in SVN. Developers always make changes against this central repository.

Because changes can only be made individually, this configuration makes it challenging for developers to work together. Second, the developers are essentially blocked if the central server fails or is unavailable for any reason.

A different strategy was adopted by Git. It permits developers to duplicate the central repository on their own. It is called a **Distributed Version Control System** for this reason.

## INITIALIZING A GIT REPOSITORY

### PRECONDITIONS:

1. Install Git on your machine.
2. Install and open your selected terminal, for example, git bash.
3. Move to the directory where you want to create your repository using `cd` command in the terminal. 
```Bash
`cd` Lessons
```
### To intialize a git repository

1. Run the command on bash terminal to create a working folder or directory eg: DevOps folder.
```Bash
mkdir DevOps
```
2. change directory into the working directory using the command:
```Bash
cd DevOps
```
3. In this working directory enter the command:
```Bash
git init
```
This will initialize a new git repository within your current directory. 

![Alt text](<images/Intializing a git repository.png>)

## Making first commit

`Commit` is more or less like saving the changes you made to your files. Changes can be `adding`, `modifying`, or `deleting` files or text. 

When you make a commit, git takes a snapshot of the current state of your repository and saves a copy in the `.git` folder

To make the first commit by following these steps:

- Inside the working directory create a file called index.txt using this command: 
```Bash
touch index.txt
```
- Write any sentence of your choice inside the text file. Save the changes.
- Add your changes to git staging area using this command:
```Bash
git add .
```
- To commit your changes to git, run the commnd:
```Bash
git commit -m "initial commit"
```
The -m flag is used to provide a message. The commit message is a nice way of providing context about the commit.

![Alt text](<images/first commit.png>)

## Working with Branches
Git allows us to work on multiple projects simultaneously without altering our main codebase.

It is common practice to develop new features for your application using the Git branch. Since the initial code has not been tested, it cannot be added to the live project's code base.

In remote teams, where developers work from different locations, the Git branch is a crucial tool for collaboration. They can work on the same feature in separate branches. Finally, converge their code into a single branch.

### Make first git branch

To make a new branch run this command: 
```Bash
git checkout -b 
```
The -b flag helps you create and change into the new branch.   
With that said let's make our first branch following these steps:   
- Make a new branch by running this command:
```Bash 
git checkout -b major
```
![Alt text](<images/new branch(major) command.png>)

## List git Branches
Use the command below to list the branches on your local git repository:
```Bash
git branch
```
![Alt text](<images/branch list command.png>)

## Change into an old branch
To change into an old or existing branch use the command below:
```Bash
git checkout <branch-name>
```
![Alt text](<images/change into an old branch.png>)

## Merging a branch into another branch
Let's say we have two branches "main" and "major". And we want to add the content of branch "main" into "major". First we change into branch "major" and run the git command below:
```Bash
git merge main
```
![Alt text](<images/merging branches command.png>)

## Deleting a git branch
When new feature is added to an application, its often done in a feature branch. Usually this feature branch is deleted when the code must have been tested and merged into a staging or dev environment depending on the branch strategy of the team.   
Git branch can be deleted with the command below:   
```Bash
git branch -d major
```
![Alt text](<images/delete branch command.png>)

## Collaboration and Remote Repositories

GitHub is a web based platform where git repositories are hosted. It becomes available in the public internet(it is possible to create private repository and limit who has access to the repository). Remote Teams can now view, update and make changes to the same repository.

- Create a github account.
- Create a new repository in your github account.
- Add a remote repository to your to your local repository by the command:
```Bash
 git remote add origin <link to github repo>
```
![Alt text](<images/remote add origin command.png>)

- After making changes, you can commit back to the Github repository by the command: 
```Bash
git push
```
![Alt text](<images/first commit.png>)

- You can clone remote Git repo by the command: 
```Bash
git clone <link to remote repo>
```
![Alt text](<images/cloning repository command.png>)
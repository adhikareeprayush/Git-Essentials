# Git Essentials🚂

In this tutorial, I will be discussing how to start using Git. This tutorial references multiple platforms and books that I have read. Follow along with the instructions to master Git. So, let's get started.

### Table of Contents

The contents of the tutorial are divided as follows:

1. [Why use Git?](#why-use-git)
2. [How does Git work?](#how-does-git-work)
3. [Install and configure Git](#install-and-configure-git)
4. [Push your code with Git](#push-your-code-with-git)
5. [Make changes to files](#make-changes-to-files)
6. [Important concepts in Git](#important-concepts-in-git)

### Why Use Git?

#### Version Control

One of the main reason of using git is for version control. A version control system can be used to track the changes in the code.
Let's take a senario where we have multiple versions of our project in our local storage.

![1716872273010](image/README/1716872273010.png)

In above example, I have seperate folders of all the changed codes as versions of my project. It is very hard to maintain and stresses me out😖.

Using git just simplifies the process. We can change the code and create separate versions of our code/project as commit which is stored in the git locally or remotely. Then we can access the dififerent versions of our project. lets take a visual representation of what I have just said🤯.

![1716872828495](image/README/1716872828495.png)

Can git be used only locally? What will happen if my hard disk is damaged? What if I lost my computer?

For these types of situations we can use **Git Provider .** By using git provider we can store the projects both locally and on the cloud too.

#### To Share Code

What if more than one person is working on a project or take instance of 10 people working on the same project.

Let's assume one person makes changes now the changes must be synced with all other people codebase. What can you do in these kind of situations?

![1716873878825](image/README/1716873878825.png)

Well the first answer comes to my mind is **_I WOULD USE GIT_**. Using git provider we will be able to share the codes with our team easily.

#### To Colaborate

Git is used for collaboration. When there are more people working on a same project they can be added as collaborator. We use git provider to establish a remote connection and then share the code as mentioned earlier. Git also is very intelligent machine that can merge two codes into a single one but sometime it can fail. So as a responsible citizen we sometime have to merge the code ourselves.

#### Open Source

Open Souce means the code which is publicly available. You can download it, you can modify it, create your version of it and publish it.

We can observe that a community works on a open source project and detects the bug, fixes it, improves the code and many more. Git has many features like branches which make the open source contributions easy.

### How does Git work?

Let's see some technical part of git. We will learn how to use git locally, use git provider and gain some knowledge on distributed version control.

#### Using Git Locally

While using git locally on our local computer we have three stages. The first is the local folder. We make some changes in the local folder then after the command `git add filename` we will get into the staging area which makes clear to the git that which files are we going to change in the git repo. After this we will use the command `git push` to move the saved files into the local git repo.

![1716878267484](image/README/1716878267484.png)

#### Use a git provider

Using a git provider we can use `git push` to make to code available to others in the remote repository in the git ptovider and use `git pull` to pull the changed files.

#### Distributed Version Control

In disctributed version control, all the clients have their seperate database with all the files, snapshots and history. We also have a central git provider. And if i pull some files from the git provider we not only pull files we also pull the complete history of the files. Which means that, even if something happens to the git provider we all have copy of our project

### Install and configure Git

#### Downloading

Let's start working with git by installing git in your respective os. You can download git for your os from the link: [https://git-scm.com/downloads](https://git-scm.com/downloads)

#### Installation

Installing git is pretty simple, select the required changes if you want to make any otherwise go with the flow and install the git.

#### Configuration

All the configurations for git is done through file gitconfig

There are few config files and the most important one are the two scopes:

- Global:
  ~.gitconfig
  C:\Users\[user\.gitconfig]
- Local: For a specific repository
  .git/config

Local settings can overwrite the global settings.

#### Showing the configuration

Type the command `git config --list` into the terminal to view the config

**Before Starting lets add the two necessary configs for the git**
We have to set a global username and email for git. In order to do it, we have to type the following command and be sure to replace the username and email with yours. Remember it is mandatory to setup these two configs in order to use git.

- **_UserName_**
  `git config --global user.name "Your_name"`

- **_Email_**
  `git config --global user.email "name@example.com"`

### Push your code with Git

In this section, we will learn to create a new repository and work with it. For this we will use git provider **Github**. You can use any other git provider but I am going with github.

#### Setting up a remote repo

There are few steps to create your new repository lets review each:

- After Signing up to github visit: https://github.com/new
- You have to name your repository, choose the visibility and add readme if you want and get started

#### Cloning the remote repository

In order to clone the remote repository you have to follow the steps:

- Open the github repo
- Click on the Green code dropdown
- Copy the HTTPS url
- Open your local folder where you want to clone the repo
- Open the terminal
- Type `git clone <the code>` (Replace the code with the HTTPS url)
- `cd <repo-name>` to open the repo in terminal
- `code .` to open the repo inside vscode.

#### Creating a file and staging it

Follow the steps:

- Create any file, add changes and save
- In order to put the file in the staging state type `git add <filename>`
- If you wanna check which files are in staging area you can do it by typing `git status`
- Now in order to commit this file locally, you can simply type `git commit -m "first commit"`
- Since the file on the staging area is committed you may reverify the process by using `git status`

#### Pushing file to remote repo

Follow the steps:

- To push the local repo changes to remote repo, type `git push`
- Check the github repo from the browser to confirm the changes

#### The .git folder

### Make changes to files

### Important concepts in Git

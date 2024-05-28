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

The `.git` folder is a fundamental component of a Git repository, acting as the storage for all the metadata and object data that Git needs to manage the version history of a project. When you initialize a Git repository with `git init`, Git creates this hidden `.git` directory in the root of your project.

**_Structure of the .git Folder_**

The `.git` folder contains several subdirectories and files, each serving a specific purpose. Here is an overview of the primary components:

- **config**: This file contains the configuration settings for the repository, such as user information, remote repository URLs, and other Git settings.

- **HEAD**: This file points to the current branch reference, indicating where Git should look for the latest commit in the checked-out branch.

- **index**: Also known as the staging area, this file stores information about the files that are staged for the next commit.

- **logs/**: This directory contains logs of all reference updates, helping to track changes to branches and HEAD.

- **objects/**: This directory stores all the objects (blobs, trees, commits) that make up the history of the repository. Git objects are identified by their SHA-1 hash.

- **refs/**: This directory contains references to commit objects. It includes subdirectories for heads (branches), tags, and remotes.

- **hooks/**: This directory contains client- or server-side scripts that are triggered by various Git actions, such as commits or merges. These can be used for tasks like enforcing commit policies or automating testing.

**Use of the .git Folder**

The `.git` folder is crucial for the functionality of Git, as it holds all the information about the repository's history and state. When you perform Git operations like commit, push, pull, or merge, Git reads from and writes to the files in the `.git` directory to manage changes and keep track of the project's history.

Here’s a brief explanation of common Git commands and how they interact with the `.git` folder:

- **git status**: Checks the current state of the working directory and staging area, using information from the `.git/index` file.
- **git add**: Stages changes to be committed, updating the `.git/index` file.

- **git commit**: Records changes to the repository, creating a new commit object in `.git/objects` and updating references in `.git/refs`.

- **git log**: Displays the commit history, reading from the commit objects stored in `.git/objects`.

Understanding the structure and purpose of the `.git` folder helps in comprehending how Git manages and tracks project changes, ensuring a reliable version control system.

#### Initializing empty repo locally and sync to remote

Follow the steps to get started:

- Create a new repo locally by creating a folder and running `git init`
- `git add .` for adding the files to staging area
- `git commit -m "first commit"` to make the files commit to the local repository
- Now in order to connect this local repository with remote repository you have to create a new repo in github or any other git provider and get thee HTTPS or SSH link to the repo
- Run the command `git remote add origin <the-link>`
- Since I have branch locally but don't have any branch setup in the remote repository I have to set the branch in remote repo and push the code I can achieve both by running `git push --set-upstream origin main`

### Make changes to files

#### Introduction to `git status`

The `git status` command in Git provides a comprehensive overview of the current state of your working directory and staging area. It helps you track changes and understand what is happening in your repository.

**Purpose of `git status`**

- **Changes to be committed**: Shows files staged and ready for commit.
- **Changes not staged for commit**: Lists modified files that are not yet staged.
- **Untracked files**: Identifies new files not being tracked by Git.

**Typical Output**

Running `git status` might produce an output like this:

```plaintext
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
    modified:   file1.txt
    new file:   file2.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
    modified:   file3.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
    file4.txt
```

**Effective Use**

- **Before committing**: Ensure all intended changes are staged.
- **After modifying files**: Check which files need staging.
- **After pulling changes**: Verify the state and address conflicts if any.

Regular use of `git status` keeps you informed about your repository's state, aiding in effective version control and smooth workflow management.

#### Introduction to `git diff`

The `git diff` command in Git is used to show the differences between various states of a repository. It helps you see what has changed in your files before committing those changes.

**Purpose of `git diff`**

- **Working Directory vs. Staging Area**: Shows changes in the working directory that are not yet staged.
- **Staging Area vs. Last Commit**: Shows changes that are staged but not yet committed.
- **Two Commits or Branches**: Compares changes between any two commits, branches, or tags.

**Basic Usage**

- **Compare working directory to staging area**: `git diff`
- **Compare staging area to last commit**: `git diff --cached`
- **Compare specific file**: `git diff <file>`
- **Compare two commits**: `git diff <commit1> <commit2>`

**Example Output**

Running `git diff` might produce an output like this:

```plaintext
diff --git a/file1.txt b/file1.txt
index d3ff2c6..f7c3f58 100644
--- a/file1.txt
+++ b/file1.txt
@@ -1,3 +1,4 @@
 Line 1
 Line 2
+New line 3
 Line 4
```

**Effective Use**

- **Before Staging**: Run `git diff` to review changes in the working directory.
- **Before Committing**: Run `git diff --cached` to review staged changes.
- **For Specific Comparisons**: Use commit hashes to compare specific versions.

By regularly using `git diff`, you can closely monitor and manage changes, ensuring accuracy and intentionality in your commits.

#### Introduction to `git log`

The command `git log` as the name refers is used to view all the commits history.
It gives us the follwoing info:

- Commit hash through which you can rollback to that commit
- Author Name and email of the user who made the commit
- Date and time of the commit
- The commit message

You can also use something like `git log --graph` which represents the same thing in graphical format...

Lets us take a look what we can do with the **Commit hash**

- `git show <commit-hash>` can be used to view the files changed and the changes during that commit

**What if you wanna search the details for a specific commit?**
The answer is `git log --grep='your_commit'`.

#### Renaming a file

You can rename a file using git (Not a big deal). The commamnd for renaming a file using git is `git mv current_name new_name`

#### Working with folders

**Empty folders don't get push**. By default git doesn't keep the track of epty folder but if we want to keep track of an empty folder we just have to create a file `.gitkeep` inside that folder.

#### Undoing the changes

Let's see how can we undo the changes that have been added to the staging area. By now you must have been clear that `git add .` adds all the files changed into the staging area. For now let's take an example of a file `example.txt`. I am following the steps below:

- Made some changes to `example.txt`
- `git add example.txt`
- To check if the file is added to the staging area or not type `git status`
- `git restore --staged example.txt`
- Again to verify if the file is removed from staging area type `git status`

Not only the staged changes can be reversed using restore we can use `git restore` to even restore the changes made to a file.

- Make some changes to `example.txt`
- `git status` to see the change is made
- `git restore example.txt` to revert the changes in the file

#### Look back in history

### Important concepts in Git

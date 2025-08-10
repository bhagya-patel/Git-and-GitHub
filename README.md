# Git-and-GitHub

🔹Git VS GitHub
![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/1.png)

🔹Git & GitHub short Notes

There is a term Source Code Management and it has two types:–

CVCS — Centralized Version Control System

DVCS — Distributed Version Control System

CVCS — Centralized Version Control System

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/2.png)


It is not locally available, meaning we've always needed to be connected to a network to perform any action.

Since everything is centralized, if the central server gets failed, you will lose the entire data

DVCS — Distributed Version Control System
![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/3.png)

In DVSC, every contributor has a local copy or ‘clone’ of the main repository i.e. everyone maintains a local repository of their own, which contains all the files & metadata present in the main repository.

Why do we need Source Code Management as a DevOps Engineer?

To use the CICD pipeline in DevOps, you must have the most recent project updates on hand. Because DevOps monitors the most recent code and creates definitions that execute a variety of tasks by user needs, the release definitions that assist in deploying the most recent binaries on your primary environment also use these definitions. Any end server where the finished product is made ready for usage might be your client computer, the production environment, or both.


🔹Important Terms

🔹 Repository

A repository is a place where you have all your codes or kind of folder on the server.

It is a kind of folder related to one product.

Changes are personal to that particular repository.

🔹 Server

It stores all repository.

It contains metadata also.

🔹 Working directory

Where you see files physically and do the modification.

At a time, you can work on a particular branch.

🔹 Commit

Store changes in the repository. You will get one Commit-Id.

It is 40 Alpha–Numeric characters.

It uses the SHA1 checksum concept.

Even if you change one dot, Commit-Id will change.

Commit is also named the SHA-1 hash.

🔹 Commit Id / Version-Id / Version

Reference to identify each change.

To identify who changed the file.

🔹 Tags

Tags assign a meaningful name with a specific version in the repository.

Once a tag is created for a particular save, even if you create a new commit, it will not be updated.

🔹 Snapshots

Represents some date of a particular time.

It is always incremental i.e. it stores the change (append date) only. Not the entire copy.

🔹 Push

Push operations copy changes from a local repository server to a remote or central repository.

This is used to store the changes permanently in the Git repository.

🔹 Pull

Pull operation copies the changes from a remote repository to a local machine.

The pull operation is used for synchronization between the repository.

🔹All about Git Branch

The product is the same, so one repository but a different task.

Each task has one separate branch.

Finally, merges (code) all branches.

Changes are present in that particular branch.

The default branch is master.

Files created in the workspace will be visible in any of the branch workspaces until you commit. Once committed, the file belongs to that particular branch.

After finishing the code, merge other branches with Master.

This concept is useful for parallel development.

You can create any number of branches.

When a new branch is created, data from the existing branch is copied to the new branch.

🔹Commands

(1). git init

git init is a Git command used to initialize a new Git repository in your project directory. It is usually the first command you run when starting a new project you want to track with Git.

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/4.png)

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/5.png)

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/6.png)

(2). git status

The git status command shows you what's going on in your working directory and staging area. It's one of the most commonly used Git commands because it tells you:

Which files are untracked

Which files have been modified

Which files are staged and ready to be committed

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/7.png)

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/8.png)

🔹Git File Life Cycle

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/9.png)

🟠 1. Untracked

Meaning: The file exists in your working directory but Git doesn't know about it yet.

Example: You create a new file hello.txt, but haven’t told Git to track it.

Command to move to next state:

git add hello.txt

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/10.png)

If you want to go back from the staged state to the untracked state, use the following command:

git rm --cached <file name>

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/11.png)

if you want to add all untracked file

git add .

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/12.png)

➡️ Moves to → Staged

🟡 2. Staged

Meaning: The file is marked to be included in the next commit.

It’s stored in Git’s staging area (also called the "index").

Command to move to next state:

git commit -m "your commit message"

here, The -m option in the git commit command is used to provide a commit message inline — directly in the terminal — instead of opening a text editor.

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/13.png)

➡️ Moves to → Committed

🟢 3. Committed

Meaning: The file and its content are now saved in Git’s version history.

Git is now tracking this file.

At this stage, the file is clean (unmodified).

If a file has already been committed, and you delete it, you can restore it using Git.

git restore

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/14.png)

🟠 4. Modified

Meaning: You've made changes to the file since the last commit.

Git detects that the file is tracked but now has unsaved changes.

Command to move to next state:

echo "Update" >> test.txt # Now Modified

git add test.txt # Staged again

git commit -m "Updated file"

➡️ Moves back to → Staged, and the cycle repeats.

(3). git branch

A branch in Git allows you to diverge from the main line of development and continue to work without affecting the main codebase (usually the main or master branch).

Command

Description

git branch

List all local branches

git branch <branch-name>

Create a new branch

git checkout <branch-name>

Switch to an existing branch

git checkout -b <branch-name>

Create and switch to a new branch

git merge <branch-name>

Merge the specified branch into the current one

git branch -d <branch-name>

Delete a local branch

git push origin <branch-name>

Push a branch to a remote repository

git branch -r

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/15.png)

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/16.png)

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/17.png)

List remote branches

The changes committed on the dev branch are not visible on the master branch until they are merged.

(4). git log --oneline

This command shows the Git commit history in a condensed format:

✅ One line per commit

✅ Short commit hash (e.g., a1b2c3d)

✅ Commit message

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/18.png)

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/19.png)

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/20.png)

🔹Local to GitHub(Remote) and GitHub(Remote) to Local

Here’s a clear and concise comparison of the two main ways to connect your local Git repository to GitHub:

✅ 1. Using PAT (Personal Access Token) via HTTPS

✅ 2. Using SSH Key Authentication (Recommended for Developers)

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/21.png)

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/22.png)

✅ 1. Using PAT (Personal Access Token) via HTTPS

after it shows a token then copy it and paste it.

(5). git remote -v

is used in Git to list all the remote repositories associated with your local Git repository, along with their URLs.

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/23.png)

(6). git remote add origin <link>

is used to add a remote repository to your local Git project, and name it origin.

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/24.png)

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/25.png)


(7). git remote set-url origin <link>

is used to update the remote repository URL (origin) and embed a personal access token (PAT) for authentication.

A personal access token can be used here, as Git no longer accepts a username and password for authentication.

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/26.png)

(8). git push origin master

This command pushes the latest commits from your local master branch to the remote master branch on the origin remote (e.g., GitHub).

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/27.png)

(9). git pull origin master

git pull origin master will:

Connect to the remote repository named origin.

Download the latest commits from the master branch on that remote.

Automatically merge those commits into your current local branch.

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/28.png)

![image alt](https://github.com/bhagya-patel/Git-and-GitHub/blob/cd00e56770584c3318ec9f878007c4b0375dd54c/screenshots/29.png)

here we pull a new.txt in local

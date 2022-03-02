---
layout: page
title: Portfolio
subtitle: Software Engineer | Quality Assurance Engineer | Enthusiastic Researcher
---

## 🥇 Git rapid experience

> Git belongs to a family of version control systems that are referred to as “distributed.” In a distributed system, everyone who clones a repository gets a full copy of the repository.

### ⚓ The three stages of Git

***Untracked file*** – git does not have history about it - only exists in working directory

***Tracked file*** – a file git cares about

***Staged file*** – a file added to the index area (staged) - git started to care by tracking it

***Unmodified file*** – a file moved from staging area to commit object database

***Modified file*** – a file edited after being stored in the database


### 🎂 Essential commands on git instructions

```git status``` - query repository and display history information - in no way affects the repository

```git init``` - initialize local git repository 
<details>
<summary markdown="span">more details</summary>
The command creates hidden directory .git with hidden config files and commit objects repository to save changes snapshots. 

On defaults creates a working branch, named master or main, depending on the git version (older versions use master)
</details>

```git add <filename>``` - git makes a copy of a file and puts it in the index area - the index is a place to temporarily house changes - terminologically, the index is the “staging area” that hosts objects before storing them into the repository.

```git commit [-m <msg>]``` - records changes to the repository

<details>
<summary markdown="span>"> more details </summary>
It takes the content of the staging area and stores it in the database.

When we commit, git creates a commit object that records the state of the index in its memory. Changes are stored in object database. Each object has a reference to the changes together with information as timestamp, hash id, author etc.
</details>

### 🌴 Branching

> The branch represent line of work, independent of other branches.
> Following good practice, generation of branches follows new features, resolving issues or experimental workspace.
> Each branch contains changes snapshots - commits. For navigation through git tree, braches and commits, the user location is regulated with HEAD reference. Where HEAD points, there you are :)

```git switch [-c | --create] <branch name>``` - switch on a specified branch - with parameter --create, create a new branch and switch to it in one fell swoop.

```git branch [-a] [-v] [-d] [-D] [-m] [-vv] <name>``` - create a new branch - best practice name for branch includes: _<initials>/<issue_number>/<short_description>_. Git helps and puts an asterisk next to the branch that we are currently using.
- [-a] - show all branches
- [-v] - show all branches with top commit hash id
- [-d] - delete a branch
- [-D] - force delete
- [-m] - rename a branch
- [-vv] - very verbose

```git merge <branch-name>``` - takes changes from the branch _<branch-name>_ and merges the content to the HEAD branch (one in which we are located).

> HEAD\~1 references the first parent of the commit you are on (remember commit reference each other in child -> parent relationship. Thus build asymmetrical tree). 
> HEAD~2 means the parent of the parent of the commit you are, and so on and so forth.
> Git offers another operator that works with HEAD: the caret (^), which helps when you’re navigating from commits with multiple parents (merge commits)
>
>HEAD^1~2 – navigate to first parent, find the parents parent

### :mouse: Listing repo

```git log [--abbrev-commit] [--oneline] [--all] [--graph]``` - lists all the commits in the current branch, with the latest commit at the top, followed by its parent, and so on.

- [--abbrev-commit] - shows shortened hashes
- [--pretty=oneline] - shows commits’ info in a line
- [--all] - displays all branches in the repository
- [--graph] - displays the commits as a graph


```git diff [--word-diff] [--cached | --staged] <commit> <commit>``` - find the difference between lines of committed files

<details>
<summary markdown="span>"> more details </summary>
The git diff command is always comparing two sets of changes, which can be visualized by a Venn diagram. The first argument is the set on the left (always indicated by “a/”) and prefixed with a minus (“-”). The second argument is the set of the right, indicated by “b/”, and prefixed with a “+”.
</details>

- [--word-diff] - shows how individual words differ rather than how lines differ 
- [--cached | --staged] - tells git to compare the content of the object from database with those in the index

### :rabbit: Fixing mistakes by undoing

```git restore [--staged]``` - discards any changes in the working directory.
- [--staged] - moves files from staged state to unstage

> Git commits are immutable. That is, once you create a commit, that version of the commit is preserved. Any edits to the commit (like amending it) will create a new commit that replaces the old commit in your history.

```git rm [-r] [--cached]``` - removes tracked files from the working directory and from index
<details>
<summary markdown="span>"> more details </summary>
Versions of the file that were previously committed remain as they were in the object database. This is because a commit represents the changes you made at the time of the commit. If a file existed at the time a commit was made, the commit will remember that for as long as the repository exists.
</details>

```git mv``` - renames or moves the files you tell it to in both the working directory and the index

> Git allows for editing commit messages using the git commit command, with a special flag called --amend.
git commit --amend -m “message>
> The first thing to check is that you are on the same branch as the commit you wish to edit (you need to have a clean working directory).

### 🏴 Undoing commits

```git reset [--soft] [--mixed] [--hard]``` - has two immediate effects —it moves the HEAD and the branch to the commit you specify
- [--soft] - takes the edits you committed and moves them back into the index, and then from the index it copies those changes into the working directory alone.
- [--mixed] - does a bit more work than the _--soft_ mode does. It has two steps:
    1.	Moves the changes in commit B (the commit you are undoing) into the index, and then copies those changes from the index into the working directory, just like --soft mode does.
    2.	It then copies the contents of commit A into the index. That is, the index now looks exactly like the commit you just reset to. 
- [--hard] - takes what the --mixed mode does to its logical end. In mixed mode, the second step copies the contents commited in “A” into the index, and stops there. --hard mode does not. It takes the contents of the index (which have the changes as they are in commit A) and overwrites the working directory. This means that the object database, the index, and the working directory all look the same. It’s as if commit B never happened! After a hard reset, the working directory, the index, and HEAD all point to commit “A.”

```git revert``` - is to be given the ID or reference of the commit you want to undo - looks at the changes introduced in B and calculates the anti-commit - this is an actual commit that Git will prepare -you are not erasing commits - rather, you are adding new commits.

### 🤿 Working with remotes

> The remote repository and the local copy are completely independent of one another

```git fetch [-p | --prune] <repository_name> <branch>``` – updates the remote tracking branches and info on the latest commits
- [-p | –-prune] - lean up all remote tracking branches that no longer have a remote counterpart

> Remote tracking braches origin/<branch_name> cannot be switched or changed, they serve git as a reference to what is happening to remote

```git pull``` – copies the remote repository to local repository - _git pull_ is _git fetch_ + _git merge_

```git remote -v``` – print name of the remote repository, url and push or fetch actions

```git config –global push.default <branch_name>``` - set the name of a branch to push on default without specifying it - default is master

```git push``` – pushes changes to remote - name of remote repository is origin - git knows where to push because the git clone records the URL of the remote - change remote with config

> When you attempt to push a branch to the remote, git tries to figure out exactly which remote branch it should update. But if the branch is brand new, Git won’t see a counterpart in the remote.

```git push –set-upstream origin <new_branch_name>```

### 💺 Searching repos


```git blame <file-name | commit-id>``` - annotate any tracked file in a the repository - shows, on a per-line basis, details about the latest commit that changed that line, including the commit ID, the author info, and the date the change was made.

```git grep [-i | --ignore-case] [-n | --line-number] ``` - search the contents of all tracked files in repository (default is case-sensitive).

- [-i | --ignore-case] - search case-insensitive.
- [-n | --line-number] - display the line number for a match.
- [-n | --line-number] - display the line number for a match.
- [-l | --name-only] - list just the names of the files.
- [-S | --name-only] - list just the names of the files.

```git log [-S] [-p | --patch] [-G]``` - shows the commit logs

- [-S] - find which commit added or removed a piece of text - search the entire commit history - limit to inspect the history of a single file by supplying the name of the file.
- [-p | --patch] - display the patch introduced in every commit using the -p (shorthand for --patch) flag. This can be combined with the -S flag to see if the search text was added or removed in a particular commit.
- [-G] - find all commits where the line that contains a piece of text changed


```git checkout <commit-id``` - “flip back” to any commit in your commit history - will rewrite your working directory to look like it did when you made that commit.

> Checking out a commit puts you in “detached HEAD” state. This means that you are no longer working on a branch.
You can continue to make editions and commits, but switching away from that commit history means you will abandon your commits (since they are not referenced by a branch).
It’s best not to make any commits when you are in detached HEAD state. Always work on branches.

```git bisect <commit-id>``` - you can search for commits that introduced a typo or a bug using the git bisect command, which uses the binary search algorithm to navigate your commit history, and quickly zero in on the commit you are looking for.

>At each step in a git bisect session, Git checks out a commit, leaving you in detached HEAD state. Since Git will rewrite your working directory, you can look around to see if you spot the unwelcome behavior.
Depending on whether you see the issue, you can tell Git if the current commit is “good” or “bad”, which informs Git which direction in the commit history to search for. This repeats till you’ve isolated the commit with the reported issue


### :tiger: Configuring git

> Git is extremely customizable. You can set and override many settings using the git config command.

```git config --global ``` - allows to create settings that affect every repository you work in on that particular workstation.

> All global settings are stored in a file called .gitconfig, which is stored in the home directory under your account. It consists of sections and keys under a section, each associated with a value.
You’ll have to configure some settings, like user.name and user.email, to be able to use Git. Others, like core.editor, override Git’s defaults and are optional.

```git config --local``` - store certain settings at the repository level, that is, local to a specific repository.

```git config --list``` - list all settings.

> Most, if not all, projects require that some files never be committed. You can tell Git to ignore an untracked file. Once ignored, it will remain forever untracked.
To tell Git to ignore a file, create a .gitignore file at the root of your repository that lists all the files you wish to ignore.

> “Commit early, commit often” is the mantra when it comes to working with Git. Recording snapshots of your work regularly is a good habit to develop.
Think of each commit in terms of its scope, not its size. Try to group changes together logically.

> Use consistent and informative commit messages. This can be helpful when reading the output of the git log command or searching for a commit using git bisect.

> Create contexual and meaningful branch names that help discern which branches are yours and what their purposes are.

### 🏸 Something more advance

```git tag [-l | --list]``` - record thes current ID (that is, where HEAD points to) in the tag. However, you can supply a specific commit ID after the tag name. _git tag 2.0.0 <commit_id>_
- [-l | --list] - list all the tags in the repo

```git cherry-pick <commit_id>``` - copy a commit to another branch

```git stash``` – stash your changes, git stuffs them away in a special location - leaves your working directory clean to switch branches - think of a stash as a sort of pseudo-commit

> The difference between stash and commit is that stashing records the changes in both your working directory and the index, as opposed to a commit, which only records what is in your index. The other difference is that a commit adds to your commit history, while a stash does not. If you push, your stashes don’t go along for the ride, they remain in your local Git repository.

```git stash pop –index``` - to return changes from stash stack

```git reflog``` - maintains a log called the reflog, (short for reference log) that is updated every time HEAD moves

```git rebase``` - rebasing “flattens” the history—you end up with a straight line. Rebases new branch on top of the master branch commit.

This will tell git you want to start ignoring the changes to the file
```git update-index --assume-unchanged <path/to/file>```

When you want to start keeping track again
```git update-index --no-assume-unchanged path/to/file```


```git log --follow --all -p <path/to/file``` - displays commits info that introduces changes on the file

# Intro to Git

Git is one of the most important tools in software development. It is used to track changes in code over time.

My simple explanation: Git is like a save system for a coding project. Not just one save button, but a history of important checkpoints. If you make a bad change, you can look back at what changed, compare versions, or go back to an older version.

The official Git book describes version control as a system that records changes to files over time so you can recall specific versions later: [About Version Control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control).

## Git vs GitHub

Git and GitHub are not the same thing.

- **Git** is the version control software. It runs on your computer.
- **GitHub** is a website where you can store Git projects online, share code, and collaborate with other people.

You can use Git without GitHub. But GitHub is very popular because it makes it easier to back up code, review changes, and work with other people.

GitHub's Git basics are here: [GitHub Git basics](https://docs.github.com/en/get-started/git-basics).

## Why Git matters

Imagine you spend a few months building an app. It works pretty well. Then you start a big new feature. A few weeks later, you realize the feature was a bad idea and the app is now broken.

Without Git, you might have no easy way to know exactly what changed.

With Git, you can make commits as you work. A commit is a saved checkpoint with a message attached. For example:

```text
added login page
fixed jump button bug
updated README
```

Future you, your teammates, or even an AI coding agent can look at the history and understand why the project changed.

## The basic Git idea

Most beginner Git work follows this loop:

1. Change files.
2. Check what changed.
3. Choose which changes to save.
4. Commit those changes.
5. Push the commit to GitHub if you are using GitHub.


```text
Working files -> Staging area -> Commit history -> GitHub
```

- **Working files**: The files you are editing right now.
- **Staging area**: The changes you are preparing to commit.
- **Commit history**: The saved checkpoints in your project.
- **GitHub**: The online copy of your project, also called a remote.

The Git book explains these file states here: [What is Git?](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F).

## Starting a Git project

If you already have a project folder on your computer, go into the folder and run:

```bash
git init
```

That tells Git to start tracking the project.

If you created an empty repository on GitHub and want to connect your local project to it, add the GitHub repository as a remote:

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
```

`origin` is the common nickname for your main online repository. GitHub explains remotes here: [Managing remote repositories](https://docs.github.com/en/get-started/git-basics/managing-remote-repositories).

## The commands you actually need first

### `git status`

Shows what changed and what is staged.

```bash
git status
```

Example idea:

```text
Changes not staged for commit:
  modified: intro-to-git.md

Untracked files:
  notes.md
```

This means `intro-to-git.md` already exists in Git and has been changed. `notes.md` is new and Git is not tracking it yet.

### `git add`

Adds changes to the staging area.

Add one file:

```bash
git add intro-to-git.md
```

Add all current changes:

```bash
git add .
```

I like thinking of `git add` as saying: "Yes, include this in my next checkpoint."

### `git commit`

Creates the checkpoint.

```bash
git commit -m "write intro to git"
```

The message should be short, but useful. A good commit message says what changed.

Good:

```text
fix broken login button
add homepage layout
update install instructions
```

Less useful:

```text
stuff
changes
final final
```

### `git push`

Uploads your commits to GitHub.

The first push for a new branch often looks like this:

```bash
git push -u origin main
```

After that, you can usually just run:

```bash
git push
```

GitHub explains pushing here: [Pushing commits to a remote repository](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository).

### `git pull`

Downloads changes from GitHub and updates your local files.

```bash
git pull
```

Use this when someone else changed the project online, or when you worked on another computer and need the latest code.

### `git fetch`

Downloads information from GitHub without changing your files yet.

```bash
git fetch
```

For beginners, `git pull` is usually enough. `git fetch` is useful when you want to see what changed before merging it into your current work.

GitHub explains getting remote changes here: [Getting changes from a remote repository](https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository).

## A simple beginner workflow

When you make a change, do this:

```bash
git status
git add .
git commit -m "describe what changed"
git push
```

Before you ask an AI agent to make a big code change, it is a good idea to commit your current work first. That gives you a clean checkpoint. If the agent makes a mess, you can see exactly what changed.

## Branches

A branch is like a separate path of work.

If you are working alone and just learning, you can use `main` most of the time. That is fine. Branches become more useful when:

- You want to try an idea without touching the main version.
- Two people are working on the same project at the same time.
- You want to review a change before adding it to `main`.

Create and switch to a new branch:

```bash
git switch -c feature-name
```

Switch back to main:

```bash
git switch main
```

Git explains branches here: [Branches in a Nutshell](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell). GitHub also has a shorter explanation here: [About branches](https://docs.github.com/articles/about-branches).

## Pull requests

A pull request, often called a PR, is a request to merge one branch into another branch.

In normal words: "Here are my changes. Please review them before they become part of the main project."

Pull requests are very useful for teams because people can comment on code, ask questions, run tests, and approve changes before merging.

If you are working alone, you do not always need pull requests. But they are still useful practice, especially if you want to learn how real software teams work.

GitHub explains pull requests here: [About pull requests](https://docs.github.com/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests).

## `.gitignore`

You may see a file named `.gitignore`.

This file tells Git what not to track. For example, you usually do not want to commit:

- Secret keys or passwords.
- Big dependency folders like `node_modules`.
- Build output files.
- Temporary files made by your computer or editor.

Example `.gitignore`:

```text
node_modules/
.env
dist/
*.log
```

GitHub explains ignored files here: [Ignoring files](https://docs.github.com/articles/ignoring-files).

## Commands cheat sheet

```bash
git init                         # Start Git in this folder
git status                       # See what changed
git add file-name.md             # Stage one file
git add .                        # Stage all changes
git commit -m "message"          # Save a checkpoint
git remote add origin URL        # Connect to GitHub
git push -u origin main          # First push to GitHub
git push                         # Push later commits
git pull                         # Get latest changes and update files
git fetch                        # Get remote info without changing files
git switch -c branch-name        # Create and switch to a branch
git switch main                  # Switch back to main
```

## The main point

Git is about tracking and organizing changes. GitHub is about storing and sharing those changes online.

You do not need to master every Git command at the start. Learn the basic loop first:

```bash
git status
git add .
git commit -m "message"
git push
```

That small loop is enough to start building good habits. Also ask LLMs/Agents for help with git, they are great at it.

## Helpful links

- [Official Git book](https://git-scm.com/book/en/v2)
- [GitHub Git basics](https://docs.github.com/en/get-started/git-basics)
- [Managing remote repositories](https://docs.github.com/en/get-started/git-basics/managing-remote-repositories)
- [Pushing commits to GitHub](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository)
- [Getting changes from a remote repository](https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository)
- [About branches](https://docs.github.com/articles/about-branches)
- [About pull requests](https://docs.github.com/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)
- [Ignoring files](https://docs.github.com/articles/ignoring-files)

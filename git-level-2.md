# Git Level 2: Work Locally

This level is for students who have seen Git or GitHub before, but do not feel confident yet.

You will take the repo from Level 1, clone it to your computer, make a branch, edit the README locally, commit the change, and push it back to GitHub.

## What Already Happened

In Level 1, you created a repo in the class GitHub organization:

```text
Summer-2026-Coding-Club/YOUR-NAME-time-capsule
```

It has a `README.md` file.

In this level, you will work on that same repo from your own computer.

## Before You Start

You need Git installed.

Use the setup guide if needed:

[Git setup guide](./setup-git.md)

Check Git:

```bash
git --version
```

Set your Git name and email if you have not already:

```bash
git config --global user.name "Your Name"
git config --global user.email "YOUR_GITHUB_NOREPLY_EMAIL"
```

GitHub's setup docs are here:

[Set up Git](https://docs.github.com/en/get-started/git-basics/set-up-git)

## Big Ideas

### Clone

To clone a repo means to download a copy to your computer.

Example:

```bash
git clone https://github.com/Summer-2026-Coding-Club/YOUR-NAME-time-capsule.git
```

### Branch

A branch is a separate path of work.

My simple explanation: `main` is the clean version. A branch is where you try a change before deciding if it should go into `main`.

### Fork vs Clone

These two words are easy to mix up.

- **Clone**: Copy a repo from GitHub to your computer.
- **Fork**: Make your own GitHub copy of someone else's repo.

For this demo, you probably need **clone**, not fork.

## Demo: Add a Local Update

You will add a new section to your README from your own computer.

## Step 1: Clone Your Repo

Open a terminal.

Choose a folder where you keep projects, then run:

```bash
git clone https://github.com/Summer-2026-Coding-Club/YOUR-NAME-time-capsule.git
cd YOUR-NAME-time-capsule
```

Replace `YOUR-NAME-time-capsule` with your real repo name.

Check where you are:

```bash
git status
```

If it says something like `On branch main`, you are in the repo.

## Step 2: Make a Branch

Create a branch for your new change:

```bash
git switch -c add-local-update
```

This means: create a new branch named `add-local-update` and switch to it.

## Step 3: Edit the README

Open `README.md` in any text editor.

Now that we have done some real git work, Im going to increase my git confidence. On the first commit of the repo I made in part 1 I wrote:
```md
# Marco's README Time Capsule

Welcome to my Markdown-only project for Summer 2026 Coding Club.

## Snapshot

- Git confidence: 1/10 but improving
- Weather today: Cloudy with some rain
...
```

Inside my text editor im going to change it to

```md
...
- Git confidence: 2/10 and still improving
- Weather today: Sunny and warm!
...
```

## Step 4: Check the Changes

Run:

```bash
git status
```

You should see that `README.md` was modified.

## Step 5: Stage the File

Run:

```bash
git add README.md
```

This means: include this file in my next commit.

## Step 6: Commit the Change

Run:

```bash
git commit -m "add local update"
```

This creates a checkpoint on your branch.

## Step 7: Push the Branch

Run:

```bash
git push -u origin add-local-update
```

This sends your branch to GitHub.

Refresh your repo page on GitHub. You should see your new branch or a message offering to make a pull request.

## Beginner Workflow

Most days, this is the core loop:

```bash
git status
git add README.md
git commit -m "describe the change"
git push
```

If you are adding many files, you may use:

```bash
git add .
```

But beginners should use `git status` first so they know what they are adding.

## Pull and Fetch

If GitHub has changes you do not have locally, run:

```bash
git pull
```

That downloads changes and updates your files.

If you only want to check what changed online without updating your files yet:

```bash
git fetch
```

For beginners, `git pull` is usually the one you will use more.

GitHub explains remote changes here:

[Getting changes from a remote repository](https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository)

## Level 2 Finish Line

You are done when:

- Your repo exists on your computer.
- You made a branch named `add-local-update`.
- You edited `README.md` locally.
- You committed the change.
- You pushed the branch to GitHub.

Next: [Git Level 3](./git-level-3.md)

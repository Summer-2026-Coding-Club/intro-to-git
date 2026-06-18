# Git Level 1: Make Your First Repo

This level is for students who have never used Git or GitHub before.

By the end, you will have a real repo in the class GitHub organization with your own `README.md`.

Class organization:

[Summer-2026-Coding-Club](https://github.com/Summer-2026-Coding-Club)

## Big Ideas

### What is Git?

Git is version control software. That means it tracks changes to files over time.

My simple explanation: Git is like a save system for a coding project. Instead of one save button, it keeps a history of important checkpoints.

The official Git book explains version control here:

[About Version Control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)

### What is GitHub?

GitHub is a website for storing Git projects online.

- **Git** runs on your computer.
- **GitHub** stores and shares your project online.

Git and GitHub are connected, but they are not the same thing.

GitHub's beginner Git docs are here:

[GitHub Git basics](https://docs.github.com/en/get-started/git-basics)

### What is a repository?

A repository, or repo, is a project folder that Git tracks. What you are reading right now is a file inside a repository, specifically a file named `git-level-1.md` in the repo *intro-to-git*

A repo could contain 1 file:

```text
README.md
```

That still counts. A repo does not need to be a giant app.

### What is a commit?

A commit is a saved checkpoint.

Every commit has a message. The message should explain what changed.

Good commit messages:

```text
create time capsule
add app idea
fix spelling in README
```

Bad commit messages:

```text
stuff
asdf
final final
```

### What do push, pull, and fetch mean?

You do not need to use these commands yet, but you should know the words.

- **Push**: Send your local commits up to GitHub.
- **Pull**: Download changes from GitHub and update your local files.
- **Fetch**: Check what changed on GitHub without updating your files yet.

At Level 1, we mostly use the GitHub website. In Level 2, we use these commands on your computer.

## Demo: Create Your README Time Capsule

Your goal is to make a fun Markdown-only repo that other students can browse.

You will create:

```text
NAME-time-capsule
```

## Step 1: Check GitHub Access

1. Go to [GitHub](https://github.com).
2. Sign in or create an account.
3. Open the class org: [Summer-2026-Coding-Club](https://github.com/Summer-2026-Coding-Club).
4. Make sure you can see the organization.

If you cannot see it, ask the instructor to invite you.

Privacy note: GitHub commits can be connected to an email address. If you wish to keep your email address private, GitHub's has a private `noreply` email setting.

## Step 2: Create Your Repo

I made a simple template that you can copy. There is no code and only a `README` file:

1. Open [readme-time-capsule-template](https://github.com/Summer-2026-Coding-Club/readme-time-capsule-template)
2. Click **Use this template**.
3. Choose **Create a new repository**.
4. Owner should be `Summer-2026-Coding-Club`.
5. Name it `NAME-time-capsule`.
6. Make it public unless the instructor says otherwise.
7. Click **Create repository**.

GitHub's official guide is here:

[Creating a repository from a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)

[Creating a new repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)

## Step 3: Edit the README on GitHub

Open `README.md` and click the pencil/edit button.

Add or fill in sections like this:

```md
# Marco's README Time Capsule

Welcome to my Markdown-only project for Summer 2026 Coding Club.

## Snapshot

- Git confidence: 1/10 but improving
- Weather today: Cloudy with some rain
- Something I want to learn: How to do a backflip

## Ridiculous App Idea

Name: FindMyWater

What it does: Reminds you where you left your water bottle.

Why it should exist: I always seem to lose my water bottle.


## Visitor Challenge

If someone visits this repo, they should suggest: A new dish or recipe I can cook at home, Im always looking for new food to try.
```

## Step 4: Commit the Change

At the bottom of the GitHub edit page, GitHub asks for a commit message.

Use:

```text
create time capsule
```

Click **Commit changes**.

You just made a commit.

## Level 1 Finish Line

You are done when:

- Your repo exists in the class org.
- Your `README.md` has your time capsule.
- Your repo has at least one commit.

## Quick Vocabulary

| Word | Simple meaning |
| --- | --- |
| Git | Tracks changes |
| GitHub | Stores repos online |
| Repo | A project folder |
| README | The front page of a repo |
| Commit | A saved checkpoint |
| Push | Send changes to GitHub |
| Pull | Bring GitHub changes down |
| Fetch | Check for GitHub changes |

Next: [Git Level 2](./git-level-2.md)

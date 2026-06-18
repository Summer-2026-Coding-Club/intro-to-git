# Git Level 3: Pull Requests and Diffs

This level is for students who know the basic terms and commands.

You will take the branch from Level 2, open a pull request, inspect the diff, merge it, and sync your local `main` branch.

## What Already Happened

In Level 1, you created:

```text
Summer-2026-Coding-Club/YOUR-NAME-time-capsule
```

In Level 2, you cloned it locally, made a branch called:

```text
add-local-update
```

Then you changed `README.md`, committed it, and pushed the branch to GitHub.

## Big Ideas

### Diff

A diff shows what changed.

Lines added usually show with `+`.

Lines removed usually show with `-`.

The diff is one of the most useful parts of Git. It lets you review the actual change instead of guessing.

### Pull Request

A pull request, or PR, is a request to merge one branch into another.

In normal words:

```text
Here are my changes. Please review them before they become part of main.
```

GitHub explains pull requests here:

[About pull requests](https://docs.github.com/en/pull-requests)

### Merge

To merge means to combine one branch into another.

In this demo, you will merge:

```text
add-local-update -> main
```

## Demo: Open and Merge Your Pull Request

## Step 1: Open Your Repo on GitHub

Go to:

```text
https://github.com/Summer-2026-Coding-Club/YOUR-NAME-time-capsule
```

GitHub may show a button that says **Compare & pull request**.

Click it.

If you do not see that button:

1. Click the **Pull requests** tab.
2. Click **New pull request**.
3. Set base branch to `main`.
4. Set compare branch to `add-local-update`.

GitHub's official guide is here:

[Creating a pull request](https://docs.github.com/articles/creating-a-pull-request)

## Step 2: Write the PR

Use a title like:

```text
Add local update to README
```

Use a short description:

```md
## What changed

- Added a Local Update section to my README.
- Practiced using a branch, commit, and push.

## How to review

Read the README and check that the new section makes sense.
```

Click **Create pull request**.

## Step 3: Inspect the Diff

Open the **Files changed** tab.

Look for:

- What lines were added.
- Whether anything was removed by accident.
- Whether the README still looks appropriate to share.

My take: reviewing the diff is one of the best habits you can build. It is how you catch mistakes before they become part of the main project.

## Step 4: Merge the PR

If the diff looks good:

1. Click **Merge pull request**.
2. Confirm the merge.
3. If GitHub offers to delete the branch, delete it.

The branch was just for the change. Once it is merged, you usually do not need it anymore.

## Step 5: Sync Your Local Main Branch

Go back to your terminal.

Switch to `main`:

```bash
git switch main
```

Pull the merged change:

```bash
git pull
```

Your local `main` now matches GitHub.

If the branch still exists locally, you can delete it:

```bash
git branch -d add-local-update
```

## Optional: Diff Detective

Try this after the main demo.

Create another branch:

```bash
git switch -c add-visitor-challenge
```

Add this to your README:

```md
## Visitor Challenge

Suggest one feature my ridiculous app idea should have.
```

Before committing, run:

```bash
git diff
```

This shows your unstaged changes.

Then commit and push:

```bash
git add README.md
git commit -m "add visitor challenge"
git push -u origin add-visitor-challenge
```

Open another PR and review the diff.

## What About Conflicts?

A conflict happens when Git cannot safely combine changes.

Example: two people edit the same line in different ways.

Git may show something like this inside a file:

```text
<<<<<<< HEAD
Current status: Learning Git locally
=======
Current status: Updating from GitHub
>>>>>>> main
```

This means Git needs a human to choose the final version.

To fix it:

1. Edit the file so only the final text remains.
2. Delete the conflict marker lines.
3. Save the file.
4. Run:

```bash
git add README.md
git commit -m "resolve README conflict"
```

Conflicts look scary at first, but they are just Git saying: "I need help choosing between two changes."

## Best Practices

- Commit small changes.
- Write commit messages that explain what changed.
- Use branches for changes you want to review.
- Read the diff before merging.
- Pull before starting new work.
- Do not commit secrets like passwords or API keys.

## Level 3 Finish Line

You are done when:

- You opened a pull request.
- You inspected the diff.
- You merged the PR into `main`.
- You pulled the merged change back to your computer.
- Your README Time Capsule is visible in the class org.

Browse class repos here:

[Summer-2026-Coding-Club repositories](https://github.com/orgs/Summer-2026-Coding-Club/repositories)

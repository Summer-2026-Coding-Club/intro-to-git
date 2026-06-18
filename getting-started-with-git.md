# Getting Started With Git

This guide is the shortest path to installing Git, checking that it works, making your first commit, pushing it to GitHub, and syncing changes later.

Official links:

- [Git downloads](https://git-scm.com/downloads)
- [GitHub: Set up Git](https://docs.github.com/en/get-started/git-basics/set-up-git)
- [GitHub: Managing remote repositories](https://docs.github.com/en/get-started/git-basics/managing-remote-repositories)
- [GitHub: Pushing commits](https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository)
- [GitHub: Getting changes from a remote repository](https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository)

## 1. Install Git

### Windows

1. Go to [Git for Windows](https://git-scm.com/downloads/win).
2. Download the installer.
3. Run it and keep the default options unless you know you want something different.
4. After installing, open **Git Bash** or **PowerShell**.

### macOS

If you use Homebrew (I highly reccomend homebrew for macOS, learn more [here](https://brew.sh/)):

```bash
brew install git
```

The official macOS install page is here: [Install Git on macOS](https://git-scm.com/downloads/mac).

### Linux

Ubuntu / Debian:

```bash
sudo apt update
sudo apt install git
```

Fedora:

```bash
sudo dnf install git
```

Arch:

```bash
sudo pacman -S git
```

The official Linux install page is here: [Install Git on Linux](https://git-scm.com/downloads/linux).

## 2. Check That Git Installed

Open your terminal and run:

```bash
git --version
```

If Git is installed, you should see something like:

```text
git version 2.54.0
```

The exact number does not need to match. You just need to see a Git version.

## 3. Set Your Name and Email

Git commits store the name and email of the person who made them. Set yours once:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Check that it worked:

```bash
git config --global user.name
git config --global user.email
```

GitHub explains this setup here: [Set up Git](https://docs.github.com/en/get-started/git-basics/set-up-git).

## 4. Create a Local Repo

Make a folder:

```bash
mkdir my-first-repo
cd my-first-repo
```

Start Git:

```bash
git init
```

Set the branch name to `main`:

```bash
git branch -M main
```

Create a file:

```bash
echo "# My First Repo" > README.md
```

Check what Git sees:

```bash
git status
```

Stage the file:

```bash
git add README.md
```

Commit it:

```bash
git commit -m "add README"
```

At this point, you have a Git repo on your computer.

## 5. Create the GitHub Repo

1. Go to [GitHub](https://github.com).
2. Click **New repository**.
3. Give it a name, like `my-first-repo`.
4. Do not add a README on GitHub if you already made one locally.
5. Create the repository.
6. Copy the repository URL. It will look like:

```text
https://github.com/YOUR-USERNAME/my-first-repo.git
```

## 6. Connect Local Git to GitHub

In your terminal, inside your project folder, run:

```bash
git remote add origin https://github.com/YOUR-USERNAME/my-first-repo.git
```

Check that the remote was added:

```bash
git remote -v
```

You should see `origin` and your GitHub URL.

## 7. Push Your Code to GitHub

Push your first commit:

```bash
git push -u origin main
```

You may be asked to sign in to GitHub. Follow the browser login or terminal instructions.

After this first push, future pushes are usually just:

```bash
git push
```

Refresh your GitHub repo page. You should see your `README.md`.

## 8. Make Another Change and Push It

Edit `README.md`, then run:

```bash
git status
git add README.md
git commit -m "update README"
git push
```

That is the basic Git workflow:

```bash
git status
git add .
git commit -m "message"
git push
```

## 9. Sync From GitHub Later

If the GitHub repo has changes that your computer does not have yet, run:

```bash
git pull
```

This downloads the latest changes and updates your local files.

If you only want to check for remote changes without updating your files yet, run:

```bash
git fetch
```

For beginners, `git pull` is usually the command you want.

## 10. Basic Setup Tips

- Commit before making big changes. It gives you a checkpoint.
- Run `git status` often. It tells you what is happening.
- Use clear commit messages, like `fix navbar link` or `add homepage text`.
- Do not commit passwords, API keys, or secret files.
- Add a `.gitignore` file for files Git should ignore.

Example `.gitignore`:

```text
.env
node_modules/
dist/
*.log
```

GitHub explains ignored files here: [Ignoring files](https://docs.github.com/articles/ignoring-files).

## Quick Command List

```bash
git --version                         # Check install
git config --global user.name "Name"  # Set your name
git config --global user.email "you@example.com"

mkdir my-first-repo
cd my-first-repo
git init
git branch -M main

git status
git add .
git commit -m "message"

git remote add origin URL
git remote -v
git push -u origin main

git pull
git push
```

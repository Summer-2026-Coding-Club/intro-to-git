# Setup Git

Use this when you need to install Git or check your setup.

Official install page:

[Git downloads](https://git-scm.com/install/)

## Windows

1. Go to [Git for Windows](https://git-scm.com/downloads/win).
2. Download the installer.
3. Run it and keep the default options unless the instructor says otherwise.
4. Open **Git Bash** or **PowerShell**.

Git Bash is a terminal that comes with Git for Windows. PowerShell also works for the commands in this course.

## macOS

If you use Homebrew:

```bash
brew install git
```

Homebrew is here:

[Homebrew](https://brew.sh/)

If you do not use Homebrew, use the official macOS Git page:

[Install Git on macOS](https://git-scm.com/downloads/mac)

## Linux

Ubuntu or Debian:

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

Official Linux page:

[Install Git on Linux](https://git-scm.com/downloads/linux)

## Check the Install

Run:

```bash
git --version
```

If Git is installed, you should see something like:

```text
git version 2.54.0
```

The number can be different. That is fine.

## Set Your Name and Email

Git commits store the name and email of the person who made them.

For students, do not use a personal email unless the instructor says it is okay. GitHub can give you a private `noreply` email address for commits.

GitHub explains that here:

[Setting your commit email address](https://docs.github.com/en/account-and-profile/how-tos/email-preferences/setting-your-commit-email-address)

Run:

```bash
git config --global user.name "Your Name"
git config --global user.email "YOUR_GITHUB_NOREPLY_EMAIL"
```

Check it:

```bash
git config --global user.name
git config --global user.email
```

GitHub explains this setup here:

[Set up Git](https://docs.github.com/en/get-started/git-basics/set-up-git)

## Login Tip

When you push to GitHub for the first time, GitHub may ask you to sign in.

Follow the browser login or terminal instructions. If it fails, ask the instructor before trying random fixes.

## Quick Check

Before starting Level 2, you should be able to run:

```bash
git --version
git config --global user.name
git config --global user.email
```

If all three commands return something useful, you are ready.

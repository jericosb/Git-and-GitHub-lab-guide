# Week 2: Version Control with Git and GitHub

## Learning outcomes

By the end of this lab you should be able to:

- Explain how the web works (client, server, HTTP)
- Set up Git and GitHub for version control
- Track changes in a project and push them to GitHub

## Part 1: How the web works

A short refresher before the hands-on part.

- **Client**: the browser that requests a page (Chrome, Edge, Firefox).
- **Server**: the computer that stores the website and sends it back.
- **HTTP**: the rules the client and server use to talk to each other.

Flow: you type a URL, the browser (client) sends an HTTP request, the server responds with HTML, CSS, and JavaScript, and the browser displays the page.

## Part 2: Install and check Git

Open a terminal (Git Bash, PowerShell, or Terminal) and check if Git is installed:

```bash
git --version
```

If you see a version number, Git is ready. If not, download it from https://git-scm.com.

## Part 3: One-time setup

Set your name and email. Use the same email as your GitHub account.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@student.tsu.edu.ph"
```

Check your settings:

```bash
git config --list
```

## Part 4: Local workflow

Create a project folder and turn it into a Git repository.

```bash
mkdir my-first-site
cd my-first-site
git init
```

Copy the starter file `index.html` from this lab folder into `my-first-site`, then check the status:

```bash
git status
```

Stage the file, then save the version (commit):

```bash
git add index.html
git commit -m "Add starter page"
```

View the history:

```bash
git log --oneline
```

Now open `index.html`, change the text inside `<h1>`, save, and record the new version:

```bash
git add index.html
git commit -m "Update page heading"
```

Run `git log --oneline` again. You should see two commits.

## Part 5: Push to GitHub

1. Go to https://github.com and create a new **empty** repository named `my-first-site`. Do not add a README on GitHub for now.
2. Connect your local repo to GitHub (replace `your-username`):

```bash
git remote add origin https://github.com/your-username/my-first-site.git
git branch -M main
git push -u origin main
```

3. Refresh the GitHub page. Your files are now online.

## Common commands

| Command | What it does |
|---------|--------------|
| `git status` | Shows changed and staged files |
| `git add <file>` | Stages a file for commit |
| `git commit -m "message"` | Saves a version with a message |
| `git log --oneline` | Shows commit history |
| `git push` | Uploads commits to GitHub |
| `git pull` | Downloads changes from GitHub |
| `git clone <url>` | Copies a GitHub repo to your computer |

## Exercise

1. Create a new repo folder named `about-me`.
2. Add an `index.html` with your name, course, and three things you want to learn this term.
3. Make at least **three** commits with clear messages.
4. Push the repo to GitHub.
5. Submit the GitHub link.

## Checklist before submitting

- [ ] `git config` shows your name and email
- [ ] Repo has at least three commits
- [ ] Repo is visible on GitHub
- [ ] Link submitted

# GIT Essentials 
## Git is a VCS (Version Control System) tool:
  - It is used for versioning your code, which means keeping a history of different versions.
  - It allows developers to work in parallel on different features of the same application code without overwriting each other's projects.
  - Share your work on platforms like GitHub.

  
## Key Concepts
#### *Repository (repo)* - your project's folder 
#### *Commit* - A saved snapshot of your changes, like a checkpoint
#### *Branch* - A parallel version of your project for isolated work
#### *Merge* - combining changes from two branches
#### *Remote* - A copy of your repo hosted online (e.g., GitHub)
#### *Clone* - Downloading a remote repo to your machine

![git_flow_diagram.svg](screenshots/git_flow_diagram.svg)

- Working Directory - where you edit files on your computer. Untracked changes live here.
- Staging Area - a "preparation zone". You choose which files go into your next commit with git add.
- Local Repository - your personal commit history, saved on your machine.
- Remote Repository - the shared copy on GitHub/GitLab. git push uploads; git pull downloads.

## Getting Started

### Part 1 — Setting up Git (one time only)
#### Step 1: Install Git
Download Git from [https://git-scm.com](https://git-scm.com) and install it.
Open your terminal (Mac/Linux) or Git Bash (Windows).

#### Step 2 — Tell Git who you are
Type these two commands (replace with your real name and email, which you need to use further):
``git config --global user.name "Maria Santos" ``
``git config --global user.email "maria@example.com"``

![Git Bash first step](screenshots/GIT_first_step_regist.png)

### Part 2 — Creating your first repository on GitHub
GitHub is the online home for your Git projects. Think of it as Google Drive, but built for code.
#### Step 3 — Create a GitHub account
Go to [https://github.com](https://github.com) and sign up (it's free).

#### Step 4 — Create a new repository

Click the green "New" button on your GitHub homepage
Fill in the form:

- Repository name: my-ds-project
- Description: My first data science project
- ✅ Check "Add a README file"
- ✅ Check "Add .gitignore" → choose Python from the dropdown
- Click "Create repository"

![The GitHub "Create new repository" form filled in](screenshots/new_repo.png)

#### Step 5 — Copy your repository link
On your new repo page, click the green "Code" button and then copy the HTTPS link.

![The green "Code" button open, with the HTTPS link visible](screenshots/copy_https.png)

### Part 3 - Getting the repo onto your computer
#### Step 6 - Clone the repository
*"Cloning"* means downloading a copy of the repo to your computer.
In your terminal, navigate to where you want to save the project (e.g. your Desktop):
bash
``cd Desktop``
``git clone https://github.com/your-username/my-ds-project.git``
``cd my-ds-project``
![Terminal showing the git clone command and its output](screenshots/Cloning_repo.png)
You now have a folder called my-ds-project on your Desktop. Open it and you will see a README.md file already inside!!!

### Part 4 - Saving your work (the daily workflow)
This is what you will do every single day. Learn these 4 commands by heart 
#### Step 7 — Check what has changed
After creating or editing a file (for example, a new notebook eda.ipynb), run in bash:
``git status``

![Terminal showing the git status](screenshots/git_status.png)
- 🔴 Red files = Git sees them but is not tracking them yet
- 🟢 Green files = staged and ready to be committed

#### Step 8 — Stage your files
"Staging" means telling Git: "I want to include this file in my next save."
bash
``git add project.py``
Or to stage all changed files at once:
bash
``git add .``
Run ``git status`` again to confirm:
![Terminal showing the git added files and status](screenshots/git_add_status.png)

#### Step 9 — Commit your changes

A commit is like hitting "Save Game" — it creates a permanent checkpoint.
bash
``git commit -m "Add my first data science project"``

!!! Write your commit message like you are finishing the sentence: "This commit will..."

✅ "Add EDA notebook for sales data"
✅ "Fix null values in preprocessing step"
❌ "stuff" or "update" or "asdfgh"

 ![Terminal showing the git commit](screenshots/git_commit.png)

#### Step 10 — Push to GitHub
"Pushing" uploads your commits to GitHub so your team can see them.
bash
``git push``

 ![Terminal showing successful git push output](screenshots/git_push.png)

Now go to your GitHub repo page and refresh so your file will be there! 

### Part 5 — Working with branches






# Student Guide: Creating a Local Lab Folder and Linking It to GitHub

## Goal

In this exercise, you will:

1. Open your terminal.
2. Navigate to your course folder.
3. Create missing folders if needed.
4. Create a new lab folder using a standard naming convention.
5. Create a matching GitHub repository using the GitHub web interface.
6. Use GitHub’s generated command list to connect your local folder to the remote repository.

---

## Target Course Folder

Your course work should live inside this folder:

```bash
~/Documents/TheoWAF/cpg/cloudfundamentals
```

This means:

```text
Your home folder
└── Documents
    └── TheoWAF
        └── cpg
            └── cloudfundamentals
```

> Note: In most Linux, macOS, and Git Bash environments, `~` means your user home directory.

For example:

```bash
~/Documents
```

usually means something like:

```text
/home/student/Documents
```

or:

```text
/Users/student/Documents
```

or in Git Bash on Windows:

```text
/c/Users/student/Documents
```

---

# Part 1: Open Your Terminal

Use one of the following:

- macOS: Terminal
- Windows: Git Bash
- Linux: Terminal

Confirm your current location:

```bash
pwd
```

## Command Explanation

```bash
pwd
```

means **print working directory**.

It shows the folder you are currently inside.

---

# Part 2: Go to Your Documents Folder

Run:

```bash
cd ~/Documents
```

## Command Explanation

```bash
cd
```

means **change directory**.

This command moves you into another folder.

```bash
~
```

means your home folder.

So this command:

```bash
cd ~/Documents
```

means:

```text
Go to the Documents folder inside my home directory.
```

Confirm that you are in the correct place:

```bash
pwd
```

Expected result should end with:

```text
Documents
```

---

# Part 3: Check Whether the TheoWAF Folder Exists

Run:

```bash
ls
```

## Command Explanation

```bash
ls
```

means **list**.

It shows files and folders in your current location.

Look for a folder named:

```text
TheoWAF
```

---

# Part 4: Create the Course Folder Structure If Needed

If the folder structure does not already exist, run:

```bash
mkdir -p ~/Documents/TheoWAF/cpg/cloudfundamentals
```

## Command Explanation

```bash
mkdir
```

means **make directory**.

It creates a new folder.

```bash
-p
```

means **create parent folders if needed**.

This is useful because it allows one command to create multiple missing folders.

For example, this command:

```bash
mkdir -p ~/Documents/TheoWAF/cpg/cloudfundamentals
```

will create:

```text
TheoWAF
TheoWAF/cpg
TheoWAF/cpg/cloudfundamentals
```

if they do not already exist.

If some of the folders already exist, `mkdir -p` will not fail. It will simply create whatever is missing.

---

# Part 5: Navigate to the Course Folder

Run:

```bash
cd ~/Documents/TheoWAF/cpg/cloudfundamentals
```

Confirm your location:

```bash
pwd
```

Expected result should end with:

```text
Documents/TheoWAF/cpg/cloudfundamentals
```

List the contents:

```bash
ls
```

This folder may be empty if this is your first lab.

---

# Part 6: Choose a Lab Folder Name

Your lab folder should use this naming convention:

```text
<date>_<repo_subject>_lab
```

Use lowercase letters and hyphens or underscores. Avoid spaces.

## Examples

```text
2026-10-08_python_util_lab
2026-10-08_bash_scripting_lab
2026-10-08_linux_practice_lab
2026-10-08_git_intro_lab
2026-10-08_cloudfundamentals_lab
```

Recommended format:

```text
YYYY-MM-DD_subject_lab
```

For example:

```text
2026-10-08_python_util_lab
```

---

# Part 7: Create the New Lab Folder

From inside:

```bash
~/Documents/TheoWAF/cpg/cloudfundamentals
```

run a command like this:

```bash
mkdir 2026-10-08_python_util_lab
```

## Command Explanation

```bash
mkdir 2026-10-08_python_util_lab
```

creates a new folder named:

```text
2026-10-08_python_util_lab
```

You can replace `python_util` with the subject of your lab.

Examples:

```bash
mkdir 2026-10-08_bash_scripting_lab
```

```bash
mkdir 2026-10-08_linux_practice_lab
```

```bash
mkdir 2026-10-08_cloudfundamentals_lab
```

---

# Part 8: Move Into the New Lab Folder

Use `cd` to enter the folder you just created.

Example:

```bash
cd 2026-10-08_python_util_lab
```

Confirm your location:

```bash
pwd
```

Expected result should end with your lab folder name:

```text
2026-10-08_python_util_lab
```

---

# Part 9: Create a Starter File

Create a simple starter file:

```bash
echo "# 2026-10-08_python_util_lab" > README.md
```

## Command Explanation

```bash
echo
```

prints text.

```bash
>
```

redirects the output into a file.

So this command:

```bash
echo "# 2026-10-08_python_util_lab" > README.md
```

creates a file named:

```text
README.md
```

and puts this text inside it:

```markdown
# 2026-10-08_python_util_lab
```

Check that the file exists:

```bash
ls
```

View the file:

```bash
cat README.md
```

## Command Explanation

```bash
cat README.md
```

prints the contents of the file to the terminal.

---

# Part 10: Go to GitHub in the Browser

Open your web browser and go to:

```text
GitHub.com
```

Sign in to your GitHub account.

---

# Part 11: Create a New GitHub Repository

In the GitHub web interface:

1. Click the `+` icon near the top-right corner.
2. Select `New repository`.
3. In the repository name field, enter the exact same name as your local folder.

Example:

```text
2026-10-08_python_util_lab
```

Your GitHub repository name should match your local folder name.

---

# Part 12: Do Not Generate a README

On the new repository page, make sure these options are **not selected**:

```text
Add a README file
Add .gitignore
Choose a license
```

Leave the repository empty.

This is important because GitHub will then show a standard set of commands for connecting your local folder to the remote repository.

If you create a README on GitHub and also create one locally, you may create conflicting repository histories.

---

# Part 13: Create the Empty Repository

Click:

```text
Create repository
```

After the repository is created, GitHub should show a setup page with command options such as:

```text
…or create a new repository on the command line
```

or:

```text
…or push an existing repository from the command line
```

Use the commands GitHub gives you.

---

# Part 14: Initialize Git Locally

From your terminal, make sure you are inside your local lab folder.

Example:

```bash
pwd
```

Expected folder ending:

```text
2026-10-08_python_util_lab
```

Initialize the local Git repository:

```bash
git init
```

## Command Explanation

```bash
git init
```

turns the current folder into a Git repository.

It creates a hidden `.git` folder that stores Git tracking information.

You can check for it with:

```bash
ls -la
```

## Command Explanation

```bash
ls -la
```

means:

```text
-l = long listing format
-a = show all files, including hidden files
```

You should see a hidden folder named:

```text
.git
```

---

# Part 15: Add Your Files to Git

Run:

```bash
git add .
```

## Command Explanation

```bash
git add .
```

stages all files in the current folder.

The dot:

```text
.
```

means:

```text
the current directory
```

So this command means:

```text
Add everything in this folder to the next commit.
```

---

# Part 16: Commit Your Files

Run:

```bash
git commit -m "Initial commit"
```

## Command Explanation

```bash
git commit
```

creates a saved snapshot of your staged files.

```bash
-m
```

adds a commit message.

```bash
"Initial commit"
```

is the message describing this first saved version of your project.

---

# Part 17: Rename the Branch to Main

Run:

```bash
git branch -M main
```

## Command Explanation

```bash
git branch
```

works with Git branches.

```bash
-M main
```

renames the current branch to:

```text
main
```

This is commonly used because GitHub repositories usually use `main` as the default branch name.

---

# Part 18: Link Your Local Folder to GitHub

GitHub will show a command that looks similar to this:

```bash
git remote add origin https://github.com/<your-username>/<repo-name>.git
```

Copy the exact command from your GitHub repository page and run it in your terminal.

Example:

```bash
git remote add origin https://github.com/student-name/2026-10-08_python_util_lab.git
```

## Command Explanation

```bash
git remote add origin
```

adds a remote repository connection named:

```text
origin
```

The URL points to your GitHub repository.

In simple terms:

```text
This connects your local folder to the GitHub repository.
```

---

# Part 19: Push Your Code to GitHub

Run:

```bash
git push -u origin main
```

## Command Explanation

```bash
git push
```

uploads your local commits to GitHub.

```bash
-u
```

sets the upstream connection.

This allows future pushes to use the shorter command:

```bash
git push
```

```bash
origin
```

is the name of your GitHub remote.

```bash
main
```

is the branch you are pushing.

---

# Part 20: Verify on GitHub

Go back to your GitHub repository page.

Refresh the page.

You should now see your local files on GitHub, including:

```text
README.md
```

---

# Full Example Command Sequence

This is an example for a lab named:

```text
2026-10-08_python_util_lab
```

Run:

```bash
cd ~/Documents
mkdir -p ~/Documents/TheoWAF/cpg/cloudfundamentals
cd ~/Documents/TheoWAF/cpg/cloudfundamentals
mkdir 2026-10-08_python_util_lab
cd 2026-10-08_python_util_lab
echo "# 2026-10-08_python_util_lab" > README.md
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<your-username>/2026-10-08_python_util_lab.git
git push -u origin main
```

Replace:

```text
<your-username>
```

with your GitHub username.

---

# Common Mistakes

## Mistake 1: Creating a README on GitHub

If GitHub creates a README and you also create one locally, your local and remote repositories may not match.

For this exercise, do not select:

```text
Add a README file
```

---

## Mistake 2: Creating the GitHub Repo with a Different Name

Your local folder and GitHub repository should match.

Good:

```text
Local folder: 2026-10-08_python_util_lab
GitHub repo: 2026-10-08_python_util_lab
```

Avoid:

```text
Local folder: 2026-10-08_python_util_lab
GitHub repo: python-lab
```

---

## Mistake 3: Running Git Commands in the Wrong Folder

Before running Git commands, always check your location:

```bash
pwd
```

You should be inside your lab folder.

Example:

```text
~/Documents/TheoWAF/cpg/cloudfundamentals/2026-10-08_python_util_lab
```

---

## Mistake 4: Forgetting to Add or Commit Files

If you skip:

```bash
git add .
```

or:

```bash
git commit -m "Initial commit"
```

there may be nothing to push.

Check status with:

```bash
git status
```

## Command Explanation

```bash
git status
```

shows the current state of your Git repository.

It tells you whether files are untracked, staged, committed, or ready to push.

---

# Final Check

At the end, you should have:

```text
A local folder:
~/Documents/TheoWAF/cpg/cloudfundamentals/<date>_<repo_subject>_lab

A matching GitHub repository:
https://github.com/<your-username>/<date>_<repo_subject>_lab

At least one file pushed to GitHub:
README.md
```
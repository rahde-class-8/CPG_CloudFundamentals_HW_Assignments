# CPG Cloud Fundamentals Homework Assignments

## Overview

This repository contains weekly homework assignments for the **CPG Cloud Fundamentals** course.

Students will use this repository to download homework files from a centrally managed source. The instructor will update this repository each week. Students should clone the repository once, then regularly fetch and pull updates to receive new assignments.

---

# Local Folder Location

You should store this homework repository in the following local folder path:

```bash
~/Documents/TheoWAF/cpg/cloudfundamentals/hw/CPG_CloudFundamentals_HW_Assignments
```

The `~` symbol means your home directory.

On macOS, this usually means:

```text
/Users/your-username
```

On Windows Git Bash, this usually means:

```text
/c/Users/your-username
```

So this path:

```bash
~/Documents/TheoWAF/cpg/cloudfundamentals/hw
```

means:

```text
Your home folder → Documents → TheoWAF → cpg → cloudfundamentals → hw
```

---

# First-Time Setup

## Step 1: Open Your Terminal

Use one of the following:

- macOS: Terminal
- Windows: Git Bash

---

## Step 2: Confirm Your Current Location

Run:

```bash
pwd
```

This shows the folder you are currently inside.

---

## Step 3: Create the Parent Homework Folder

Run:

```bash
mkdir -p ~/Documents/TheoWAF/cpg/cloudfundamentals/hw
```

This creates the required parent folder structure if it does not already exist.

The `-p` option tells the terminal to create any missing parent folders along the way.

---

## Step 4: Navigate Into the Homework Parent Folder

Run:

```bash
cd ~/Documents/TheoWAF/cpg/cloudfundamentals/hw
```

Confirm your location:

```bash
pwd
```

Your output should end with:

```text
Documents/TheoWAF/cpg/cloudfundamentals/hw
```

---

## Step 5: Clone the Homework Repository

Your instructor will provide the repository URL.

It will look similar to this:

```text
https://github.com/organization-name/CPG_CloudFundamentals_HW_Assignments.git
```

Clone the repository by running:

```bash
git clone <REPOSITORY_URL> CPG_CloudFundamentals_HW_Assignments
```

Replace `<REPOSITORY_URL>` with the actual URL provided by your instructor.

Example:

```bash
git clone https://github.com/organization-name/CPG_CloudFundamentals_HW_Assignments.git CPG_CloudFundamentals_HW_Assignments
```

This command downloads the homework repository and creates this local folder:

```bash
~/Documents/TheoWAF/cpg/cloudfundamentals/hw/CPG_CloudFundamentals_HW_Assignments
```

---

## Step 6: Navigate Into the Homework Repository

Run:

```bash
cd CPG_CloudFundamentals_HW_Assignments
```

Confirm that you are inside the repository:

```bash
pwd
```

Your output should end with:

```text
CPG_CloudFundamentals_HW_Assignments
```

List the files:

```bash
ls
```

You should see the homework repository contents.

---

# Weekly Homework Update Instructions

Each week, your instructor may add new homework files to this repository.

To get the latest homework, open Terminal or Git Bash and navigate into your local homework repository:

```bash
cd ~/Documents/TheoWAF/cpg/cloudfundamentals/hw/CPG_CloudFundamentals_HW_Assignments
```

Then run:

```bash
git fetch origin
```

This checks GitHub for new updates from the instructor.

Then run:

```bash
git pull --ff-only origin main
```

This downloads the latest files and updates your local copy.

---

# Weekly Update Command Summary

Use these commands each week:

```bash
cd ~/Documents/TheoWAF/cpg/cloudfundamentals/hw/CPG_CloudFundamentals_HW_Assignments
git fetch origin
git pull --ff-only origin main
```

---

# Important Notes

## Do Not Rename the Repository Folder

Keep the folder name as:

```text
CPG_CloudFundamentals_HW_Assignments
```

This helps keep everyone’s local setup consistent.

---

## Do Not Delete the `.git` Folder

This repository contains a hidden `.git` folder that tracks the connection to GitHub.

You can see hidden files with:

```bash
ls -la
```

Do not delete `.git`.

If you delete it, your local folder will no longer behave like a Git repository.

---

## Do Not Edit Instructor Assignment Files Unless Directed

This repository is meant to receive homework assignments from the instructor.

If your instructor asks you to complete assignments in a separate folder or submit your work elsewhere, follow those instructions carefully.

---

# If You Already Cloned the Repository

If the repository already exists on your machine, do not clone it again.

Instead, navigate into the existing folder:

```bash
cd ~/Documents/TheoWAF/cpg/cloudfundamentals/hw/CPG_CloudFundamentals_HW_Assignments
```

Then update it:

```bash
git fetch origin
git pull --ff-only origin main
```

---

# If the Folder Already Exists but Is Not a Git Repository

If you run:

```bash
git status
```

and see an error like:

```text
fatal: not a git repository
```

then you are either:

1. In the wrong folder, or
2. Inside a folder that was not cloned from GitHub.

First, check your location:

```bash
pwd
```

Then list the files:

```bash
ls -la
```

A real Git repository should contain a hidden folder named:

```text
.git
```

If `.git` is missing, ask your instructor before deleting or replacing the folder.

---

# Basic Linux Command Reference

## `pwd`

```bash
pwd
```

`pwd` means **print working directory**.

It shows your current folder location.

Example output:

```text
/Users/student/Documents/TheoWAF/cpg/cloudfundamentals/hw
```

---

## `cd`

```bash
cd folder-name
```

`cd` means **change directory**.

It moves you into another folder.

Example:

```bash
cd ~/Documents
```

This moves you into your `Documents` folder.

---

## `ls`

```bash
ls
```

`ls` means **list**.

It shows the files and folders in your current location.

Example:

```bash
ls
```

You might see:

```text
TheoWAF
```

You can also run:

```bash
ls -la
```

This shows a detailed list, including hidden files such as `.git`.

---

## `mkdir`

```bash
mkdir folder-name
```

`mkdir` means **make directory**.

It creates a new folder.

Example:

```bash
mkdir hw
```

This creates a folder named `hw`.

You can also use:

```bash
mkdir -p ~/Documents/TheoWAF/cpg/cloudfundamentals/hw
```

The `-p` option creates missing parent folders as needed.

---

## `touch`

```bash
touch filename
```

`touch` creates an empty file if the file does not already exist.

Example:

```bash
touch notes.txt
```

This creates a file named:

```text
notes.txt
```

If the file already exists, `touch` updates its timestamp.

---

# Final Check

At the end of setup, you should be able to run:

```bash
cd ~/Documents/TheoWAF/cpg/cloudfundamentals/hw/CPG_CloudFundamentals_HW_Assignments
pwd
ls
git status
```

You should be inside the homework repository and ready to receive weekly assignments.

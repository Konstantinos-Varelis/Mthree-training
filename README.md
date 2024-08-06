# Mthree SRE Training Repository

Welcome to my training repository for the Site Reliability Engineer (SRE) position with Mthree. This repository contains all the projects, exercises, and notes from my training program.

## Table of Contents

- [Introduction](#introduction)
- [Course Overview](#course-overview)
- [Activities](#activities)
  - [Set up a Personal GitHub Repository](#activity-set-up-a-personal-github-repository)
  - [Create a GitHub Personal Access Token](#activity-create-a-github-personal-access-token)
  - [AWS EC2 Setup](#activity-aws-ec2-setup)
  - [Linux Exercises: Basic Commands](#activity-linux-exercises-basic-commands)
  - [Linux Tools & Navigation](#activity-linux-tools--navigation)
  - [File Management & Git](#activity-file-management--git)
  - [Editing Files in Linux](#activity-editing-files-in-linux)
  - [Fix Log Analysis](#activity-fix-log-analysis)
  - [File Systems in Linux](#activity-file-systems-in-linux)
  - [Linux Jobs](#activity-linux-jobs)
  - [Scheduling and Automation](#activity-scheduling-and-automation)
  - [Using Vi](#activity-using-vi)
- [Exercises](#exercises)
- [Notes](#notes)
- [Resources](#resources)

## Introduction

This repository documents my journey through the Mthree training program to become a Site Reliability Engineer. It includes various projects and exercises that demonstrate the skills and knowledge I have acquired during the training.

## Course Overview

The training program covers a wide range of topics essential for an SRE, including but not limited to:

1. Basic Concepts and Terminology
2. Git Basics
3. Linux Fundamentals
4. Basic Tools and Navigation
5. Monitoring

## Activities

### Activity: Set up a Personal GitHub Repository

**Description:** 
This activity involves [creating a personal GitHub repository](https://docs.github.com/en/get-started/quickstart/create-a-repo) to store and manage your code and projects. Setting up a GitHub repository is a fundamental step for version control and collaboration in software development. This activity covers the steps to create a repository, initialize it with a README file, and make the first commit.

**Key Features:**
- [Creation of a new GitHub repository](https://docs.github.com/en/get-started/quickstart/create-a-repo).
- Initialization of the repository with a README file.
- Making the first commit to the repository.
- Basic understanding of version control using Git and GitHub.

**Files:** 
- [README.md](README.md) (this file)


### Activity: Create a GitHub Personal Access Token

**Description:**
This activity involves creating a GitHub Personal Access Token (PAT) to securely authenticate and authorize access to your GitHub account when performing operations from the command line or other tools. This is crucial for tasks that require elevated permissions, such as pushing changes to repositories or accessing private repositories. Detailed steps can be found in the [GitHub documentation](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token).

**Key Features:**
- [Generating a personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token).
- Configuring the token for use in command-line operations.
- Understanding the scope and permissions associated with the token.

**Files:**
- No specific files for this activity.


### Activity: AWS EC2 Setup

**Description:**
This activity involves setting up an AWS EC2 instance, which is a virtual server in Amazon's Elastic Compute Cloud (EC2) for running applications on the AWS infrastructure. This includes steps to launch, configure, and connect to an EC2 instance. Detailed instructions can be found in the [AWS EC2 documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html).

**Key Features:**
- [Launching an EC2 instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html).
- Configuring security groups and key pairs.
- Connecting to the instance using SSH.
- Basic management and monitoring of the instance.

**Files:**
- No specific files for this activity.


### Activity: Linux Exercises: Basic Commands

**Description:**
This activity covers fundamental Linux commands essential for navigating and managing a Linux environment. These commands form the basis of everyday operations in Linux, such as file management, system navigation, and basic system information retrieval. Detailed explanations and examples can be found in the [Linux Command Line documentation](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview).

Complete the following activities using a Linux interface, using skills covered in Linux Lesson 2:

1. Run a command to find your current location on the server.
2. Change directory from your current location to /var/log.
3. Go back up a directory.
4. Find your current location again.
5. List all the files in the current directory.
6. Now list all the files with the long listing.
7. Now list all the files with the long listing in reverse order, with the newest appearing at the bottom of your screen.
8. Change to root directory.
9. Change back to your home directory.
10. Go up a level in directory structure.
11. Find out more information about the ls command.
12. Go back to /var.
13. Show the contents of this directory with details reverse sorted by size (you may have to use `man` to help).
14. Find out the hardware version you are running.

**Key Features:**
- [Basic navigation commands](https://ubuntu.com/tutorials/command-line-for-beginners#2-navigating-the-command-line) (e.g., `cd`, `ls`).
- File manipulation commands (e.g., `cp`, `mv`, `rm`).
- Viewing file contents (e.g., `cat`, `less`, `head`, `tail`).
- Basic system information commands (e.g., `uname`, `top`, `df`).

**Files:**
- [Activity - Linux Exercises - Basic Commands](Activities/Activity%20-%20Linux%20Exercises%20-%20Basic%20Commands.docx)


### Activity: Linux Tools & Navigation

**Description:**
This activity involves practising basic navigation commands in a Linux system. It includes tasks such as checking the current version of Linux, navigating through the file system, and using commands to list files and view command history. Detailed explanations and examples can be found in the [Linux Tools documentation](https://linux.die.net/man/).

Complete the following activities using a Linux interface:

1. Check the current version of Linux:
    ```bash
    uname -a
    ```
2. Check your current location in the file structure:
    ```bash
    pwd
    ```
3. Move up one folder:
    ```bash
    cd ..
    ```
4. Check your location again:
    ```bash
    pwd
    ```
5. List all the files with details. Try both of these commands to see how they are different:
    ```bash
    ls -l
    ls -ltr
    ```
6. Change the directory to the root folder:
    ```bash
    cd /
    ```
7. Check your location again:
    ```bash
    pwd
    ```
8. List all files in the current directory, sorted with the most recently-changed file at the bottom of the screen:
    ```bash
    ls -ltr
    ```
9. Change back to your home directory:
    ```bash
    cd ~
    ```
10. List all files, including the hidden files:
    ```bash
    ls -ltra
    ```
11. Run the history command:
    ```bash
    history
    ```

**Key Features:**
- Practising basic Linux navigation commands.
- Understanding how to list and manage files.
- Using commands to view system information and command history.

**Files:**
- [Activity - Linux Tools & Navigation](Activities/Activity%20-%20Linux%20Tools%20&%20Navigation.md)

### Activity: File Management & Git

**Description:**
This activity focuses on managing files and directories in a Linux environment along with basic Git operations. It includes tasks such as creating, moving, and deleting files and directories, as well as initializing a Git repository, committing changes, and pushing to a remote repository. Detailed explanations and examples can be found in the [Linux File Management documentation](https://www.guru99.com/linux-file-directory-management.html) and [Git documentation](https://git-scm.com/doc).

#### Part A: Managing Files and Folders

1. Create a folder in your home directory using your name as the name of the folder:
    ```bash
    mkdir <yourname>
    ```

2. Move into the folder:
    ```bash
    cd <yourname>
    ```

3. Create an empty file:
    ```bash
    touch test.txt
    ```

4. Create a new folder in this folder called `myfolder`:
    ```bash
    mkdir myfolder
    ```

5. Move the empty file you created into `myfolder`:
    ```bash
    mv test.txt myfolder
    ```

6. Create a backup of the file:
    ```bash
    cp myfolder/test.txt myfolder/test.bkp
    ```

7. Remove the backup file:
    ```bash
    rm myfolder/test.bkp
    ```

8. Go back to your home directory:
    ```bash
    cd ~
    ```

#### Part B: Working with Git

1. Clone the repository:
    ```bash
    git clone https://github.com/TheSoftwareGuild/git-collection-display.git
    ```

2. Go to the newly created `git-collection-display` directory:
    ```bash
    cd git-collection-display
    ```

3. Navigate to the folder `collection/_data/sets`:
    ```bash
    cd collection/_data/sets
    ```

#### Searching Files

1. Display the contents of the file `comic_comfort_services.txt`:
    ```bash
    cat comic_comfort_services.txt
    ```

2. Display the first line of the file:
    ```bash
    head -n 1 comic_comfort_services.txt
    ```

3. Display the first three lines of the file:
    ```bash
    head -n 3 comic_comfort_services.txt
    ```

4. Display how many times the word GOOD is used:
    ```bash
    grep -c GOOD comic_comfort_services.txt
    ```

5. Display how many times the word BAD is used:
    ```bash
    grep -c BAD comic_comfort_services.txt
    ```

6. List the files that contain the word SPY in any case:
    ```bash
    grep -i SPY *
    ```

7. List the files that do not contain the word SPY:
    ```bash
    grep -L SPY *
    ```

8. Find files that contain the word “data” in their name:
    ```bash
    find . -name "*data*"
    ```

9. Change permissions on the file `comic_comfort_services.txt` to allow read and write for the user, and read-only for group and others:
    ```bash
    chmod 644 comic_comfort_services.txt
    ```

10. List all the access control permissions for the file:
    ```bash
    ls -l comic_comfort_services.txt
    ```

11. Locate and remove write permission for all users on the file named `SPYGRD.tab`:
    ```bash
    chmod a-w SPYGRD.tab
    ```

**Key Features:**
- Creating, moving, and deleting files and directories using `touch`, `mv`, and `rm`.
- Initializing a Git repository with `git init`.
- Adding files to the staging area with `git add`.
- Committing changes with `git commit`.
- Pushing changes to a remote repository with `git push`.

**Files:**
- [Activity - File Management & Git](Activities/Activity%20-%20File%20Management%20&%20Git.md)

### Activity: Editing Files in Linux

**Description:** 

**Key Features:**

**Files:**

### Activity: Fix Log Analysis

**Description:** 

**Key Features:**

**Files:**

### Activity: File Systems in Linux

**Description:** 

**Key Features:**

**Files:**

### Activity: Linux Jobs

**Description:** 

**Key Features:**

**Files:**

### Activity: Scheduling and Automation

**Description:** 

**Key Features:**

**Files:**

### Activity: Using Vi

**Description:** 

**Key Features:**

**Files:**

## Exercises

This section contains various exercises that I completed during the training. Each exercise is designed to reinforce the concepts learned in the lectures.

**Files:**

## Notes

Personal notes and summaries of important concepts covered during the training.

**Files:**

## Resources

A list of additional resources that were helpful throughout the training program.



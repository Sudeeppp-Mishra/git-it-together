# Git Getting Started

---

## Get Started with Git

Now that Git is installed, and it knows who you are, you can start using Git.

Lets create our first repo.

## Key Steps to Get Started

- Create a project folder
- Navigate to the folder
- Initialize a Git repository

---

## Creating Git Folder

Start by creating a new folder for our project:

> Example
>
> ```sh
> mkdir myproject
>
>```
>
Then go to that project folder by typing:
>Exmaple:
>
>```sh
>cd myproject
>```

`mkdir` creates a new directory. <br>
`cd` changes our working directory

Now we are in the correct directory and can intialize Git!

---

## Initialize Git

Now that we are in the correct folder, we can initialize Git on that folder:

>Example:
>
>```sh
> git init
>```
>
You just created your first Git Repository!

---

## What is a Repository?

A Git **repository** is a folder that Git tracks for changes.

The repository stores all your project's history and versions.

---

## What Happens When You Run `git init`?

Git creates a hidden folder called `.git` inside your project.

This  is where Git stores all the information it needs to track your files and history.

> Example: Show Hidden .git Folder (Linux/macOS)
>
> ```sh
> ls -a
>```
>
o/p:
>
>```sh
> . .. .git
>```
>
On Windows, you may need to enable "Show hidden files" in File Explorer to see the `.git` folder.

---

## Troubleshooting

- **git: command not found**<br>
_Solution_: Make sure Git is installed and added to your PATH. Restart your terminal if needed.
- **Permission denied**<br>
_Solution_: Try running your terminal as administrator (Windows) or use `sudo` (macOS/Linux) if needed.

# Git New Files
---
## What is a New File?

A **new file** is a file that you have created or copied into your project folder, but haven't told Git to watch.

Here are the key things to know:

- Create a new file (with a text editor)
- `ls` - List files in the folder
- `git status` - Check which files are tracked
- Understand **untracked** and **tracked** files

---

## Create a New File

Your new Git repository is empty.

Let's add a file using your fav. text editor, and save it in your project folder.

Eg:
> ```html
> <!DOCTYPE html>
> <html>
> <head>
> <title>Hello World!</title>
> </head>
> <body>
> 
> <h1>Hello world!</h1>
> <p>This is the first file in my new Git Repo.</p>
> 
> </body>
> </html>
> ```

Save this as `index.html` in your project folder.

---

---

## List Files in the Directory - `ls`

---

## Check File Status with `git status`

Now check if Git is tracking your new file:

you will get o/p like:

> `git status` <br>
> On branch master <br><br>
> No commits yet<br><br>
> Untracked files:<br>
> (use "git add ..." to include in what will be committed index.html<br><br>
> nothing added to commit but untracked files present (use "git add" to track)

Git sees `index.html`, but it is **untracked** (not yet added to the repository).

---

## What is an Untracked File?

An **untracked file** is any file in your project folder that Git is not yet tracking.

These are files you've created or copied into the folder, but haven't told Git to watch.

---

## What is a Tracked File?

A **tracked file** is a file that git is watching for changes.

To make a file tracked, you need to add it to the staging area...(about staging we will learn next)

---

## Troubleshooting

- **File not showing up with** `ls`: Make sure you saved it in the correct folder. Use `pwd` to check your current directory.
- **File not listed in** `git status`: Make sure you are in the corerect folder and that you saved the file.
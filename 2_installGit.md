# Git Install
---
## How to install Git?

We can download Git for free from [git-scm.com](git-scm.com).

<br>

- **Windows**: Download and run the installer. It will install Git and Git Bash.
- **macOS**: If you use Homebrew, open Terminal and type :
```zsh
brew install git
```
Or, download the .dmg file and drag Git to your Applications folder.

- **Linux**: Open your terminal and use your package manage. Eg: on Ubuntu: 
```zsh
sudo apt-get install git
```
After intallation, we can use Git from our terminal or command prompt.

---

## Git Bash

Git Bash is a terminal for Windows that lets you use Git commands.

You can use Git Bash just like the command prompt, but with extra Unix commands (like ls and pwd).

---

## Verifying Your Installation

In terminal type:
```bash
git --version
```
If Git is installed, you will see something like _git version X.Y.Z_

If you see an error, try closing and reopening your terminal, or check that Git is in your PATH.

---
## Default Editor

During installation, Git asks you to pick a default text editor.

This is the program that will open when you need to write messages (like for commits).

> Example: Set VS Code as Default Editor
> ```bash
> git config --global core.editor "code --wait"
>```

If you are not sure, just pick the default (Notepad on Windows). You can always change this later.

>Example: Set Notepad as Default Editor
> ```bash
> git config --global core.editor "notepad"
>```

---

## PATH Environment
Choosing to add Git to your PATH means you can use Git commands in any terminal window.

This is highly recommended for most users to do this during installation.

## How to Add Git to PATH after installation

- **Windows**:
    1. If you missed the option during installation, search for "Environment Variables" in the Start menu and open it.
    2. Click "Environment Variables..." and find the "Path" variable under "System variables".
    3. Click "Edit", then "New", and add the path to your Git `bin` and `cmd` folders <br>
    (e.g., `C:\Program Files\Git\bin` and `C:\Program Files\Git\cmd`).
    4.  Click OK to save. Restart your terminal.

- **macOS**:
    1. If you installed with Homebrew, your PATH is usually set automatically.
    2. If not, open Terminal and add this line to your `~/.zshrc` or `~/.bash_profile`:
    ```bash
    export PATH = "/usr/loal/bin:$PATH"
    ```
    3. Save the file and run `source ~/.zshrc` or `source ~/.bash_profile`.

- **Linux**:
    1. Most package managers add Git to PATH automatically.
    2. If not, add this line to your ~/.bashrc or ~/.profile:
    ```bash
    export PATH = "/usr/bin:$PATH"
    ```
    3. Save the file and run `source ~/.bashrc` or `source ~/.profile`.

After adding Git to your PATH, open a new terminal window and run `git --version` to check that it works everywhere.

---

## Line Endings

Git can convert line endings in text files.

On Windows, it's usually best to select "Checkout Windows-style, commit Unix-style line endings".

This helps prevent problemsn when you share code with people using different OSs.

---

## Updating or Uninstalling Git

- **Update**: Download and run the latest installer, or use your package manager<br>(e.g., `brew upgrade git` or `sudo apt-get upgrade git`)
It's good idea to keep Git up to date for the latest features and security fixes.
- **Uninstall**: Use "Add or Remove Programs" on Windows, or your package manager on Mac/Linux.

---

## Troubleshooting Git Installation

If you run into problems installing or running Git, don't worry!

Here are solutions to some of the most common issues.

> **Tip**: If something doesn't work right away, try closing and reopening your terminal, or restarting your computer.

### Common Installation Issues

- **"git is not recognized as an internal or external command"**<br>
*Solution:* Git is not in your system's PATH. Make sure you installed Git and restart your terminal.
If needed, add Git's bin folder (usually C:\Program Files\Git\bin) to your PATH.
If it still doesn't work, try restarting your computer.

- **Permission errors ("Permission denied")**<br>
*Solution:* On Windows, run Git Bash or your terminal as administrator.
On macOS/Linux, use sudo if necessary.

- **SSL or HTTPS errors when cloning/pushing**<br>
*Solution:* Check your internet connection.
Make sure your Git version is up to date.

- **Wrong version of Git**<br>
*Solution:* Check your installed version with git --version.
Download the latest version from git-scm.com if needed.
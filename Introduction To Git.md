
---
# Getting Started With Git
---
## What is Git

1. Git is something that is created as a version control system
2. The founder of git is Linus Torvalds who is the founder of Linus operating system
3. Git was introduced as a method to manage the several versions of Linux operating system in a good and structured manner

## What is GitHub

1. GitHub provides a Nice and better UI for managing our GitHub repositories
2. Git is out system GitHub just makes it looks good an good to showcase

# Creating our First Repository

1. Go to [GitHub](https://github.com) official website and create your account and login if you already have an account
2. ![[Pasted image 20250720002849.png]]
3. Choose a name for your repository 
4. Make it public / private as your choice
5. But please tick the README file this will create a README file in your repo creating and empty repo is not promoted by me
6. After creating it you will be redirected to your very own repository
7. Now just copy the Repo Link from the Code Tap 
   ![[Pasted image 20250720003359.png]]
8. Now lets leave GitHub and setup Git

## Setting Up Git

1. For windows go to the [Git](https://git-scm.com/downloads) website and download the Git Package
2. For Linux users this is not needed as your system is already loaded with Git
3. Ok, this will install Git on your system We can use this to access my GitHub repo

## Using Git With GitHub

Now that we have Git installed and our GitHub repository created, let's learn the essential Git commands to work with our repository:

### 1. Git Clone
First, we need to clone our repository to our local machine:

```bash
git clone <repository-url>
```

Replace `<repository-url>` with the URL you copied from GitHub. For example:
```bash
git clone https://github.com/yourusername/your-repo-name.git
```

This will create a local copy of your repository on your computer.
From there you can make changes to your repository and We need to Commit it to our repo

### 2. Git Add
When you make changes to files in your repository, you need to stage them before committing:

```bash
# Add a specific file
git add filename.txt

# Add all files in the current directory
git add .

# Add all files in the entire repository
git add -A
```

use git add . for now
### 3. Git Commit
After staging your changes, you need to commit them with a descriptive message:

```bash
git commit -m "Your commit message here"
```

Good commit messages are descriptive and explain what changes were made. For example:
- `git commit -m "Add README file"`
- `git commit -m "Fix bug in login function"`
- `git commit -m "Update documentation"`

### 4. Git Push
Finally, push your committed changes to GitHub:

```bash
# Push to the main branch
git push origin main

# Or if you're using the master branch
git push origin master
```

### Complete Workflow Example

Here's how you would typically use these commands together:

```bash
# 1. Clone the repository (only needed once)
git clone https://github.com/yourusername/your-repo-name.git

# 2. Navigate to the repository folder
cd your-repo-name

# 3. Make changes to your files
# (edit files using your preferred editor)

# 4. Stage your changes
git add .

# 5. Commit your changes
git commit -m "Add new feature"

# 6. Push to GitHub
git push origin main
```

### Important Notes:
- Always use meaningful commit messages
- Use `git status` to check the current state of your repository
- Use `git log` to view commit history
- Make sure you're in the correct directory when running Git commands
---
##  Using Visual Studio Code for Git (Easier Alternative)
---
If the command line seems too complex, Visual Studio Code provides a much easier way to work with Git through its built-in Source Control features.

### Setting Up VS Code for Git

1. **Install Visual Studio Code** from [code.visualstudio.com](https://code.visualstudio.com)
2. **Open your repository folder** in VS Code:
   - File → Open Folder → Select your cloned repository folder
   - Or drag and drop your repository folder into VS Code

### Using VS Code Source Control

#### 1. Viewing Changes
- Click on the **Source Control icon** in the left sidebar (looks like a branch/fork)
- You'll see all your modified files listed under "Changes"
- Click on any file to see a side-by-side diff view

#### 2. Staging Changes (Git Add)
- In the Source Control panel, you'll see a **"+"** icon next to each modified file
- Click the **"+"** to stage individual files
- Or click the **"+"** next to "Changes" to stage all files at once
- This is equivalent to `git add .`

#### 3. Committing Changes (Git Commit)
- After staging, type your commit message in the text box at the top of the Source Control panel
- Click the **"✓"** (checkmark) button to commit
- This is equivalent to `git commit -m "your message"`

#### 4. Pushing to GitHub (Git Push)
- After committing, click the **"..."** (three dots) menu in the Source Control panel
- Select **"Push"** to upload your changes to GitHub
- This is equivalent to `git push origin main`

### VS Code Git Workflow Example

1. **Make changes** to your files in VS Code
2. **Open Source Control** (Ctrl+Shift+G)
3. **Stage changes** by clicking the "+" next to files
4. **Write commit message** in the text box
5. **Click the checkmark** to commit
6. **Click "..." → Push** to upload to GitHub

### Benefits of Using VS Code

- **Visual diff view** - See exactly what changed
- **No command line needed** - Everything is point-and-click
- **Built-in terminal** - Still available if you need it
- **Git integration** - Seamless workflow
- **Extensions** - Many Git-related extensions available

### Quick Tips

- Use **Ctrl+Shift+G** to quickly open Source Control
- The **status bar** at the bottom shows your current branch
- **Hover over files** to see what changes were made
- Use **Ctrl+Enter** to commit after typing your message

---

## Using GitHub Desktop Is Also a Good Idea

If you prefer a simple, graphical interface for working with Git and GitHub, **GitHub Desktop** is a great choice. It’s free, easy to use, and works on both Windows and Mac.

### Setting Up GitHub Desktop

1. **Download and install** GitHub Desktop from [desktop.github.com](https://desktop.github.com)
2. For linux
```bash

wget -qO - https://apt.packages.shiftkey.dev/gpg.key | gpg --dearmor | sudo tee /usr/share/keyrings/shiftkey-packages.gpg > /dev/null

sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/shiftkey-packages.gpg] https://apt.packages.shiftkey.dev/ubuntu/ any main" > /etc/apt/sources.list.d/shiftkey-packages.list'


sudo apt update && sudo apt install github-desktop
```
3. **Sign in** with your GitHub account when prompted.
4. **Clone your repository**:
   - Click **File → Clone repository**
   - Paste your repository URL or select it from the list
   - Choose a local path and click **Clone**

### Basic Workflow in GitHub Desktop

1. **Make changes** to your files using your favorite editor (e.g., VS Code, Notepad, etc.)
2. **View changes** in GitHub Desktop:
   - Open GitHub Desktop and select your repository
   - The **Changes** tab will show all modified files
   - Click on a file to see what changed
3. **Stage and commit** your changes:
   - Enter a summary (commit message) in the bottom-left box
   - Optionally, add a description
   - Click **Commit to main** (or your branch name)
4. **Push your changes** to GitHub:
   - Click **Push origin** (top bar) to upload your commits to GitHub

### Benefits of GitHub Desktop

- **No command line required** – everything is point-and-click
- **Visual diff** – see exactly what changed in each file
- **Easy branch management** – create, switch, and merge branches with a click
- **Simple conflict resolution** – built-in tools to help resolve merge conflicts
- **Works with any editor** – open files in VS Code, Atom, Notepad, etc.

### Quick Tips

- Use **Repository → Open in Terminal** if you ever want to use the command line
- Use **Repository → Open in Visual Studio Code** to quickly open your project in VS Code
- The **History** tab shows all past commits and changes
---
### You can Contact Me with Any Queries or doubts regarding using The GitHub or Git or any further information You need

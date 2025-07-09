Git is a "version control system" that helps you track changes to your files. Think of it like a save game feature for your projects!

## 1. Set Up Git (First Time Only!)
You only need to do this once on your computer.
- **Your Name:**
```
git config --global user.name "Your Name"
```
*(Replace "Your Name" with your actual name)*
- **Your Email:**
```
git config --global user.email "your.email@example.com"
```
*(Replace with your email)*
## 2. Start a Git Project (Initialize)
Go to your project folder in your computer's terminal (like Command Prompt on Windows or Terminal on Mac/Linux) and run:
```
git init
```
*This creates a hidden `.git` folder that Git uses to track changes.*
## 3. Basic Workflow: Stage, Commit, Push
This is the most common cycle you'll use.
- `git status` **(Check Your Work)**
	- Shows you what files have changed.
	- Helps you see what's "staged" (ready to be saved) and "unstaged."
```
git status
```
- `git add .` **(Stage Changes)**
	- "Stages" all your changes, meaning you're telling Git: "I want to save these files in my next commit."
	- The `.` means "all files in the current directory."
```
git add .
```
**Tip:** You can also `git add filename.md` to stage just one file.
- `git commit -m "Your Commit Message"` (Save Changes)
	- This is like taking a snapshot of your project at this moment.
	- The `-m` means "message." Your message should describe _what_ you changed
	- **Good Commit Message Example:** `git commit -m "Add initial project setup"` or `git commit -m "Fix typo in introduction"`
```
git commit -m "Your concise message here"
```
- `git push` (Send to GitHub)
	- If you're using GitHub (which we'll cover next), this command sends your saved changes from your computer to your GitHub project online.
	- You'll typically only need to set up where to push to the very first time with `git push -u origin main` (or `master`), then just `git push` after that.
```
git push
```
## 4. Get Latest Changes (Pull)
- `git pull` (Download from GitHub)
	- If others are working on the same project (or you're working from another computer), `git pull` downloads the latest changes from GitHub to your computer.
```
git pull
```
## 5. Essential Commands Summary
- `git init` - Start a new Git project in a folder.
- `git status` - See what files are changed/staged.
- `git add .` - Stage all changes (prepare them for commit).
- `git commit -m "message"` - Save the staged changes with a message.
- `git push` - Send your local commits to GitHub.
- `git pull` - Get the latest changes from GitHub.
### Using GitHub Desktop
If you prefer a visual way to use Git, GitHub Desktop is great!
1. **Open GitHub Desktop:** Open the application.
2. **Add a Repository:**
	- **Clone a Repository:** If your project is already on GitHub, choose "Clone a Repository" and select it from your GitHub account.
	- **Add an Existing Repository:** If you have a project folder on your computer that you initialized with `git init`, choose "Add an Existing Repository" and point it to that folder.
	- **Create a New Repository:** To start fresh, choose "Create a New Repository."
3. **Making Changes:**
	- As you change files in your project folder, GitHub Desktop will automatically show you these changes in its "Changes" tab.
	- **Stage/Select Changes:** Check the boxes next to the files you want to include in your commit.
	- **Commit:** Write a clear "Summary" (your commit message) and an optional "Description." Then click "Commit to [your-branch-name]".
	- **Push:** After committing, click the "Push origin" button (usually in the top bar) to send your changes to GitHub.
	- **Pull:** Click the "Fetch origin" or "Pull origin" button to get the latest changes from GitHub.
### Using VS Code's Source Control
VS Code has built-in Git support that makes managing your changes very easy.
1. **Open the Source Control View:** Click the **Source Control icon** in the Activity Bar on the left (it looks like a three-node graph with lines, often with a badge showing pending changes, as in your image).
2. **Initialize or Open a Repo:**
	- If your project isn't a Git repo yet, VS Code will prompt you to "Initialize Repository" in the Source Control view.
	- If it's already a Git repo, it will automatically show your changes.
3. **Making Changes & Staging:**
	- As you make changes to files, they will appear in the "Changes" section of the Source Control view
	- To "stage" a file (prepare it for commit), hover over the file and click the **`+` icon** next to it, or click the **`+` icon** next to "Changes" to stage all modified files. Staged files move to the "Staged Changes" section.
4. **Committing:**
	- In the text box at the top of the Source Control view, type your **commit message**.
	- Click the **"Commit" button** (it looks like a checkmark) to save your staged changes.
5. **Pushing to GitHub:**
	- After committing, click the **"..." (More Actions)** menu in the Source Control view title bar.
	- Select **"Push"** to send your local commits to your GitHub repository.
6. **Pulling from GitHub:**
	- To get the latest changes from GitHub, click the **"..." (More Actions)** menu.
	- Select **"Pull"**.
7. **Viewing History:**
	- Many Git extensions (like GitLens) can show you a visual history of your commits directly within VS Code.
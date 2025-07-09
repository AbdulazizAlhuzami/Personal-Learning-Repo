GitHub is a website where you can store your Git projects online. It's like a cloud storage for your code, but with powerful collaboration features!
## 1. What to Include in a Repository (Repo)
A "repository" (or "repo") is your project folder on GitHub.
- **Your Project Files:** All your code, documents, images, etc.
- **`README.md` (MUST-HAVE!):**
    - A Markdown file that explains what your project is, how to use it, what it does, and anything important.
    - GitHub automatically shows this on your project's main page.
    - **Simple structure:**
```
# My Awesome Project

This project does [briefly describe what it does].

## Installation 

## How to Use
1. First go to the releases page
2. Go to the latest release
3. Download...

4. Step one.
5. Step two.
```
**`.gitignore` (Important!):**
- A text file that tells Git _what to ignore_.
- Use it to prevent Git from tracking temporary files, sensitive information (like passwords), or large files that don't belong in Git (e.g., `node_modules` folders, `.DS_Store` on Mac, `Thumbs.db` on Windows).
- Each line is a file or folder to ignore.
- **Example `.gitignore`:**
```
# Ignore common macOS files 
.DS_Store 

# Ignore common Windows files 
Thumbs.db 

# Ignore node.js modules 
node_modules/ 

# Ignore temporary files 
*.tmp 
*.log
```
## 2. Creating a New Repository on GitHub
1. Go to `github.com` and log in.
2. Click the **`+`** sign in the top right corner, then select **"New repository."**
3. **Repository name:** Choose a clear, short name (e.g., `my-first-website`, `obsidian-notes`).
4. **Description (optional):** A short sentence about your project.
5. **Public or Private:**
	- **Public:** Anyone can see your code (good for open-source projects or portfolios).
	- **Private:** Only you (and people you invite) can see it.
6. **Add a README file:** **Highly recommend checking this box** when creating a new repo on GitHub.
7. **Add .gitignore:** You can choose a template based on your project type (e.g., `Node`, `Python`).
8. Click **"Create repository."**
## 3. Connecting Your Local Project to GitHub
If you created your repo _first_ on GitHub with a README/gitignore, you'll "clone" it:
- Go to your GitHub repo page.
- Click the green **`<> Code`** button.
- Copy the HTTPS URL.
- In your terminal, go to the folder where you want to save the project and run:
```
git clone [THE_URL_YOU_COPIED]
```
*This downloads the repo to your computer.*
If you initialized Git locally (`git init`) _first_, you'll "remote add" it:
- After creating an _empty_ repo on GitHub (no README/gitignore yet).
- GitHub will show you instructions. It usually looks like this (run these in your local project folder in the terminal):
```
git remote add origin https://github.com/your-username/your-repo-name.git
git branch -M main
git push -u origin main
```
*(Note: `main` is the modern default branch name; older repos might use `master`).*
## 4. Basic Contribution Flow (Working with Others/Yourself)
1. **`git pull`:** Start your work session by pulling the latest changes from GitHub. This prevents conflicts.
2. **Make your changes:** Edit your files.
3. **`git add .`:** Stage your changes.
4. **`git commit -m "Descriptive message"`:** Save your changes locally.
5. **`git push`:** Send your changes to GitHub.
## 5. Explore GitHub Features
- **Issues:** A place to report bugs, suggest features, or ask questions about a project.
- **Pull Requests (PRs):** When you want to contribute changes to someone else's project (or merge a `feature-branch` into your `main` branch), you open a Pull Request to discuss and review your changes.
- **Wikis:** For documentation.
- **Projects:** For task management.
### Using GitHub Desktop with GitHub
GitHub Desktop makes working with GitHub repos very visual and easy.
1. **Clone a Repo:** In GitHub Desktop, go to `File > Clone Repository`. You can select a repository directly from your GitHub.com account.
2. **Publish a Repo:** If you created a new repository locally in GitHub Desktop, it will ask you if you want to "Publish repository" to GitHub.com. This creates the online version.
3. **Syncing Changes:**
	- After you commit changes in GitHub Desktop (as described in the Git document), you'll see a "Push origin" button. Click it to send your local commits to GitHub.
	- To get changes from GitHub (e.g., if you worked on another computer or someone else pushed changes), click the "Fetch origin" or "Pull origin" button.
4. **Viewing History:** The "History" tab in GitHub Desktop clearly shows all your past commits.
5. **Creating Pull Requests:** You can easily create a Pull Request directly from GitHub Desktop after pushing a new branch or changes.
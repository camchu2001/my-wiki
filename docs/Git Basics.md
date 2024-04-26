> **Resources**
> [Setting up Git](https://www.theodinproject.com/lessons/foundations-setting-up-git)
# What is Git and Github?
***Git*** is a version control system, which can be understood as an **epic save button** for your files and directory. 
***Github*** is a service that allows you to upload, host, and manage your code using **Git** with a web interface. 
# Git Commands
### 1. Create a new repository on the command line
```
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:github-user-name/repo-name.git
git push -u origin main
```
### 2. Push an existing repository from the command line
```js
git remote add origin git@github.com:github-user-name/repo-name.git
git branch -M main
git push -u origin main
```
# Meaningful Commit Messages
Writing good commits on GitHub enhances clarity for fellow developers by providing insights into your code changes and the reasons behind them. Clear and meaningful commit messages contribute to a straightforward history of your progress, making it easier for others to understand your code and track the evolution of the project.
### When to Commit?
When writing code, it’s considered best practice to ***commit every time you have a meaningful change*** in the code. This will create a timeline of your progress on the project.
### Bad vs. Good Commits
> **Resources**
> - [How to Write a Git Commit Message](https://cbea.ms/git-commit/)
> - [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
* `fix a bug` → this is a ***bad commit*** because the message is too vague and may cause confusion. 
* `fix: add missing link and alt attribute to the logo image` → this is a detailed and pretty ***good commit*** because it specifies the code’s action type (`fix`) then providing a clear and concise description of what changes were made and why it needed to be made. 

> GitHub has a **72-character limit** so it’s recommend to keep commits’ subject and description within this amount.

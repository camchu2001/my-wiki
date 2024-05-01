> **Resources**
> [Setting up Git](https://www.theodinproject.com/lessons/foundations-setting-up-git)
## What is Git and Github?
***Git*** is a version control system, which can be understood as an **epic save button** for your files and directory. 
***Github*** is a service that allows you to upload, host, and manage your code using **Git** with a web interface. 
## Git Basic Commands
### 1. Push an existing repository from the command line
```
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:<github_user_name>/<repo-name.git>
git push -u origin main
```
### 2. Remove remote origin
```
// verify remote origin
git remote -v 

// remove remote origin
git remote remove origin
```
## Git Branching
![](https://i.imgur.com/QkA8uV5.png)
* The **default branch** is just what we call the branch that is created when you make your first commit on a project, and in that command we set the name to be `main` as is the current standard.
* Like the branches in a tree (hence the name), all of the branches for a project stem off of a “trunk” (the `main` branch) or off of _other_ branches.
* When you make commits on a specific branch, those changes only exist on **that** branch, leaving all of your other branches exactly as they were when you branched off of them.
→ You can keep your `main` branch as a place for only finished features that you know are working properly, and add each feature to your project using dedicated branches which we call _feature branches_.
1. <u>**Create a new branch**</u>
```
git checkout -b <branch_name> 
```
 2. <u>**Switch to a branch**</u>
```
git checkout <branch_name>
```
3. <u>**View all current branches**</u>
```
git branches
```
4. <u>**Merge branches**</u>
Take the changes from <branch_name> and add them to the branch you’re currently on. 
```
git merge <branch_name>
```
5. <u>**Delete branch**</u>
```
git branch -d <branch_name>
```
## Meaningful Commit Messages
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

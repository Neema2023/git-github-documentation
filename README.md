Git & GitHub
1. What is Git?
Git is a version-control system. It helps you track changes in your project.
For example:
MyProject
   ↓
Git tracks changes
   ↓
You can save versions
   ↓
You can go back to previous versions
2. What is GitHub?
GitHub is an online platform where you can store Git repositories and collaborate with other developers.
Think of it like:
Git     = manages your project versions on your computer
GitHub  = stores/shares your Git project online
3. Check if Git is installed
Open the Terminal in VS Code and type:
git --version
Example result:
git version 2.x.x
If you see a version number, Git is installed.
4. Create a Git repository
If you already have a project and want Git to track it:
git init
What does it mean?
It creates a Git repository inside your project.
Before:
MyProject
├── src
├── pom.xml
After git init:
MyProject
├── src
├── pom.xml
└── .git
.git contains Git's information about your project.

5. Check the status of your project
git status
This is one of the most important commands.
It tells you:
•	which files have changed 
•	which files are ready to commit 
•	which files are not tracked 
•	whether you have merge conflicts 
Example:
modified: UserService.java
modified: UserController.java

6. Add files
git add .
The . means:
Add all changed files.
You can also add one specific file:
git add UserService.java
Important
git add does not upload your files to GitHub.
It prepares them for a commit.

7. Commit your changes
git commit -m "Add user service"
A commit is like taking a snapshot/save point of your project.
For example:
git add .
      ↓
Prepare changes
      ↓
git commit
      ↓
Save changes in Git
Good commit messages describe what you changed.
Examples:
git commit -m "Add login feature"
git commit -m "Fix user registration"
git commit -m "Update product controller"
Avoid messages like:
git commit -m "changes"
when you can be more specific.

8. Connect your project to GitHub
First create a repository on GitHub.
Then connect your local project:
git remote add origin https://github.com/USERNAME/REPOSITORY.git
Example:
git remote add origin https://github.com/liliane/MyProject.git
Check the connection
git remote -v
You should see your GitHub repository.

9. Rename your main branch
Modern GitHub repositories normally use main.
git branch -M main
This renames your current branch to main.
10. Push your project to GitHub
For the first push:
git push -u origin main
What does it mean?
git push
Send your commits to GitHub.
origin
Your GitHub repository.
main
The branch you are pushing.
-u
Sets the upstream relationship so later you can simply use:
git push
11. The basic workflow
After your project is connected to GitHub, your normal workflow is:
git status
git add .
git commit -m "Describe your changes"
git push
Think:
CHANGE CODE
    ↓
git status
    ↓
git add .
    ↓
git commit
    ↓
git push
    ↓
GITHUB
12. Branches
A branch allows you to work on something without directly changing main.
For example:
main
 │
 ├── feature-login
 │
 ├── feature-payment
 │
 └── bug-fix
Usually:
main
contains the stable/main version.
You create another branch to work on a feature.
13. See your branches
git branch
Example:
* main
  10
The * shows your current branch.
If you have:
* 10
  main
you are currently working on branch 10.
14. Create a new branch
git checkout -b feature-login
This does two things:
1.	Creates feature-login 
2.	Switches you to it 
You can verify:
git branch
You might see:
  main
* feature-login



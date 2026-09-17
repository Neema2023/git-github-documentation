# Git & GitHub

## Introduction

Git and GitHub are commonly used in software development to manage source code, track changes, and support collaboration between developers.

In this documentation, I demonstrate ten Git commands that I used to manage and work with a project repository.

---

## 1. `git clone`

### Command

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
```

### Explanation

The `git clone` command copies an existing repository from GitHub to my local computer.

It allows me to get the project files, branches, and Git history so that I can work on the project locally.

### Example

```bash
git clone https://github.com/Neema2023/MyProject.git
```

---

## 2. `git log`

### Command

```bash
git log
```

### Explanation

The `git log` command displays the history of commits in the repository.

It helps me see previous changes, including the commit message, author, and date.

### Example

```text
commit 82ab451
Author: Neema
Message: Add project documentation
```

---

## 3. `git diff`

### Command

```bash
git diff
```

### Explanation

The `git diff` command shows the changes that have been made to files but have not yet been staged.

It helps me review my changes before adding them to the staging area.

### Example

```bash
git diff
```

This allows me to identify what was added, removed, or modified.

---

## 4. `git show`

### Command

```bash
git show
```

### Explanation

The `git show` command displays information about a specific commit.

It can show the commit details and the changes introduced by that commit.

### Example

```bash
git show
```

This is useful when I want to inspect what was changed in a particular version of the project.

---

## 5. `git remote`

### Command

```bash
git remote
```

### Explanation

The `git remote` command displays the names of remote repositories connected to my local repository.

For example:

```text
origin
```

`origin` normally represents the GitHub repository from which the project was cloned or to which it is connected.

---

## 6. `git fetch`

### Command

```bash
git fetch origin
```

### Explanation

The `git fetch` command downloads information about new changes and branches from the remote GitHub repository without immediately merging those changes into my current branch.

It allows me to check what has changed on GitHub before integrating the changes into my local work.

### Example

```bash
git fetch origin
```

---

## 7. `git stash`

### Command

```bash
git stash
```

### Explanation

The `git stash` command temporarily saves my uncommitted changes.

This is useful when I need to switch branches but I am not ready to commit my current work.

For example:

```bash
git stash
git switch main
```

Later, I can restore the saved changes using:

```bash
git stash pop
```

---

## 8. `git tag`

### Command

```bash
git tag v1.0
```

### Explanation

The `git tag` command creates a tag that identifies a particular point in the project's history.

Tags are often used to mark important versions or releases.

For example:

```bash
git tag v1.0
```

This can identify a version of the project as `v1.0`.

---

## 9. `git reset`

### Command

```bash
git reset HEAD~1
```

### Explanation

The `git reset` command can be used to move the current branch to an earlier commit or remove a commit from the current branch history.

For example:

```bash
git reset HEAD~1
```

This moves the current branch one commit backward while keeping the changes in the working directory.

This command should be used carefully because different reset options can affect commits and working files differently.

---

## 10. `git clean`

### Command

```bash
git clean -n
```

### Explanation

The `git clean` command is used to identify or remove untracked files from the working directory.

The `-n` option performs a preview. It shows which untracked files would be removed without actually deleting them.

Example:

```bash
git clean -n
```

If I confirm that the files should be removed, I can use:

```bash
git clean -f
```

The `-f` option actually removes the untracked files, so it should be used carefully.

---

# Summary of My 10 Git Commands

| No. | Git Command  | Purpose                                        |
| --- | ------------ | ---------------------------------------------- |
| 1   | `git clone`  | Copy a GitHub repository to the local computer |
| 2   | `git log`    | View commit history                            |
| 3   | `git diff`   | View unstaged changes                          |
| 4   | `git show`   | Inspect a commit and its changes               |
| 5   | `git remote` | View connected remote repositories             |
| 6   | `git fetch`  | Download information from a remote repository  |
| 7   | `git stash`  | Temporarily save uncommitted changes           |
| 8   | `git tag`    | Mark a specific project version                |
| 9   | `git reset`  | Move the branch back to an earlier commit      |
| 10  | `git clean`  | Preview or remove untracked files              |

# Conclusion

Git provides many commands that help developers manage source code and maintain the history of their projects. The ten commands demonstrated above provide additional ways to inspect a repository, work with remote repositories, manage temporary changes, identify versions, and maintain the working directory.

Using these commands helps me understand how Git can support organized software development and collaboration through GitHub.

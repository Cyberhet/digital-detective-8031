# Mission 6 — Git and GitHub

## 1. Task / objective
Understand version control, stage and commit changes, create a branch, open a Pull Request, and explain the team collaboration workflow.

## 2. Work completed

### Task 6.1 — Understand the basic Git workflow

| Git operation | What it does in your own words |
|---|---|
| Check repository status (`git status`) | Displays the current working tree status: staged changes, unstaged modifications, and untracked files. |
| Stage selected changes (`git add <file>`) | Moves specific modified files from the working directory into the staging area (index) to prepare them for the next commit. |
| Create a commit (`git commit -m "message"`) | Takes a snapshot of all currently staged changes and permanently saves it into the repository history with an author and message. |
| View commit history (`git log --oneline`) | Displays a reverse chronological timeline of past commits, listing short SHA hashes and commit descriptions. |

#### Difference between Staging and Committing:
- **Staging (`git add`):** Acts as a draft preparation table where you pick and choose which specific modifications or files to group together into a logical unit of work.
- **Committing (`git commit`):** Takes whatever is currently staged and records a permanent, cryptographically hashed checkpoint into the repository's permanent history.

---

### Task 6.2 — Create and use a branch
- Created a separate feature branch:
  ```bash
  git checkout -b update-about
  ```
- Added a "My Learning" section to the root `README.md` reflecting on insights gained.
- Staged, committed, and published the branch to the remote repository:
  ```bash
  git add README.md
  git commit -m "Add My Learning section to root README"
  git push -u origin update-about
  ```

---

### Task 6.3 — Create a Pull Request
- **Pull Request (PR) workflow:**
  1. Opened GitHub repository and navigated to the compare & pull request view for branch `update-about`.
  2. Created a PR targeting `main` from `update-about` with a clear description of changes.
  3. Reviewed the diff online to verify no extraneous files were included.
  4. Merged the PR into `main` (or documented review status if instructor verification is required).
  5. Switched back to local `main` and synced with `git pull origin main`.

#### What are branches and Pull Requests, and why are they useful?
- A **branch** creates an isolated line of development where changes can be made without destabilizing the stable `main` codebase.
- A **Pull Request** is a collaborative review mechanism where code changes from a feature branch are inspected, discussed, tested, and approved before being merged into the primary branch. This prevents broken code from entering production and facilitates peer code reviews.

---

### Task 6.4 — Git command glossary
| Git operation | One-line explanation in your own words |
|---|---|
| Initialise a repository (`git init`) | Sets up a brand-new Git version-tracking database (`.git` folder) in the current directory. |
| Check status (`git status`) | Shows tracked, modified, and staged files relative to the latest commit. |
| Stage changes (`git add`) | Indexes modified files into the staging area ready for the next commit snapshot. |
| Commit changes (`git commit`) | Records indexed changes into permanent repository history with a descriptive log message. |
| View history (`git log`) | Lists previous commits showing commit hashes, author details, dates, and messages. |
| Create or list branches (`git branch`) | Lists all local development branches or creates a new branch pointer. |
| Switch branches (`git checkout` / `git switch`) | Moves `HEAD` and changes the working directory files to match the specified branch state. |
| Publish changes (`git push`) | Uploads local branch commits to the corresponding remote repository on GitHub. |
| Retrieve remote changes (`git pull`) | Fetches updates from the remote GitHub branch and merges them directly into the local branch. |

## 3. Commands / tools used
- `git status`, `git add`, `git commit`
- `git log --oneline --graph`
- `git branch`, `git checkout -b`, `git switch`
- `git push`, `git pull`
- GitHub web interface for Pull Request creation, code review, and branch merging.

## 4. My understanding
I understood that version control provides complete traceability and safety when writing code. Commits act as permanent checkpoints that can be revisited if bugs occur, and branching combined with Pull Requests allows multiple developers to contribute concurrently without overwriting each other's work.

## 5. Difficulties faced
Resolving differences between remote branch state and local working copy when syncing after a remote merge.

## 6. How I resolved them
Used `git fetch origin` followed by `git status` and `git pull` to keep the local main branch cleanly updated.

## 7. Evidence / files
- Git commit log history.
- Branch and Pull Request documentation in `mission-06-git-github/README.md`.

## 8. Commit details
- **Commit message:** `Complete Git and GitHub collaboration mission`
- **Pushed to GitHub:** Yes

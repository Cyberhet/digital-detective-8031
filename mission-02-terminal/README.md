# Mission 2 — Become comfortable with the Terminal

## 1. Task / objective
Use the command-line interface to inspect folders, create and manage practice files, understand options and pipes, and explain package managers.

## 2. Work completed

### Task 2.1 — Explore basic Terminal operations
| Operation / command name | What it does | What I observed |
|---|---|---|
| Current-directory display (`pwd`) | Prints the full path of the current working directory. | Displayed `/Users/het/digital-detective-8031`. |
| Directory listing (`ls`) | Lists names of non-hidden files and folders in the current location. | Displayed all mission folders and repository files. |
| Detailed listing (`ls -l`) | Displays detailed information including permissions, owner, size, and modification timestamp. | Formatted list with file metadata and timestamps. |
| Change directory (`cd ..`) | Moves navigation up one level to the parent directory. | Path changed from project folder to `/Users/het`. Returned using `cd digital-detective-8031`. |
| Create directory (`mkdir terminal-practice`) | Creates a new directory with the specified name. | New folder `terminal-practice` appeared in the workspace. |
| Create empty file (`touch notes.txt`) | Creates a new empty file or updates timestamp if it exists. | An empty file `notes.txt` was created inside the practice folder. |
| Copy file (`cp notes.txt notes-copy.txt`) | Creates a duplicate copy of the target file under a new name. | Duplicate file was created while preserving the original. |
| Move / rename file (`mv notes-copy.txt notes-backup.txt`) | Renames a file or moves it to another location. | File was safely renamed to `notes-backup.txt`. |
| Display file contents (`cat notes.txt`) | Reads and outputs the contents of a text file to Terminal standard output. | Printed the written text lines directly to the console. |

---

### Task 2.2 — Practise file changes safely
Completed in `terminal-practice/` directory:
1. Created `notes.txt` with initial text using `echo "hey guys" > notes.txt`.
2. Appended second line using `echo "this is the appended line" >> notes.txt`.
3. Verified both lines using `cat notes.txt`.
4. Created and renamed backup copy: `cp notes.txt notes-copy.txt` then `mv notes-copy.txt notes-backup.txt`.

#### Questions & Answers:
- **What is the difference between replacing a file's contents and adding text to the end?**
  Replacing (`>`) overwrites and truncates the existing file content with new data, whereas adding (`>>`) appends new lines to the end of the file, preserving all existing contents.
- **What is the difference between copying a file and moving a file?**
  Copying (`cp`) leaves the original file untouched and creates a separate clone at the destination. Moving (`mv`) relocates or renames the file, removing it from its original path/name.
- **What information does the current-directory display provide?**
  `pwd` (Print Working Directory) provides the complete absolute path from the root directory (`/`) to where the terminal shell is currently operating.
- **Why is a directory-listing operation useful?**
  It allows the user to inspect what files and directories exist in the current folder, verify file creation/deletion, check filenames before executing commands, and view timestamps and permissions.

---

### Task 2.3 — Understand flags and pipes
- **Flags/Options (`ls` vs `ls -lah`):**
  - A flag modifies command behavior. Running plain `ls` only lists visible file names.
  - Running `ls -lah` uses:
    - `-l`: Long listing format showing permissions, link count, owner, group, file size, and timestamp.
    - `-a`: All files, including hidden files and directories starting with `.` (e.g. `.git`).
    - `-h`: Human-readable file sizes (e.g. `4.0K`, `128B`) instead of raw byte counts.
- **Pipes (`|`):**
  - Running `ls -lah | head -n 5` redirects the standard output (`stdout`) of `ls -lah` directly into the standard input (`stdin`) of `head -n 5`.
  - The left side produces the full detailed directory listing, and the right side filters and displays only the first 5 lines.

---

### Task 2.4 — Understand package managers
A package manager (such as **Homebrew** on macOS) is a command-line tool that automates installing, configuring, upgrading, and removing software packages and development tools. It automatically handles dependency resolution so all required supporting libraries are installed together, preventing version conflicts and eliminating manual download/drag-and-drop installations.

## 3. Commands / tools used
- `pwd`, `ls`, `ls -l`, `ls -lah` — Inspected directory path and contents with options.
- `cd`, `mkdir`, `touch`, `cp`, `mv`, `cat` — Navigation and safe file manipulation.
- `>`, `>>` — Redirection operators for writing and appending text.
- `|` (pipe), `head` — Stream chaining and output truncation.

## 4. My understanding
I understood that the Terminal offers precise, rapid control over the operating system. Flags customize command behavior without needing different tools, and pipes allow small single-purpose tools to be composed into powerful processing pipelines.

## 5. Difficulties faced
Understanding how the pipe operator passes streams in memory between programs rather than writing intermediate temporary files to disk.

## 6. How I resolved them
Tested practical pipe examples with `ls` and `head`, observing how `head` immediately consumes the piped output stream from `ls`.

## 7. Evidence / files
- `terminal-practice/notes.txt`
- `terminal-practice/notes-backup.txt`
- Command reference and observation tables in this README.

## 8. Commit details
- **Commit message:** `Complete Terminal and file management mission`
- **Pushed to GitHub:** Yes

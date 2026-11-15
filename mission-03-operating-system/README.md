# Mission 3 — Understand the operating system

## 1. Task / objective
Explore the operating system, running processes, storage, paths and file permissions, and describe the core responsibilities of an operating system.

## 2. Work completed

### Task 3.1 — Explore your operating system
*(Privacy Note: Personal identifiers such as device names and usernames are redacted as `[redacted]` per assignment guidelines).*

| Information explored | What it tells you | Your observation (privacy-safe) |
|---|---|---|
| Operating system / system details | Identifies the OS name, kernel version, and build architecture. | macOS Darwin Kernel Version 25.x / arm64 |
| Current account identity | Identifies the currently active user account running the shell. | `[redacted-user]` (non-root standard user account) |
| Available and used storage | Displays disk filesystem capacity, used space, and free space. | Main volume (`/System/Volumes/Data`): ~460GB capacity, ~40% used, ~270GB available |
| System activity snapshot | Provides real-time metrics on CPU usage, load averages, memory allocations, and active tasks. | CPU: ~5-10% user/sys, Memory: ~12GB used / 4GB cached, ~400 total active tasks |

---

### Task 3.2 — Understand processes
- **What is a process?**
  A process is an active instance of a computer program in execution. It contains the program's code, its current execution state, dedicated memory address space, and allocated system resources.
- **What does the PID column represent?**
  PID stands for **Process Identifier**. It is a unique numeric identifier assigned by the operating system kernel to each active process to track, control, prioritize, and manage it independently.
- **Two examples of processes running on this computer:**
  1. `Terminal` / `zsh` (Interactive shell process)
  2. `Visual Studio Code` / `Code Helper` (Application editor process)

---

### Task 3.3 — Understand paths and permissions

#### Absolute vs Relative Paths
- **Absolute path:** The complete filesystem path starting from the root directory (`/`), independent of the current working location.
  - *Example:* `/Users/[redacted]/digital-detective-8031/mission-03-operating-system`
- **Relative path:** A path specified relative to the current working directory, using references like `.` (current) or `..` (parent).
  - *Example:* `./mission-03-operating-system/README.md` or `../terminal-practice`

#### File Permissions
Inspected using `ls -l`:
| Permission | Meaning | Example |
|---|---|---|
| `r` — Read | Allows the contents of a file to be opened and viewed; on directories, allows listing contents. | Opening a `.txt` file or viewing `README.md`. |
| `w` — Write | Allows modifying, editing, renaming, or deleting the file contents. | Editing and saving changes in a text editor. |
| `x` — Execute | Allows a file to be executed as a binary program or shell script; on directories, allows traversal and entry. | Running a Python script or entering a folder with `cd`. |

---

### Task 3.4 — Explain operating-system responsibilities
| OS responsibility | Your explanation | Example |
|---|---|---|
| Process management | Allocates CPU time slices, schedules active threads, and coordinates process lifecycle (creation, pause, termination). | Switching between a code editor and a web browser without crashing. |
| Memory management | Tracks primary memory (RAM) allocation for running applications and swaps data to virtual memory when RAM is full. | Allocating 500 MB of RAM to VS Code while reclaiming memory from closed tabs. |
| Device management | Coordinates communication between computer hardware devices and software using device drivers. | Translating keyboard keypresses or USB drive read/write requests. |
| File management | Manages file storage hierarchies, directories, file metadata, permissions, and disk block allocation. | Creating folders, saving files, and organizing the directory tree. |
| User interface / shell | Provides an interface (CLI or GUI) enabling users and software to interact with the OS kernel. | macOS Terminal (`zsh`) or Finder graphical window. |
| Security and permissions | Protects files and memory space against unauthorized access by enforcing user accounts and access control lists. | Preventing standard users from modifying `/System` core files. |

## 3. Commands / tools used
- `uname -a`, `sw_vers` — Inspected operating system build and kernel version.
- `whoami` — Checked active user account identity.
- `df -h` — Displayed disk storage statistics in human-readable format.
- `top -l 1`, `ps aux` — Inspected system activity and active process table.
- `ls -l` — Inspected file owner and permissions strings.

## 4. My understanding
I understood that the operating system acts as the essential bridge between physical hardware and application software. It manages resources (CPU, RAM, disk, I/O) efficiently and securely so multiple programs can run concurrently without interfering with each other.

## 5. Difficulties faced
Interpreting the 10-character permission string (`-rw-r--r--`) and understanding user, group, and others permissions.

## 6. How I resolved them
Broke down the permission string into its constituent triplets: file type (`-`), owner permissions (`rw-`), group permissions (`r--`), and other permissions (`r--`).

## 7. Evidence / files
- Privacy-safe system details, process notes, and OS responsibility tables in `mission-03-operating-system/README.md`.

## 8. Commit details
- **Commit message:** `Document operating system and file management`
- **Pushed to GitHub:** Yes

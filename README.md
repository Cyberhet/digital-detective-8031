# The Digital Detective — Mini System Report

> **Diwali Independent Learning Assignment**  
> *Explore Your Computer • Build a Mini System Report*

---

## Student Information
| Field | Details |
|---|---|
| **Repository Name** | `digital-detective-8031` |
| **Repository URL** | [https://github.com/cyberhet/digital-detective-8031](https://github.com/cyberhet/digital-detective-8031) |
| **USN (Last 4 Digits)** | `8031` |
| **OS Environment** | macOS (Darwin / arm64) |
| **Primary Tools** | Python 3.14, Git 2.54, Terminal (zsh), VS Code |

---

## Assignment Overview
**The Digital Detective** is an investigation into how personal computers operate. The assignment covers computer hardware fundamentals, operating system services, process management, command-line operations, binary and data representations, program compilation and interpretation, Git/GitHub collaboration workflows, and computer network architecture.

Every mission in this assignment was completed, documented, and committed sequentially with dedicated git checkpoints.

---

## Mission Index
| Mission | Focus Area | README Link | Key Deliverables |
|:---:|---|:---:|---|
| **0** | Repository & Workspace Setup | [Mission 0 README](mission-00-setup/README.md) | Verified tools (Python, Git), workspace folder structure |
| **1** | Computer Fundamentals & IPOS | [Mission 1 README](mission-01-computer-basics/README.md) | IPOS analysis, hardware vs software classification, everyday systems |
| **2** | Terminal & File Management | [Mission 2 README](mission-02-terminal/README.md) | Command reference (`pwd`, `ls`, `mkdir`, `cp`, `mv`, `cat`), pipes, Homebrew |
| **3** | Operating System, Processes & Permissions | [Mission 3 README](mission-03-operating-system/README.md) | OS inspection, process tables (PID), file permissions (`rwx`), OS roles |
| **4** | How Programs Run | [Mission 4 README](mission-04-programs/README.md) | Working `hello.py`, Compiler vs Interpreter analysis |
| **5** | Numbers & Data Representation | [Mission 5 README](mission-05-numbers-data/README.md) | Manual base conversions, ASCII/UTF-8 notes, working `number_converter.py` |
| **6** | Git, GitHub & Pull Requests | [Mission 6 README](mission-06-git-github/README.md) | Git lifecycle, `update-about` branch, Pull Request review, command glossary |
| **7** | Computer Networks | [Mission 7 README](mission-07-networking/README.md) | Network types (LAN/MAN/WAN), DNS, router, 7-step website loading walkthrough |
| **8** | Final Review & Submission | [Mission 8 README](mission-08-final-report/README.md) | Full repository audit, completion checklist, submission verification |

---

## Topics Explored
1. **Input, Processing, Output, and Storage (IPOS):** Tracing hardware and data lifecycles.
2. **Command-Line Interface (CLI):** Navigating filesystems, streams, flags, and pipes.
3. **Operating System Architecture:** Kernel roles, memory allocation, process scheduling, access permissions.
4. **Program Execution:** Comparing compiled ahead-of-time binaries and interpreted dynamic execution.
5. **Data Representation:** Converting between decimal, binary, and hexadecimal; character encoding standards (ASCII vs UTF-8).
6. **Distributed Version Control:** Git branch management, staging, atomic commits, Pull Requests, remote sync.
7. **Computer Networks:** Packet switching, routing, DNS name resolution, transport and application protocols.

---

## Running the Number Converter
The Python number converter program is located in `mission-05-numbers-data/`. To run it interactively:

1. Open your Terminal and navigate to the project directory:
   ```bash
   cd digital-detective-8031
   ```
2. Run the script using Python 3:
   ```bash
   python3 mission-05-numbers-data/number_converter.py
   ```
3. Enter any positive decimal integer when prompted:
   ```text
   Enter a decimal number: 25
   Binary: 0b11001
   Hexadecimal: 0x19
   ```

---

## My Learning
Throughout this assignment, I developed a hands-on mental model of how computer systems operate end-to-end:
1. **The CLI is a superpower:** Working in Terminal demystified the graphical user interface. Commands like `ls`, `grep`, pipes (`|`), and flags make file management and system inspection faster and scriptable.
2. **Code requires an execution engine:** Programs do not run by magic; compilers convert source text to machine code ahead of time, while interpreters evaluate instructions dynamically at runtime.
3. **Data is universal bits:** All texts, numbers, and media reduce to 0s and 1s. Understanding bases (decimal, binary, hex) and encoding schemes (ASCII and UTF-8) clarifies how computers reliably store and interchange information.
4. **Git gives safety and collaboration:** Staging, branching, and atomic commits make software development predictable, traceable, and secure.
5. **Networking powers connectivity:** Understanding packets, DNS resolution, and client-server communication clarifies how the modern web functions.

---

## Workflow & Privacy Notice
- Each mission was completed, documented in its dedicated folder README, and committed individually.
- All personal identifying details (passwords, access tokens, private Wi-Fi names, router IP addresses, and sensitive device usernames) have been safely redacted (`[redacted]`) throughout all logs and documentation.

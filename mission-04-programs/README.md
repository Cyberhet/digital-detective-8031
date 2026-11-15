# Mission 4 — How programs run

## 1. Task / objective
Run a simple Python program and compare how compilers and interpreters translate or execute programs.

## 2. Work completed

### Task 4.1 — Create and run a Python program
- Created `hello.py` inside `mission-04-programs/` containing:
  ```python
  print("Hello from Python")
  ```
- Executed using Python 3 in Terminal:
  ```bash
  python3 hello.py
  ```
- **Output confirmed:**
  ```text
  Hello from Python
  ```

---

### Task 4.2 — Compare compiler and interpreter

#### Comparison Table
| Point | Compiler | Interpreter |
|---|---|---|
| When translation / execution happens | Translates the entire source code into machine code or bytecode all at once before execution. | Translates and executes the program line by line (or instruction by instruction) directly at runtime. |
| Typical output | Standalone executable binary file (e.g., `.exe`, ELF binary, or `.o` object file). | Direct execution output in memory; no standalone machine-code binary saved to disk. |
| One example | C, C++, Rust, Go | Python, JavaScript, Ruby |
| One advantage | Fast runtime execution speed and early compile-time syntax/type error checking. | Faster development cycle with instant testing, interactive REPL debugging, and cross-platform portability. |

#### Explanation
A compiler translates all human-readable source code into machine code prior to program execution, producing an independent binary that runs very quickly on the target CPU architecture. In contrast, an interpreter reads and processes source statements dynamically at runtime without generating an ahead-of-time binary. Compilers detect syntax and semantic errors during the build stage before any execution occurs, while interpreters execute instructions up until they encounter a runtime error. Many modern language implementations (such as Python's CPython) combine both paradigms by first compiling source code into bytecode (`.pyc`) before running it on a virtual machine interpreter.

## 3. Commands / tools used
- `python3 hello.py` — Executed the Python script from Terminal.
- Python 3.14 runtime environment.

## 4. My understanding
I understood how computer programs transition from human-readable text into machine instructions. Compilers perform full translation ahead of time for peak efficiency, whereas interpreters provide rapid prototyping and dynamic line-by-line execution.

## 5. Difficulties faced
Understanding whether Python is purely interpreted or if compilation is involved behind the scenes.

## 6. How I resolved them
Researched CPython execution flow and learned that Python first compiles code into intermediate bytecode instructions, which the Python Virtual Machine (PVM) then interprets.

## 7. Evidence / files
- `mission-04-programs/hello.py`
- Comparison table and notes in `mission-04-programs/README.md`.

## 8. Commit details
- **Commit message:** `Compare compilers and interpreters`
- **Pushed to GitHub:** Yes

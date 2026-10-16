# Multi-Process Command Pipeline System

## Abstract
This project implements a Linux command pipeline executor using C and POSIX system calls.

## Objectives
- Execute multiple Linux commands.
- Create child processes using fork().
- Execute programs using execvp().
- Transfer data using pipes.
- Redirect input and output using dup2().
- Synchronize processes using waitpid().
- Display process IDs, exit codes, and execution time.

## Technologies
- C
- Linux / Ubuntu
- GCC
- POSIX system calls
- Git and GitHub

## System Calls
| System Call | Purpose |
|---|---|
| fork() | Create a child process |
| execvp() | Execute a program |
| pipe() | Establish inter-process communication |
| dup2() | Redirect standard input/output |
| waitpid() | Collect child-process status |
| close() | Close file descriptors |

## Compilation
gcc -Wall -Wextra -std=c11 src/main.c -o pipeline

## Execution
./pipeline

## Example
printf "apple\nbanana\napple\n" | sort | uniq -c

## Limitations
The current parser supports simple whitespace-separated commands. It does not implement full shell syntax, quoting, or shell redirection.

## Future Enhancements
- Concurrent independent pipeline execution
- Interactive process monitoring
- Execution history
- Performance analysis
- Automated testing

# Linux Software Processes Overview

A **process** is a **running instance of a program** with its own memory, CPU context, and system resources, managed by the Linux kernel.

## When You Run a Program

When you execute a program (e.g., `bash`, `nginx`, or `python`), the Linux kernel:

1. Loads the program into **memory**.
2. Assigns a unique **Process ID (PID)**.
3. Creates a **process** to execute the program.

## Summary

- **Program** → A file stored on disk.
- **Process** → A running instance of a program.
- Every process has:
  - A unique **PID**
  - Its own memory
  - CPU execution context
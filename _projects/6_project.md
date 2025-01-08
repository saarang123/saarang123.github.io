---
layout: page
title: Custom Bash Shell
description: Feature-rich shell environment with advanced functionality
img: assets/img/bash.png
redirect: /projects/all_projects#bash
importance: 7
category: work
---

This project was part of my CS252 Systems Programming course at Purdue. 

Built a robust shell environment replicating GNU Bash functionality with advanced features:

#### Command Processing

- Developed sophisticated command parser handling:
  - Complex command pipelines with multiple stages
  - I/O redirection (>, >>, <, 2>, &>) with file descriptor management
  - Command substitution ($(command)) and variable expansion
  - Environment variable management and PATH resolution
  - Wildcard expansion and filename globbing

#### Process Management

- Implemented job control system tracking foreground/background processes
- Built process group management for pipeline execution
- Added signal handlers for:
  - Ctrl-C (SIGINT) with proper process group termination
  - Ctrl-Z (SIGTSTP) for job suspension
  - SIGCHLD for zombie process cleanup and job status updates
- Managed process states (Running, Stopped, Terminated) with job table

#### Interactive Features

- Developed line editing with:
  - Emacs-style key bindings (Ctrl-A, Ctrl-E, etc.)
  - History navigation with search (Ctrl-R)
  - Context-aware tab completion for commands, files, and directories
- Implemented command history with persistent storage
- Added shell scripting support:
  - Conditional execution (&&, ||)
  - Subshell execution with proper environment inheritance
  - Exit status checking and error handling
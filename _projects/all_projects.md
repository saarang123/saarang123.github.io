---
layout: page
title: Projects
description: Collection of other projects
img: assets/img/1.png
importance: 5
category: work
---

## Mesh Simplification for Motion Planning

<a name="mesh"></a>

Developed an advanced 3D pathfinding system optimized through mesh simplification:

#### Mesh Processing

- Implemented multiple mesh simplification algorithms:
  - Quadratic Error Metrics (QEM) for vertex pair contraction
  - Edge collapse with topology preservation
  - Vertex clustering for rapid simplification
- Built mesh validation ensuring manifold preservation
- Developed adaptive simplification based on curvature and feature preservation

#### Motion Planning

- Implemented multiple pathfinding algorithms:
  - A\* with custom heuristics for 3D navigation
  - RRT (Rapidly-exploring Random Trees) with dynamic step sizing
  - Bi-directional RRT\* for optimal path finding
- Added collision detection using spatial hashing
- Developed path smoothing and optimization post-processing

### Performance Optimization

- Achieved 30% reduction in computation time through:
  - Spatial indexing for rapid nearest neighbor queries
  - Multi-resolution mesh representation
  - Parallel processing for collision checking
- Implemented benchmarking framework for comparing different simplification levels
- Analyzed and optimized memory usage for large-scale environments

## Simple C Compiler

<a name="c-compiler"></a>

Developed a full-featured compiler for a subset of C, implementing sophisticated compilation pipeline stages:

#### Frontend

- Built lexical analyzer using Flex to handle C tokens, keywords, and complex string/character literals
- Implemented recursive descent parser with Bison/Yacc supporting:
  - Function definitions with parameter passing and return values
  - Control flow (if/else, while, for) with proper scoping
  - Complex expressions with operator precedence and associativity
  - Array declarations and pointer arithmetic

#### Semantic Analysis

- Implemented symbol table with hash-based lookup for global variables and functions
- Local variables supported by stack allocation through specialized compilation to x86-64 instructions
- Built type system supporting longs, chars, and pointers.
- Added semantic checks for type compatibility in assignments and operations.

#### Code Generation

- Generated optimized x86-64 assembly targeting Linux ABI
- Managed stack frames with proper alignment and calling conventions
- Features implemented in outputted x86-64 assembly:
  - Constant folding and propagation
  - Dead code elimination
  - Readable and formatted x86 code blocks in output

## Custom Bash Shell Implementation

<a name="bash"></a>

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

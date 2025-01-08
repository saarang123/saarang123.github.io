---
layout: page
title: Simple C Compiler
description: A compiler implementation for a subset of C language
img: assets/img/compiler.png
importance: 6
category: work
---

Developed a full-featured compiler for a subset of C, implementing sophisticated compilation pipeline stages:

This project was part of my CS250 Computer Architecture class at Purdue University. 

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

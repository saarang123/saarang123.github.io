---
layout: page
title: TinyVerify - Translation Validation for Tinygrad
description: Translation Validation for the lightweight Tinygrad ML compiler
img: assets/img/3.jpg
importance: 2
category: work
giscus_comments: false
---

Compiler validation is crucial for ensuring the reliability of compiler optimizations, particularly in complex frameworks like LLVM. Traditional testing methods often fall short, prompting the use of formal verification techniques like those in the Alive2 framework, which uses SMT solvers to ensure that optimized LLVM Intermediate Representation (IR) code preserves the semantics of the original.

While LLVM and Alive2 focus on traditional programming languages, the rise of machine learning (ML) frameworks presents new challenges in verifying compilation from high-level models to low-level hardware-specific code, as ML compilers like TVM and XLA must handle complex optimizations for tensor operations and diverse hardware targets, making formal verification essential for both correctness and performance.

Tinygrad, an emerging Python-based ML framework, exemplifies these challenges. It compiles models directly into low-level GPU-specific instructions such as PTX for Nvidia GPUs or Metal for Apple GPUs, using an IR that is optimized throughout the process. Our work focuses on applying SMT-based translation validation techniques to ensure the correctness of these IR optimizations. By leveraging tools similar to Alive2, we aim to validate that the IR optimizations within Tinygrad preserve the functional behavior of the original model, regardless of the target backend.

Below is an example of a small function in Tinygrad, the generated kernel, and its respective optimized IR:

![Tinygrad](./assets/img/tinygrad.png)

Our encoding for the kernels is done through the Python Z3 library, some features of how we encode kernels is shown below:

![Encoding](./assets/img/encoding.png)


While TinyVerify validates more than half of Tinygrads operations currently, we are still working on:

- expanding the framework to properly integration of Undefined Behavior (UB) to verify abstraction refinement,
- greater support for floating point by modifying Tinygrad source to abide to IEEE standards,
- support formal verification for schedules as well, not just on kernel rewrites. (support the entire pipeline from kernel scheduling to compiler optimizations)

Github: [https://github.com/knightron0/tinyverify](https://github.com/knightron0/tinyverify) (may not be open source yet)



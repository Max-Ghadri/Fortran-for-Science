# Fortran-for-Science

A hands-on Modern Fortran tutorial with Intel Fortran (ifort) featuring clean workflow, consistent coding templates, and minimal runnable examples for scientific computing.

## Overview

This repository provides a structured learning path for scientists and engineers transitioning to Modern Fortran, with each topic including both documentation and executable code examples.

## Key Features

- **Clean Workflow**: Consistent coding templates and minimal examples
- **Intel Fortran Focus**: Primary support for ifort with gfortran compatibility
- **Hands-on Learning**: Each concept includes both documentation and runnable code
- **Scientific Computing**: Practical examples for variables, loops, conditionals, file I/O, and arrays
- **Modern Standards**: Implicit none, error-checked I/O, and readable structure

## Learning Path (Modules & Examples)

| Module | Documentation | Example Code | Concept |
|--------|---------------|--------------|---------|
| 00 | `docs/00-ifort-installation.md` | - | Intel Fortran compiler setup |
| 01 | `docs/01-main-commands.md` | - | Essential Fortran commands |
| 02 | `docs/02-coding-template.md` | - | Code structure and templates |
| 03 | `docs/03-run-code.md` | - | Compilation and execution |
| 04 | - | `examples/04-coding-template.f90` | Basic program template |
| 05 | - | `examples/05-write-read-variables-types.f90` | Variable types and I/O |
| 06 | - | `examples/06-readable-code-structure.f90` | Code organization |
| 07 | - | `examples/07-do-loop.f90` | Repetition structures |
| 08 | - | `examples/08-if-then-else.f90` | Conditional statements |
| 09 | - | `examples/09-open-file.f90` | File I/O operations |
| 10 | - | `examples/10-array.f90` | Array manipulation |

## Prerequisites

- **Operating System**: Linux, macOS, or Windows
- **Intel Fortran Compiler**: Intel oneAPI Base Toolkit with HPC Toolkit
- **Alternative Compiler**: GNU Fortran (gfortran) for compatibility testing
- **Basic Programming**: Familiarity with command-line operations
- **Text Editor**: Any editor supporting Fortran syntax highlighting

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Max-Ghadri/Fortran-for-Science.git
   cd Fortran-for-Science
   ```

2. **Install Intel Fortran Compiler**:
   - Download Intel oneAPI Base Toolkit and HPC Toolkit
   - Follow the installation guide in `docs/00-ifort-installation.md`
   - Set up environment variables for your shell

3. **Verify installation**:
   ```bash
   ifort --version
   ```


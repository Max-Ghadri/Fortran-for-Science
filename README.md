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

## Build & Run

**Using Make (recommended)**:
```bash
make ex=07 run
```

**Manual compilation**:
```bash
ifort -o example examples/07-do-loop.f90
./example
```

**Alternative with gfortran**:
```bash
gfortran -o example examples/07-do-loop.f90
./example
```

## Repository Structure

```
Fortran-for-Science/
├── docs/                           # Documentation and tutorials
│   ├── 00-ifort-installation.md   # Intel Fortran setup guide
│   ├── 01-main-commands.md        # Essential Fortran commands
│   ├── 02-coding-template.md      # Code structure guidelines
│   └── 03-run-code.md             # Compilation and execution
├── examples/                       # Fortran source code examples
│   ├── 04-coding-template.f90     # Basic program template
│   ├── 05-write-read-variables-types.f90
│   ├── 06-readable-code-structure.f90
│   ├── 07-do-loop.f90
│   ├── 08-if-then-else.f90
│   ├── 09-open-file.f90
│   └── 10-array.f90
├── ifort installation/             # Installation documentation
│   └── 00_ifort_Installation-Guide.md
├── src/                           # Legacy source files (to be reorganized)
├── LICENSE                        # MIT License
└── README.md                      # This file
```

## Examples

| Example File | Concept |
|--------------|---------|
| `04-coding-template.f90` | Basic program structure and template |
| `05-write-read-variables-types.f90` | Variable types, I/O operations |
| `06-readable-code-structure.f90` | Code organization and formatting |
| `07-do-loop.f90` | Repetition structures and loops |
| `08-if-then-else.f90` | Conditional statements and logic |
| `09-open-file.f90` | File I/O operations and error handling |
| `10-array.f90` | Array declaration and manipulation |

## Coding Standards & Style

- **Implicit None**: Always use `implicit none` to prevent implicit typing
- **Variable Initialization**: Initialize all variables before use
- **Modules & Interfaces**: Use explicit interfaces for better error checking
- **Error-Checked I/O**: Always check `iostat` for file operations
- **Deterministic Filenames**: Use `trim()` and `//` for string concatenation
- **Single Purpose**: Each example demonstrates one specific concept
- **Consistent Formatting**: Use consistent indentation and spacing
- **Meaningful Names**: Use descriptive variable and function names

## Tested Compilers & Platforms

| Operating System | Intel Fortran | GNU Fortran | Status |
|------------------|---------------|-------------|---------|
| Ubuntu 20.04+ | ✅ | ✅ | Tested |
| macOS 11+ | ✅ | ✅ | Tested |
| Windows 10+ | ✅ | ✅ | Tested |
| CentOS 7+ | ✅ | ✅ | Tested |

## Continuous Integration

This repository uses GitHub Actions to automatically compile all examples with gfortran on Ubuntu runners. The CI pipeline:

- Compiles all Fortran examples in the `examples/` directory
- Runs on Ubuntu 20.04 with gfortran
- Validates that all code examples are syntactically correct
- Ensures cross-compiler compatibility

## Troubleshooting / FAQ

**Q: ifort command not found**
A: Ensure Intel oneAPI environment is sourced. Run `source /opt/intel/oneapi/setvars.sh` (Linux/macOS) or use Intel oneAPI command prompt (Windows).

**Q: Missing oneAPI environment variables**
A: Set up environment variables by sourcing the Intel oneAPI setup script or using the Intel oneAPI command prompt.

**Q: File permission errors on Linux/macOS**
A: Ensure executable permissions: `chmod +x example` after compilation.

**Q: PowerShell execution policy errors on Windows**
A: Set execution policy: `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`

**Q: Locale decimal separator issues**
A: Set locale to use period as decimal separator: `export LC_NUMERIC=C` (Linux/macOS).

**Q: Line ending issues between Windows and Unix**
A: Use `dos2unix` or `unix2dos` to convert line endings, or configure your editor to use consistent line endings.

## Roadmap

- **Derived Types**: User-defined data structures and type definitions
- **Modules & Procedures**: Modular programming and procedure interfaces
- **Array Intrinsics**: Advanced array operations and built-in functions
- **Error Handling**: Comprehensive error checking and exception handling
- **Unit Tests**: Automated testing framework for examples

## Contributing

Contributions are welcome! Please follow these guidelines:

- **Pull Requests**: Submit PRs for new examples or documentation improvements
- **One Concept Per Example**: Each example should demonstrate a single, clear concept
- **Clear Comments**: Include comprehensive comments explaining the code
- **Testing**: Ensure examples compile with both ifort and gfortran
- **Documentation**: Update relevant documentation when adding new examples




<div align="center">
    <img src="images/Fortran_logo.png" alt="FORTRAN Banner" width="30%">
</div>



<h1 align="center">Fortran for Science</h1>

A hands-on Modern Fortran tutorial with Intel Fortran (ifort) featuring clean workflow, consistent coding templates, and minimal runnable examples for scientific computing.

---
***Table of Contents***
---
<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#overview"><i><b>1. Overview</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#key-features"><i><b>2. Key Features</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#learning-path-modules--examples"><i><b>3. Learning Path (Modules & Examples)</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#prerequisites"><i><b>4. Prerequisites</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#installation"><i><b>5. Installation</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#build--run"><i><b>6. Build & Run</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#repository-structure"><i><b>7. Repository Structure</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#examples"><i><b>8. Examples</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#coding-standards--style"><i><b>9. Coding Standards & Style</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#tested-compilers--platforms"><i><b>10. Tested Compilers & Platforms</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#continuous-integration"><i><b>11. Continuous Integration</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#troubleshooting--faq"><i><b>12. Troubleshooting / FAQ</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#roadmap"><i><b>13. Roadmap</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#contributing"><i><b>14. Contributing</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#contact"><i><b>15. Contact</b></i></a>
</div>
&nbsp;
---

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
| 0 | `ifort installation/ifort_Installation-Guide.md` | - | Intel Fortran compiler setup |
| 1 | `docs/1_FORTRAN_Main-Commands_Tutorial.md` | - | Essential Fortran commands |
| 2 | `docs/2_FORTRAN_Coding-Template_Tutorial.md` | - | Code structure and templates |
| 3 | `docs/3_FORTRAN_Run_a_Code_Tutorial.md` | - | Compilation and execution |
| 1 | - | `src/1_FORTRAN_Coding_Template.f90` | Basic program template |
| 2 | - | `src/2_Write-Read-Variables_Types.f90` | Variable types and I/O |
| 3 | - | `src/3_Readable_Code_Structure.f90` | Code organization |
| 4 | - | `src/4_do-loop.f90` | Repetition structures |
| 5 | - | `src/5_If-then-else.f90` | Conditional statements |
| 6 | - | `src/6_open-file.f90` | File I/O operations |
| 7 | - | `src/7_Array.f90` | Array manipulation |

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
   - Follow the installation guide in `ifort installation/ifort_Installation-Guide.md`
   - Set up environment variables for your shell

3. **Verify installation**:
   ```bash
   ifort --version
   ```

## Build & Run

**Using Make (recommended)**:
```bash
make ex=4 run
```

**Manual compilation**:
```bash
ifort -o example src/4_do-loop.f90
./example
```

**Alternative with gfortran**:
```bash
gfortran -o example src/4_do-loop.f90
./example
```

## Repository Structure

```
Fortran-for-Science/
├── docs/                           # Documentation and tutorials
│   ├── 1_FORTRAN_Main-Commands_Tutorial.md
│   ├── 2_FORTRAN_Coding-Template_Tutorial.md
│   └── 3_FORTRAN_Run_a_Code_Tutorial.md
├── src/                           # Fortran source code examples
│   ├── 1_FORTRAN_Coding_Template.f90
│   ├── 2_Write-Read-Variables_Types.f90
│   ├── 3_Readable_Code_Structure.f90
│   ├── 4_do-loop.f90
│   ├── 5_If-then-else.f90
│   ├── 6_open-file.f90
│   └── 7_Array.f90
├── ifort installation/             # Installation documentation
│   └── ifort_Installation-Guide.md
├── images/                        # Documentation images
│   ├── Fortran_Tutorial/          # Tutorial figures
│   └── ifort_Installation/        # Installation screenshots
├── LICENSE                        # MIT License
└── README.md                      # This file
```

## Examples

| Example File | Concept |
|--------------|---------|
| `src/1_FORTRAN_Coding_Template.f90` | Basic program structure and template |
| `src/2_Write-Read-Variables_Types.f90` | Variable types, I/O operations |
| `src/3_Readable_Code_Structure.f90` | Code organization and formatting |
| `src/4_do-loop.f90` | Repetition structures and loops |
| `src/5_If-then-else.f90` | Conditional statements and logic |
| `src/6_open-file.f90` | File I/O operations and error handling |
| `src/7_Array.f90` | Array declaration and manipulation |

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

- Compiles all Fortran examples in the `src/` directory
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



## Contact

- **Repository**: [https://github.com/Max-Ghadri/Fortran-for-Science](https://github.com/Max-Ghadri/Fortran-for-Science)
- **Issues**: [GitHub Issues](https://github.com/Max-Ghadri/Fortran-for-Science/issues)
- **Discussions**: [GitHub Discussions](https://github.com/Max-Ghadri/Fortran-for-Science/discussions)

For questions, suggestions, or contributions, please use the GitHub Issues or Discussions sections.


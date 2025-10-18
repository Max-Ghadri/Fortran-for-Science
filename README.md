

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
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#getting-started"><i><b>4. Getting Started</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#examples"><i><b>5. Examples</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#coding-standards--style"><i><b>6. Coding Standards & Style</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#continuous-integration"><i><b>7. Continuous Integration</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#roadmap"><i><b>8. Roadmap</b></i></a>
</div>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#contact"><i><b>9. Contact</b></i></a>
</div>
&nbsp;
---

# 1. About This Repository

This repository provides a comprehensive, hands-on learning path for scientists and engineers transitioning to Modern Fortran programming. It addresses the common challenge of learning Fortran through practical, executable examples that demonstrate real-world scientific computing concepts. The repository combines structured documentation with minimal, runnable code examples to create an effective learning environment that bridges theory and practice.

## 1.1. Who Is This Tutorial For?

This tutorial is designed for:
- **Scientists and Engineers**: Researchers who need to work with legacy Fortran code or develop new scientific applications
- **Graduate Students**: Those pursuing degrees in physics, engineering, mathematics, or computational sciences
- **Software Developers**: Professionals transitioning from other languages to Fortran for high-performance computing
- **Computational Researchers**: Individuals working with numerical simulations, data analysis, or scientific modeling

**Technical Expectations**: Basic familiarity with programming concepts and command-line operations. No prior Fortran experience is required, but some programming background is helpful.

## 1.2. What Will You Learn?

By completing this tutorial, you will gain:
- **Modern Fortran Fundamentals**: Understanding of Fortran 90/95/2003+ syntax and best practices
- **Scientific Computing Skills**: Practical experience with variables, arrays, loops, and file I/O operations
- **Code Organization**: How to structure Fortran programs for readability and maintainability
- **Compiler Proficiency**: Working with Intel Fortran (ifort) and GNU Fortran (gfortran) compilers
- **Error Handling**: Implementing robust I/O operations with proper error checking
- **Best Practices**: Following modern coding standards including implicit none, proper variable initialization, and clean code structure

## 1.3. Prerequisites

### For users familiar with programming but new to Fortran:
- Basic understanding of programming concepts (variables, loops, conditionals)
- Familiarity with command-line operations
- Text editor with Fortran syntax highlighting
- **Recommended starting point**: Begin with the coding template tutorial and basic variable examples

### For users experienced with Fortran but new to modern standards:
- Understanding of legacy Fortran (FORTRAN 77) concepts
- Familiarity with compilation and execution processes
- **Recommended starting point**: Focus on the modern coding standards and template sections

### For complete beginners:
- Basic computer literacy and file system navigation
- Willingness to learn command-line operations
- **Recommended starting point**: Start with the installation guide, then proceed through the tutorials in numerical order
- **Additional resources**: Consider basic programming tutorials if needed before diving into Fortran-specific concepts

## 1.4. Project Structure

```
Folder PATH listing
+---compiler installation    <-- Intel Fortran compiler setup guide
│       ifort_Installation…  <-- Detailed installation instructions
│
+---docs                     <-- Comprehensive tutorial documentation
│       1_FORTRAN_Main-Com…  <-- Essential Fortran commands
│       2_FORTRAN_Coding-T…  <-- Code structure templates
│       3_FORTRAN_Run_a_Co…  <-- Compilation and execution
│
│
+---src                      <-- Fortran source code examples
│       1_FORTRAN_Coding_T…  <-- Basic program structure
│       2_Write-Read-Varia…  <-- Variable types and I/O
│       3_Readable_Code_St…  <-- Code organization
│       4_do-loop.f90        <-- Repetition structures
│       5_If-then-else.f90   <-- Conditional statements
│       6_open-file.f90      <-- File I/O operations
│       7_Array.f90          <-- Array manipulation
│       Readme.md            <-- Source code documentation
│
│       .gitignore           <-- Git exclusions
│       LICENSE              <-- License information
│       README.md            <-- Project overview and documentation
```

# 4. Getting Started

## 4.1. Prerequisites

Before you begin, ensure you have the following software and tools installed:

- **Linux Environment**: WSL2 (Windows Subsystem for Linux) or native Linux distribution
- **Intel Fortran Compiler (ifort)**: Required for compiling and running the examples
- **Git**: For cloning the repository and version control
- **ZSH Shell**: Recommended shell with Oh My Zsh for enhanced terminal experience
- **Text Editor**: VS Code, Cursor, or any editor with Fortran syntax highlighting
- **Terminal Access**: Command-line interface for compilation and execution

### Installation Requirements
- **Intel OneAPI Base Toolkit**: Contains the Intel Fortran compiler
- **Intel OneAPI HPC Toolkit**: Contains additional high-performance computing tools
- **System Dependencies**: Git, ZSH, and basic Linux utilities

## 4.2. Quick Start

Follow these steps to get up and running with the Fortran for Science tutorial:

### 1. **Clone the Repository**
```bash
git clone https://github.com/your-username/Fortran-for-Science.git
cd Fortran-for-Science
```

### 2. **Install Intel Fortran Compiler**
Follow the detailed installation guide in the `compiler installation/` directory:
- Download and install Intel OneAPI Base Toolkit
- Download and install Intel OneAPI HPC Toolkit  
- Configure your shell environment (ZSH recommended)
- Verify installation with `ifort --version`

### 3. **Set Up Your Development Environment**
- Open the project in your preferred editor (VS Code, Cursor, etc.)
- Navigate to the `src/` directory to access Fortran source files
- Review the documentation in the `docs/` directory for learning materials

### 4. **Start Learning**
- Begin with `docs/1_FORTRAN_Main-Commands_Tutorial.md` for essential commands
- Follow the coding template tutorial: `docs/2_FORTRAN_Coding-Template_Tutorial.md`
- Learn to run code: `docs/3_FORTRAN_Run_a_Code_Tutorial.md`
- Practice with examples in the `src/` directory

### 5. **Compile and Run Examples**
```bash
# Navigate to source directory
cd src/

# Compile a Fortran program
ifort -o program_name program_name.f90

# Run the compiled program
./program_name
```

### 6. **Explore and Practice**
- Work through examples in numerical order (1_FORTRAN_Coding_Template.f90, 2_Write-Read-Variables.f90, etc.)
- Modify examples to experiment with different concepts
- Refer to the comprehensive documentation for detailed explanations

**Note**: This tutorial assumes you're working in a Linux environment. For Windows users, WSL2 is recommended for the best experience with Intel Fortran compiler.

# 9. Contact Information

For questions not addressed in the resources above, please connect with [Mostafa Rezaee](https://www.linkedin.com/in/mostafa-rezaee/) on LinkedIn for personalized assistance.


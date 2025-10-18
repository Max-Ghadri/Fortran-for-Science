

<div align="center">
    <img src="images/Fortran_logo.png" alt="FORTRAN Banner" width="30%">
</div>



<h1 align="center">Fortran for Science</h1>

***Table of Contents***
---
<details>
  <summary><a href="#1-about-this-repository"><i><b>1. About This Repository</b></i></a></summary>
  <div>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#11-who-is-this-tutorial-for">1.1. Who Is This Tutorial For?</a><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#12-what-will-you-learn">1.2. What Will You Learn?</a><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#13-prerequisites">1.3. Prerequisites</a><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#14-project-structure">1.4. Project Structure</a><br>
  </div>
</details>
&nbsp;

<details>
  <summary><a href="#2-getting-started"><i><b>2. Getting Started</b></i></a></summary>
  <div>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#21-prerequisites">2.1. Prerequisites</a><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#22-quick-start">2.2. Quick Start</a><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#23-troubleshooting">2.3. Troubleshooting</a><br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#24-next-steps">2.4. Next Steps</a><br>
  </div>
</details>
&nbsp;

<div>
  &nbsp;&nbsp;&nbsp;&nbsp;<a href="#3-contact-information"><i><b>3. Contact Information</b></i></a>
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

## 1.2. What Will You Learn?

By completing this tutorial, you will gain:
- **Modern Fortran Fundamentals**: Understanding of Fortran syntax and best practices
- **Scientific Computing Skills**: Practical experience with variables, arrays, loops, and file I/O operations
- **Code Organization**: How to structure Fortran programs for readability and maintainability
- **Compiler Proficiency**: Installing and working with Intel Fortran (ifort) compiler
- **Best Practices**: Following modern coding standards including implicit none, proper variable initialization, and clean code structure

## 1.3. Prerequisites

### For users familiar with programming but new to Fortran:
- Basic understanding of programming concepts (variables, loops, conditionals)
- Familiarity with command-line operations
- Text editor with Fortran syntax highlighting
- **Recommended starting point**: Begin with the coding template tutorial and basic variable examples

### For users experienced with Fortran but new to modern standards:
- Understanding of legacy Fortran concepts
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

# 2. Getting Started

## 2.1. Prerequisites

### System Requirements
- **Operating System**: Linux (Ubuntu 18.04+ recommended) or WSL2 on Windows
- **Architecture**: x86_64 (Intel/AMD 64-bit processors)
- **Memory**: Minimum 2GB RAM (4GB+ recommended for large computations)
- **Storage**: At least 10GB free space for Intel OneAPI installation

### Essential Software
- **Intel Fortran Compiler (ifort)**: Primary compiler for this tutorial
  - Intel OneAPI Base Toolkit (2023.1.0 or later)
  - Intel OneAPI HPC Toolkit (2023.1.0 or later)

### Additional Recommended Tools
- **Git**: Version control and repository management
- **ZSH Shell**: Enhanced shell with Oh My Zsh framework
- **Text Editor**: VS Code, Cursor, or any editor with Fortran syntax highlighting
- **Terminal**: Command-line interface for compilation and execution


### Development Environment Setup
- **VS Code Extensions**: Fortran language support, Intel OneAPI toolkit
- **Terminal Configuration**: ZSH with Oh My Zsh for enhanced productivity
- **File Permissions**: Ensure proper read/write permissions for source files

## 2.2. Quick Start

1. **Clone the Repository**
```bash
git clone https://github.com/Max-Ghadri/Fortran-for-Science.git
cd Fortran-for-Science
```

2. **Install Intel Fortran Compiler**
Follow the detailed installation guide: [`compiler installation/ifort_Installation-Guide.md`](compiler%20installation/ifort_Installation-Guide.md)

3. **Set Up Development Environment**
- Open the project in Cursor/VS Code
- Navigate to the `src/` directory to access Fortran source files
- Review the documentation in the `docs/` directory for learning materials

4. **Start Learning**
- Read the tutorials in order: [`docs/1_FORTRAN_Main-Commands_Tutorial.md`](docs/1_FORTRAN_Main-Commands_Tutorial.md), [`docs/2_FORTRAN_Coding-Template_Tutorial.md`](docs/2_FORTRAN_Coding-Template_Tutorial.md), [`docs/3_FORTRAN_Run_a_Code_Tutorial.md`](docs/3_FORTRAN_Run_a_Code_Tutorial.md)
- Practice with examples in the `src/` directory (see [`src/Readme.md`](src/Readme.md) for descriptions)

5. **Compile and Run**
```bash
cd src/
ifort -o program_name program_name.f90
./program_name
```

6. **Explore and Practice**
- Work through examples in numerical order
- Modify examples to experiment with different concepts
- Use the coding template as a starting point for new programs

## 2.3. Troubleshooting

### Common Installation Issues
- **Permission Denied**: Use `sudo` for installation commands
- **Environment Variables**: Ensure Intel OneAPI paths are properly set
- **Shell Configuration**: Restart terminal after modifying `.zshrc`

### Compilation Errors
- **Syntax Errors**: Check Fortran syntax against documentation
- **Missing Dependencies**: Verify all required libraries are installed
- **Memory Issues**: Reduce array sizes or use dynamic allocation

### Runtime Issues
- **Segmentation Fault**: Check array bounds and uninitialized variables
- **File I/O Errors**: Verify file permissions and paths
- **Performance Issues**: Use compiler optimization flags

### Getting Help
- **Documentation**: Refer to `docs/` directory for detailed explanations
- **Source Comments**: Read inline comments in example files

## 2.4. Next Steps

After completing the basic setup:
1. **Master the Coding Template**: Understand the 11-step structure
2. **Practice with Real Examples**: Work through the scientific computing example
3. **Explore Advanced Topics**: Arrays, file I/O, and optimization
4. **Build Your Own Projects**: Apply learned concepts to your research
5. **Contribute**: Share improvements and new examples with the community

**Note**: This tutorial is optimized for Linux environments. Windows users should use WSL2 for the best experience with Intel Fortran compiler and scientific computing workflows.

# 3. Contact Information

For questions not addressed in the resources above, please connect with [Mostafa Rezaee](https://www.linkedin.com/in/mostafa-rezaee/) on LinkedIn for personalized assistance.


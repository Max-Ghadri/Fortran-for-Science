

<div align="center">
    <img src="images/Fortran_logo.png" alt="FORTRAN Banner" width="30%">
</div>



<h1 align="center">Fortran for Science</h1>

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

# 4. Getting Started

## 4.1. Prerequisites

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

## 4.2. Quick Start

### Step 1: **Clone and Navigate**
```bash
# Clone the repository
git clone https://github.com/Max-Ghadri/Fortran-for-Science.git
cd Fortran-for-Science

# Verify repository structure
ls -la
```

### Step 2: **Install Intel Fortran Compiler**
Follow the comprehensive installation guide in `compiler installation/ifort_Installation-Guide.md`:

```bash
# Download Intel OneAPI Base Toolkit
wget https://registrationcenter-download.intel.com/akdlm/IRC_NAS/7deeaac4-f605-4bcf-a81b-ea7531577c61/l_BaseKit_p_2023.1.0.46401_offline.sh

# Install Base Toolkit
sudo sh ./l_BaseKit_p_2023.1.0.46401_offline.sh

# Download Intel OneAPI HPC Toolkit
wget https://registrationcenter-download.intel.com/akdlm/IRC_NAS/1ff1b38a-8218-4c53-9956-f0b264de35a4/l_HPCKit_p_2023.1.0.46346_offline.sh

# Install HPC Toolkit
sudo sh ./l_HPCKit_p_2023.1.0.46346_offline.sh

# Install ZSH and Oh My Zsh
sudo apt install git zsh -y
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"

# Configure environment
echo 'source "/opt/intel/oneapi/compiler/2023.1.0/env/vars.sh" intel64' >> ~/.zshrc
source ~/.zshrc

# Verify installation
ifort --version
```

### Step 3: **Set Up Development Environment**
```bash
# Open project in your preferred editor
code .  # For VS Code
# or
cursor .  # For Cursor

# Navigate to source directory
cd src/

# List available examples
ls -la *.f90
```

### Step 4: **Start with the Learning Path**
Follow this recommended sequence:

1. **Read Documentation** (in order):
   - `docs/1_FORTRAN_Main-Commands_Tutorial.md` - Essential Fortran commands and syntax
   - `docs/2_FORTRAN_Coding-Template_Tutorial.md` - Professional coding structure
   - `docs/3_FORTRAN_Run_a_Code_Tutorial.md` - Compilation and execution

2. **Practice with Examples** (in numerical order):
   - `1_FORTRAN_Coding_Template.f90` - Basic program structure template
   - `2_Write-Read-Variables_Types.f90` - Variable types and I/O operations
   - `3_Readable_Code_Structure.f90` - Real-world scientific computing example
   - `4_do-loop.f90` - Repetition structures and loops
   - `5_If-then-else.f90` - Conditional statements
   - `6_open-file.f90` - File I/O operations
   - `7_Array.f90` - Array manipulation and operations

### Step 5: **Compile and Run Your First Program**
```bash
# Navigate to source directory
cd src/

# Compile the coding template
ifort -o template 1_FORTRAN_Coding_Template.f90

# Run the program
./template

# Compile with optimization flags
ifort -O2 -o template_optimized 1_FORTRAN_Coding_Template.f90

# Run with timing
time ./template_optimized
```

### Step 6: **Advanced Compilation Options**
```bash
# Compile with debugging information
ifort -g -o program_debug program.f90

# Compile with maximum optimization
ifort -O3 -ipo -xHost -o program_fast program.f90

# Compile with specific Fortran standard
ifort -std=f2008 -o program_modern program.f90

# Compile with OpenMP support
ifort -qopenmp -o program_parallel program.f90
```

### Step 7: **Explore and Experiment**
- **Modify Examples**: Change parameters in the source files to see different outputs
- **Create New Programs**: Use the coding template as a starting point
- **Test Different Compilers**: Compare ifort with gfortran performance
- **Profile Performance**: Use timing commands to measure execution speed

## 4.3. Troubleshooting

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
- **Community**: Connect with [Mostafa Rezaee](https://www.linkedin.com/in/mostafa-rezaee/) on LinkedIn

## 4.4. Next Steps

After completing the basic setup:
1. **Master the Coding Template**: Understand the 11-step structure
2. **Practice with Real Examples**: Work through the scientific computing example
3. **Explore Advanced Topics**: Arrays, file I/O, and optimization
4. **Build Your Own Projects**: Apply learned concepts to your research
5. **Contribute**: Share improvements and new examples with the community

**Note**: This tutorial is optimized for Linux environments. Windows users should use WSL2 for the best experience with Intel Fortran compiler and scientific computing workflows.

# 9. Contact Information

For questions not addressed in the resources above, please connect with [Mostafa Rezaee](https://www.linkedin.com/in/mostafa-rezaee/) on LinkedIn for personalized assistance.


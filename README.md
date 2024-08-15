# install-abaqus-with-fortran-on-windows
This is a tutorial of installing **ABAQUS 2023** with **intel Fortran Compiler 2023 (intel oneAPI HPC toolkit 2023)** on Windows and link them for user subroutine. This guide should also work for Abaqus 2024 and later version (changing accordingly file names and paths), although I haven't tested it.

For more information on install **ABAQUS 2023** with **ifort 2021** on ubuntu 22.04, please visit https://github.com/Yazhuo-Liu/install-abaqus-on-ubuntu

Note: 
1. The version difference between **intel oneAPI** and **ABAQUS** should not be too large, otherwise there will be compatibility problems
2. To successfully follow this tutorial, you need to have administrator access

## References:
- https://visualstudio.microsoft.com/vs/
- https://www.intel.com/content/www/us/en/developer/articles/tool/oneapi-standalone-components.html
- https://www.bilibili.com/video/BV16W4y1y7YH

## 1. Install ABAQUS 2023
- There is a student free version that can be downloaded from https://www.3ds.com/edu/education/students/solutions/abaqus-le
- The installation instructions can be find on https://github.com/Yazhuo-Liu/install-abaqus-on-ubuntu/blob/main/SIMULIA_Installation_Instructions.pdf
- 

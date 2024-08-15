# install-abaqus-with-fortran-on-windows
This is a tutorial of installing **ABAQUS 2023** with **Visual Studio Community 2019** and **intel Fortran Compiler 2023 (intel oneAPI HPC toolkit 2023)** on Windows and link them for user subroutine. This guide should also work for Abaqus 2024 and later version (changing accordingly file names and paths), although I haven't tested it.

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
- The installation instructions can be find [here](https://github.com/Yazhuo-Liu/install-abaqus-with-fortran-on-windows/blob/main/ABAQUS_Installation_Instructions.pdf)
- Abaqus CAA API component is required for running fortran subroutine

## 2.	Install visual studio community 2019 (must before intel oneAPI)
- The visual studio community 2019 installer is already uploaded in [this repository](https://github.com/Yazhuo-Liu/install-abaqus-with-fortran-on-windows/blob/main/Visual%20Studio%20community%202019.exe)
- Download it and	run as administrator
  ![image](https://github.com/user-attachments/assets/e860d9e5-bf2f-4b2b-8580-ca49208d9fcc)
- Under the Workloads view, select the checkbox to install the **Desktop development with C++**, then install
  ![image](https://github.com/user-attachments/assets/b9608860-e96e-4cca-b5e9-22a3d2908468)
- Finish the installation
  ![image](https://github.com/user-attachments/assets/d7706635-bf61-4018-a5e6-20a43d0902bf)
- launch visual studio community 2019, make sure it is installed correctly (skip the sign in process)
  ![image](https://github.com/user-attachments/assets/4d947f3a-a7de-47bd-be3d-148f53c8c2db)
  ![image](https://github.com/user-attachments/assets/7f146b7b-ac09-452d-90d6-93daaf3eb070)

## 3. Install intel Fortran Compiler 2023 (intel oneAPI HPC toolkit 2023)
- The intel oneAPI HPC toolkit 2023 installer is already uploaded in [this repository](https://github.com/Yazhuo-Liu/install-abaqus-with-fortran-on-windows/blob/main/w_HPCKit_p_2023.1.0.46357.exe)
- The later version of intel Fortran Compiler can be download from [here](https://www.intel.com/content/www/us/en/developer/articles/tool/oneapi-standalone-components.html). Do NOT use later version of intel Fortran Compiler with Abaqus2023, because it may induce some competability issues.
  ![image](https://github.com/user-attachments/assets/bfbd6a80-ad84-43ba-86a2-38c224dd9021)
- Download intel oneAPI HPC toolkit 2023 installer and run as administrator
  ![image](https://github.com/user-attachments/assets/bbabd55a-9649-4a2b-8799-d5387deb30cd)
- Using the default installation location and custom installation
  ![image](https://github.com/user-attachments/assets/daddccd4-d559-4fa5-84f4-e0683143e699)
- Only select **intel Fortran Compiler & intel Fortran Compiler classic**
  ![image](https://github.com/user-attachments/assets/12ab7d86-c7ce-41e4-9750-2c40c060eb0b)
- Ignore the worning massage
  ![image](https://github.com/user-attachments/assets/12787b0b-475d-4b2f-a111-61bfb959fdef)
- Integrate Fortran with visual studio community 2019
  ![image](https://github.com/user-attachments/assets/f5cca5c7-56a1-49fa-9dc3-dd53ae87ee12)


  
  

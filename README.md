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
- Download [intel oneAPI HPC toolkit 2023 installer](https://github.com/Yazhuo-Liu/install-abaqus-with-fortran-on-windows/blob/main/w_HPCKit_p_2023.1.0.46357.exe) and run as administrator
  ![image](https://github.com/user-attachments/assets/bbabd55a-9649-4a2b-8799-d5387deb30cd)
- Using the default installation location and custom installation
  ![image](https://github.com/user-attachments/assets/daddccd4-d559-4fa5-84f4-e0683143e699)
- Only select **intel Fortran Compiler & intel Fortran Compiler classic**
  ![image](https://github.com/user-attachments/assets/12ab7d86-c7ce-41e4-9750-2c40c060eb0b)
- Ignore the warning massage
  ![image](https://github.com/user-attachments/assets/12787b0b-475d-4b2f-a111-61bfb959fdef)
- Integrate Fortran with visual studio community 2019
  ![image](https://github.com/user-attachments/assets/f5cca5c7-56a1-49fa-9dc3-dd53ae87ee12)
- Do not consent to collection of your information
  ![image](https://github.com/user-attachments/assets/340607f2-7e17-47c3-aee6-e1804e567167)
- Waiting the installation to be finished
  ![image](https://github.com/user-attachments/assets/46aca69e-b925-4335-b05e-9c6cd77bfc7b)

## 4. Link Fortran Compiler with ABAQUS
- Go to the folder “C:\Program Files (x86)\Intel\oneAPI\compiler\2023.1.0\env”. (Replace “2023.1.0” by your version of oneAPI if you use different version of fortran)
- Find the file named “vars.bat”. View the properties of the file and copy its location.
  ![image](https://github.com/user-attachments/assets/965dc2ce-0ad2-44e0-9337-cc46bb8db695)
- Create a new txt file, type “call” with a space. Enter two double quotes and paste the path you just copied into the double quotes. Then add the file name into the double quotes. Make sure the path target to the “vars.bat” file. Outside the double quotes, just follow by a space and “intel64 vs2019”.
  ![image](https://github.com/user-attachments/assets/411096b3-2aca-4015-81e3-fa814f512e01)
- Copy this line
- Go to the folder “C:\SIMULIA\Commands” and find the file named “abq2023.bat”. Edit the file. Paste the copied line to the beginning of the file. Then save the file (You need the administrator access to save the file).
  ![image](https://github.com/user-attachments/assets/8b739da8-e2d1-4429-b01f-0dbe464eaca2)
- Launch Abaqus CAE to check if it is functional.

## 5. Run Abaqus Vrification. 
- You can find Abaqus Vrification in the start menu.
  ![image](https://github.com/user-attachments/assets/cef40422-aae2-49dd-8a49-4fb787cc1e6f)
- Launch Abaqus Vrification, the first five test must be PASS
  ![image](https://github.com/user-attachments/assets/597737d7-6a58-4c04-875d-2500903c715f)
- If **YES**, **CONGRATULATIONS!**
- You successfully finish the installation process.
  
  

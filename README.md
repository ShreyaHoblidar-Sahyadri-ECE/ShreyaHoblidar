# RISCV INTERNSHIP PROGRAM POWERED BY SAMSUNG 
This RISC-V Internship using VSDSquadron Mini is designed around the RISC-V architecture and makes use of open-source tools to educate students on VLSI SoC Design and RISC-V. The program is mentored by Kunal Ghosh, Founder of VSD.


- **Name:** Shreya Hoblidar 
- **College:** Sahyadri College of Engineering and Management, Mangaluru - 575007  
- **Email:** [shreya.ec22@sahyadri.edu.in](mailto:shreya.ec22@sahyadri.edu.in)  
- **GitHub Profile:** [ShreyaHoblidar-Sahyadri-ECE](https://github.com/ShreyaHoblidar-Sahyadri-ECE)  
- **LinkedIn Profile:** [Shreya Hoblidar](https://www.linkedin.com/in/shreyahoblidar/)

# Task 1: Summation Program in C on Ubuntu

This task demonstrates writing, compiling, and executing a C program to calculate the summation of numbers from 1 to `n`. The program was executed in an Ubuntu environment, and additional configurations for RISC-V compilation were explored.

---

## Steps Performed

### 1. **Installing Text Editor (`leafpad`)**
- Attempted to open a file using the `leafpad` text editor.
- The command `leafpad` was not found, so it was installed using:
  ```bash
  sudo apt install leafpad

![Installing Text Editor](https://github.com/ShreyaHoblidar-Sahyadri-ECE/ShreyaHoblidar/blob/6d8a613923f4dcdb28f42944381870f95b76b432/Task1/task%201.png)

### 2. **Write the C program***
```bash
  leafpad sum1ton.c
```
![C Program code](https://github.com/ShreyaHoblidar-Sahyadri-ECE/ShreyaHoblidar/blob/e49b71ae766534af43542706462726dfcff2fac5/Task1/task11.png)

### 3.Compile and run the program:
```bash
gcc sum1ton.c
./a.out
```
### 4.Cross-compile for RISC-V:***
-Install riscv64-unknown-elf-gcc.
-Use the following command to compile:
```bash
 riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
```
-Verify the object file:
```bash
ls -ltr sum1ton.o
```
![Screenshot 3](https://github.com/ShreyaHoblidar-Sahyadri-ECE/ShreyaHoblidar/blob/c575a7a47de52a4622779829d5055f15e6648b63/Task1/task01.png)
![Screenshot 4](https://github.com/ShreyaHoblidar-Sahyadri-ECE/ShreyaHoblidar/blob/95288b8154562f58a43bc94a63d45badede232e8/Task1/task111.png)
![Screenshot 5](https://github.com/ShreyaHoblidar-Sahyadri-ECE/ShreyaHoblidar/blob/7c449bece1095d4c13b83986f9fcd41a5d74fda1/Task1/task1111.png)




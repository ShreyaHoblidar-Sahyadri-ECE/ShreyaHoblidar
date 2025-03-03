# RISCV INTERNSHIP PROGRAM POWERED BY SAMSUNG 
This RISC-V Internship using VSDSquadron Mini is designed around the RISC-V architecture and makes use of open-source tools to educate students on VLSI SoC Design and RISC-V. The program is mentored by Kunal Ghosh, Founder of VSD.


- **Name:** Shreya Hoblidar 
- **College:** Sahyadri College of Engineering and Management, Mangaluru - 575007  
- **Email:** [shreya.ec22@sahyadri.edu.in](mailto:shreya.ec22@sahyadri.edu.in)  
- **GitHub Profile:** [ShreyaHoblidar-Sahyadri-ECE](https://github.com/ShreyaHoblidar-Sahyadri-ECE)  
- **LinkedIn Profile:** [Shreya Hoblidar](https://www.linkedin.com/in/shreyahoblidar/)

# Task 1
<details>
<summary> Task 1: Summation Program in C on Ubuntu

This task demonstrates writing, compiling, and executing a C program to calculate the summation of numbers from 1 to `n`. The program was executed in an Ubuntu environment, and additional configurations for RISC-V compilation were explored.

</summary>
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
### 4.Cross-compile for RISC-V:
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
</details>

# Task 2:
<details>
  <summary> Task 2: Spike Simulation

-This repository provides a detailed demonstration of compiling and simulating C code for the RISC-V architecture using the RISC-V GCC compiler and SPIKE simulator. It specifically focuses on comparing the performance of compiled programs with different compiler optimization flags (-O1 and -Ofast).
</summary>

### Objective
- Understand how to compile a simple C program for the RISC-V architecture.
- Use RISC-V GCC to compile the program with different optimization levels (-O1 and -Ofast).
- Analyze the performance of the program using the SPIKE simulator.
- Compare the assembly output and program execution flow with different optimization levels.

###  Compile Using RISC-V GCC
- The C program is compiled using the riscv64-unknown-elf-gcc compiler. The target architecture is rv64i (64-bit RISC-V) and the ABI is lp64.

- Compile with -O1 Optimization:
To compile with basic optimization (-O1), use the following command:
```bash
 riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o swift.o swift.c
```
### Disassemble Object File:
- To view the assembly code generated by the compiler, use the following command:
 ```bash
riscv64-unknown-elf-objdump -d swift.o
```
- We can also minimize the output for easier reading:
  ```bash
   riscv64-unknown-elf-objdump -d swift.o | less

![Screenshot 1](https://github.com/ShreyaHoblidar-Sahyadri-ECE/ShreyaHoblidar/blob/675ffc0eaa81ebd3ee3de85fb6412c27552b5dcf/Task2/1.jpg)

### Run SPIKE Simulation
- To simulate the compiled RISC-V program in non-debug mode, use the following command:
  ```bash
  spike pk swift.o
  
</details>

# Task 5
<details>
 <summary>  Smart Dual-Sensor Security Alarm System using the VSDSquadron Mini, an ultrasonic sensor, an IR sensor, two buzzers, and an LED. This code continuously monitors the surroundings, and if an object is detected, the buzzers beep and the LED turns ON. The system resets automatically when no object is detected.</summary>

 # Smart Dual-Sensor Security Alarm System

## Overview
This project is a Smart Dual-Sensor Security Alarm System that continuously monitors for intruders using both an ultrasonic sensor and an IR sensor. If any object is detected within a predefined range, the system will activate two buzzers as an alarm and turn on an LED as a visual warning. The system runs automatically without requiring any manual activation or push button.

### Key Features:
- Automated Intruder Detection: Uses both an ultrasonic sensor and an IR sensor to detect objects.
- Dual-Stage Alert System:
  If an object is detected by either sensor, the LED turns ON and both buzzers sound an alarm.
- Continuous Monitoring: The system runs 24/7 without needing manual activation.
- Versatile Applications: Can be used for home security, restricted area monitoring, or smart door alarms.
  
## Components Required
- *VSD Squadron Mini*
- *Ultrasonic Sensor* 
- LED* (to display the output)
- *Breadboard*
- *IR Sensor*
- *Jumper wires*
- *VS Code* (for software development)
- *PlatformIO* (multi-framework professional IDE)

## How It Works
- The system continuously monitors the surroundings.
- If the ultrasonic sensor detects an object within 20 cm, it triggers the alarm.
- If the IR sensor detects movement or an object, it also triggers the alarm.
- When an intruder is detected, both buzzers will beep repeatedly, and the LED will turn ON.
- The alarm stops when no object is detected by both sensors.

![Circuit diagram](https://github.com/ShreyaHoblidar-Sahyadri-ECE/ShreyaHoblidar/blob/f7d95860f3624a8e3ceb19f0e193f6286c06e0f4/Task%205/duoble_smart.png)

### Code
# Working of code
- Initial Setup:
Configures GPIO pins for LED, buzzers, ultrasonic sensor, and IR sensor.
The LED and buzzers are initially off.

-Continuous Monitoring:
The system constantly checks for objects using ultrasonic and IR sensors.
The ultrasonic sensor measures distance and returns the value in centimeters.
The IR sensor detects nearby objects (it outputs LOW when something is detected).
Alarm Activation:
If the distance is less than 20 cm or the IR sensor detects an object, the LED turns ON and both buzzers beep in a pattern.

-Alarm Deactivation:
If no object is detected, the LED and buzzers remain OFF.

## Program
``` bash
#include <ch32v00x.h>

void Delay_us(uint32_t us) {
    for (uint32_t i = 0; i < (us * 8); i++) {
        __NOP();
    }
}

void Delay_ms(uint32_t ms) {
    for (uint32_t i = 0; i < (ms * 8000); i++) {
        __NOP();
    }
}

void GPIO_Config(void) {
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA | RCC_APB2Periph_GPIOC, ENABLE);

    GPIO_InitTypeDef GPIO_InitStructure = {0};

    // IR Sensor (PC0 - Input)
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_0;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IN_FLOATING;
    GPIO_Init(GPIOC, &GPIO_InitStructure);

    // Ultrasonic TRIG (PA1 - Output)
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_1;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init(GPIOA, &GPIO_InitStructure);

    // Ultrasonic ECHO (PA2 - Input)
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_2;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IN_FLOATING;
    GPIO_Init(GPIOA, &GPIO_InitStructure);

    // Buzzer (PC1 - Output)
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_1;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_Init(GPIOC, &GPIO_InitStructure);

    // LED (PC2 - Output)
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_2;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_Init(GPIOC, &GPIO_InitStructure);
}

uint16_t MeasureDistance() {
    uint32_t time = 0;
    uint32_t timeout = 300000;  // Prevent infinite loop

    // Send Trigger pulse (10µs)
    GPIO_WriteBit(GPIOA, GPIO_Pin_1, RESET);
    Delay_us(2);
    GPIO_WriteBit(GPIOA, GPIO_Pin_1, SET);
    Delay_us(10);
    GPIO_WriteBit(GPIOA, GPIO_Pin_1, RESET);

    // Wait for Echo HIGH
    while (GPIO_ReadInputDataBit(GPIOA, GPIO_Pin_2) == 0 && timeout--);
    if (timeout == 0) return 999; // Timeout: No object detected

    timeout = 300000;  // Reset timeout
    while (GPIO_ReadInputDataBit(GPIOA, GPIO_Pin_2) == 1 && timeout--) {
        time++;
    }
    if (timeout == 0) return 999; // Timeout: No object detected

    return (time / 58); // Convert to cm (Integer calculation)
}

int main(void) {
    SystemCoreClockUpdate();
    GPIO_Config();
    Delay_ms(500);  // Stabilization delay

    while (1) {
        uint8_t ir_status = GPIO_ReadInputDataBit(GPIOC, GPIO_Pin_0); // IR Sensor
        uint16_t distance = MeasureDistance();

        // IR Sensor → Controls Buzzer
        if (ir_status == 0) {
            GPIO_WriteBit(GPIOC, GPIO_Pin_1, SET);  // Buzzer ON
        } else {
            GPIO_WriteBit(GPIOC, GPIO_Pin_1, RESET); // Buzzer OFF
        }

        // Ultrasonic Sensor → Controls LED
        if (distance < 10) {  
            GPIO_WriteBit(GPIOC, GPIO_Pin_2, SET);  // LED ON
        } else {
            GPIO_WriteBit(GPIOC, GPIO_Pin_2, RESET); // LED OFF
        }

        Delay_ms(100);
    }
}

```
# Project Applications:
-  Smart Door Alarm – Detects if someone is near.
-  Obstacle Avoidance System – Used in robotics.
-  Blind Assistance Device – Alerts users when objects are close.

  </details>











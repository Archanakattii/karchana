# As per the Update given for the next task "Should Use the RISC-V Core Verilog netlist and testbench for functional Simulation.
# Veriog code is being executed and the waveforms are generated using the gtkwave

# Aim: To verify the Functional Simulation:-
# Table of contents
- [1.RISC-V RV32I](#1-RISC-V-RV32I)
 - [2.BLOCK DIAGRAM OF RISC-V RV32I](#2-BLOCK-DIAGRAM-OF-RISC-V-RV32I)
 - [3.INSTRUCTION SET OF RISC-V RV32I](#3-INSTRUCTION-SET-OF-RISC-V-RV32I)
 - [4.FUNCTIONAL SIMULATION](#4-FUNCTIONAL-SIMULATION)
    - [4.1 About iverilog and gtkwave](#41-About-iverilog-and-gtkwave)
    - [4.2 Installing iverilog and gtkwave](#42-Installing-iverilog-and-gtkwave)
    - [4.3 The output waveform](#43-The-output-waveform)
  
   ## 1. RISC-V RV32I

This project provides an insight into the working of a few important instructions of the instruction set of a Single cycle Reduced Instruction Set Computer - Five(RISC-V) Instruction Set Architecture suitable for use across wide-spectrum of Applications from low-power embedded devices to high-performance Cloud-based Server processors. The base RISC-V is a 32-bit processor with 31 general-purpose registers, so all the instructions are 32-bit long. Some Applications where the RISC-V processors have begun to make some significant threads are in Artificial intelligence and machine learning, Embedded systems, ultra-low power processing systems, etc.

## 2. BLOCK DIAGRAM OF RISC-V RV32I
![WhatsApp Image 2024-03-05 at 6 16 12 AM](https://github.com/Archanakattii/karchana/assets/160317292/2c9af464-8223-4f66-bdd9-173882837b3b)


## 3. INSTRUCTION SET OF RISC-V RV32I
![WhatsApp Image 2024-03-05 at 6 16 12 AM (1)](https://github.com/Archanakattii/karchana/assets/160317292/bfb10f5d-aaea-4c4b-80e2-3568888b7250)


![WhatsApp Image 2024-03-05 at 6 16 12 AM (2)](https://github.com/Archanakattii/karchana/assets/160317292/fdfa7c31-f3d4-4876-8567-fa0a8862c904)

## 4. FUNCTIONAL SIMULATION

### 4.1 About iverilog and gtkwave
- Icarus Verilog is an implementation of the Verilog hardware description language.
- GTKWave is a fully featured GTK+ v1. 2 based wave viewer for Unix and Win32 which reads Ver Structural Verilog Compiler generated AET files as well as standard Verilog VCD/EVCD files and allows their viewing.
  
### 4.2 Installing iverilog and gtkwave

- **For Ubuntu**
- **To clone the repository and download the netlist files for simulation, enter the following commands in your terminal.**

 ```
 $ git clone https://github.com/Archanakattii/karchana
 $ cd hello
```
 Open your terminal and type the following to install iverilog and GTKWave
 ```
 $   sudo apt get update
 $   sudo apt get install iverilog gtkwave
 ```
![WhatsApp Image 2024-03-05 at 6 12 30 AM](https://github.com/Archanakattii/karchana/assets/160317292/1ba2ae13-3ddb-4f74-a9d1-399a44c2746d)

![WhatsApp Image 2024-03-05 at 6 12 30 AM (1)](https://github.com/Archanakattii/karchana/assets/160317292/8ddea395-1e90-4de1-9eac-cb24365bd443)





- **To simulate and run the Verilog code, enter the following commands in your terminal.**

```
$ iverilog -o hello hello.v hello_tb.v
$ ./hello
```
![WhatsApp Image 2024-03-05 at 6 12 32 AM](https://github.com/Archanakattii/karchana/assets/160317292/92244e3d-0db1-42c4-81e3-81bcbcb5a763)


- **To see the output waveform in gtkwave, enter the following commands in your terminal.**

`$ gtkwave hello.vcd`

![WhatsApp Image 2024-03-05 at 6 12 33 AM](https://github.com/Archanakattii/karchana/assets/160317292/1c3b02bc-b1db-4834-9827-45f106237ca7)


### 4.3 The output waveform

 The output waveform showing the instructions performed in a 5-stage pipelined architecture.
 
 Instruction 1:add r6,r2,r1
 ![WhatsApp Image 2024-03-05 at 6 16 13 AM](https://github.com/Archanakattii/karchana/assets/160317292/4a8f457c-9902-4c78-b438-e1aeaf26bc6d)

 Instruction 2:sub r7,r1,r2
 ![WhatsApp Image 2024-03-05 at 6 16 13 AM (1)](https://github.com/Archanakattii/karchana/assets/160317292/ba37cf98-19f0-4ae7-ac4a-cd7227d8a900)

Instruction 3:and r8,r1,r3
![WhatsApp Image 2024-03-05 at 6 16 13 AM (2)](https://github.com/Archanakattii/karchana/assets/160317292/ced41569-fb74-4bee-8405-3fefa8688951)


Instruction 4:or r9,r2,r5
![WhatsApp Image 2024-03-05 at 6 16 14 AM](https://github.com/Archanakattii/karchana/assets/160317292/bf079638-7e2f-44c8-b40b-d0a970ebd783)


 Instruction 5:xor r10,r1,r4
![WhatsApp Image 2024-03-05 at 6 16 14 AM (1)](https://github.com/Archanakattii/karchana/assets/160317292/996dd2d4-968a-406a-a19a-995e8a970366)


 Instruction 6:slt r11,r2,r4
![WhatsApp Image 2024-03-05 at 6 16 14 AM (2)](https://github.com/Archanakattii/karchana/assets/160317292/3d62eb93-39b6-40e3-b71d-9b69f5e6a1d2)


 Instruction 7:addi r12,r4,5
![WhatsApp Image 2024-03-05 at 6 16 15 AM](https://github.com/Archanakattii/karchana/assets/160317292/e805e506-c35d-4db6-aa77-064d222cb203)

 Instruction 8:sw r3,r1,2
 ![WhatsApp Image 2024-03-05 at 6 16 15 AM (1)](https://github.com/Archanakattii/karchana/assets/160317292/5941c111-993e-4672-991c-aaf32e7a8c60)

 Instruction 9:lw r13,r1,2
![WhatsApp Image 2024-03-05 at 6 16 16 AM](https://github.com/Archanakattii/karchana/assets/160317292/a23d04d3-eaec-4ea7-9ec2-0912272f55ec)

 Instruction 10:beq r0,r0,15
 ![WhatsApp Image 2024-03-05 at 6 16 16 AM (1)](https://github.com/Archanakattii/karchana/assets/160317292/2e1be942-ddd4-48fc-897e-934d2973fc67)

 After branching, performing
 Instruction 11:add r14,r2,r2
 ![WhatsApp Image 2024-03-05 at 6 16 16 AM (1)](https://github.com/Archanakattii/karchana/assets/160317292/80cb6bf1-3f87-4cc4-85a1-276f306a04b1)


  Full 5-stage instruction pipeline and pc-increment description Waveform
  
![WhatsApp Image 2024-03-05 at 6 16 16 AM (2)](https://github.com/Archanakattii/karchana/assets/160317292/7bac3c18-fd58-48ae-824c-99c0d28a8867)

![WhatsApp Image 2024-03-05 at 6 12 35 AM](https://github.com/Archanakattii/karchana/assets/160317292/f7db13a8-273a-44de-874d-563159f9cac2)


![WhatsApp Image 2024-03-05 at 6 12 31 AM](https://github.com/Archanakattii/karchana/assets/160317292/8b72d733-be71-45d7-8961-49b096b28067)




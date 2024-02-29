# **The C code should undergo the simulation of normal GCC X86 Compiler and riscv compiler** (**SPIKE Simulation**) 

**AS PER THE REQUIREMENT OUTPUT OF GCC (F1) SHOULD BE EQUAL = TO OUTPUT OF RISCV GCC (F2)**



![WhatsApp Image 2024-02-29 at 6 48 23 AM](https://github.com/Archanakattii/karchana/assets/160317292/05299edb-f7ce-4fd2-8339-ef91b958b141)

**Step - 1**: To Run the code in the normal GCC Compiler</p>


  To compile the code: 
            
        gcc sum1ton.c -o sum1ton
   To Get the output use:
       
       ./a.out
  Here the output finds to be -Sum of numbers from 1 to 250 is 31375

![WhatsApp Image 2024-02-29 at 6 35 03 AM](https://github.com/Archanakattii/karchana/assets/160317292/bc0abc7f-3e35-4a23-82e0-1f533783a070)

**Step - 2**: To Run the code in the RISC-V GCC Compiler</p>
To compile the code :</p>

    riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
    gcc sum1ton.c -o sum1ton
    ./sum1ton
 Here the output finds to be -Sum of numbers from 1 to 250 is 31375</p>
  ![WhatsApp Image 2024-02-29 at 6 35 03 AM (1)](https://github.com/Archanakattii/karchana/assets/160317292/b35b8551-2682-4524-be3f-91cafd1bf1e6)
 To compile the code:
  
    riscv64-unknown-elf-gcc -o sum1ton sum1ton.c
  or
    
    riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
  or

    riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
 (by referring the image given below) </p>
 To Get the output use:

    ./a.out
 Here the output also finds to be -Sum of numbers from 1 to 250 is 31375

 
![WhatsApp Image 2024-02-29 at 6 35 03 AM (2)](https://github.com/Archanakattii/karchana/assets/160317292/c7007336-28e9-43f5-8ed0-ff66a89794e0)


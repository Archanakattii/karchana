# karchana
# **A 4-week Research Internship on RISC-V using VSDSquadron Mini RISC-V Dev Board**</p>

![Screenshot 2024-02-24 221803](https://github.com/Archanakattii/karchana/assets/160317292/e18ec90d-90da-4bcb-8a79-f64cbab322be)</p>
**CH32V003F4U6 chip with 32-bit RISC-V core based on RV32EC instruction set**</p>
<details>
<summary><b>TASK 1:</p>
</b></summary>
1.To install RISC-V GNU Tool chain </p>
  
    sudo apt install git-all  
    sudo apt-get install autoconf automake autotools-dev curl python3 libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev</p>
    git clone https://github.com/riscv/riscv-gnu-toolchain</p>
![WhatsApp Image 2024-02-20 at 5 26 03 PM](https://github.com/Archanakattii/karchana/assets/160317292/2a265643-d661-4a6a-babf-23f62a907f10)


![WhatsApp Image 2024-02-20 at 5 26 02 PM (2)](https://github.com/Archanakattii/karchana/assets/160317292/5f7e8e8f-57b3-4915-8b6a-d265b292d2c9)


![WhatsApp Image 2024-02-20 at 5 26 02 PM](https://github.com/Archanakattii/karchana/assets/160317292/f4369646-3762-4821-998e-ca4f17e5008e)

2.To install Yosys</p>

    git clone https://github.com/YosysHQ/yosys.git
    cd yosys 
    sudo apt-get install build-essential clang bison flex \libreadline-dev gawk tcl-dev libffi-dev git \ graphviz xdot pkg-config python3 libboost-system-dev\libboost-python-dev libboost-filesystem-dev zlib1g-dev
    sudo apt-get install tcl-dev
    sudo apt-get install libreadline-dev
    make config-gcc
    make 
    sudo make install

![WhatsApp Image 2024-02-20 at 5 26 01 PM (2)](https://github.com/Archanakattii/karchana/assets/160317292/74db1bcc-b5b5-4c90-8f0e-b6f4acc77c3d)
![WhatsApp Image 2024-02-20 at 5 26 01 PM (1)](https://github.com/Archanakattii/karchana/assets/160317292/5e37c28e-a048-4d18-b1f4-53fe4edf3375)

![WhatsApp Image 2024-02-20 at 5 26 00 PM (3)](https://github.com/Archanakattii/karchana/assets/160317292/3a2c62e6-c728-45d9-93d7-e9ed310b2232)


3.To install iverilog and gtkwave</p>

    sudo apt-get install iverilog
    sudo apt update
    sudo apt-get install gtkwave
![WhatsApp Image 2024-02-20 at 5 26 00 PM (2)](https://github.com/Archanakattii/karchana/assets/160317292/274ffcf3-ea84-467c-b80a-9ea3d72c3955)
![WhatsApp Image 2024-02-20 at 5 26 00 PM (1)](https://github.com/Archanakattii/karchana/assets/160317292/327420c5-1fb8-4f5d-be1d-b1e6f13b5cac)
![WhatsApp Image 2024-02-20 at 5 26 00 PM](https://github.com/Archanakattii/karchana/assets/160317292/a4ce0873-5d00-4c5a-bd59-b28e64ddceb3)

</details>

<details>
  
<summary><b>TASK 2:</p>
</b></summary>

# **Various types of RISC-V instructions**
RISC-V instructions are encoded using a fixed-length 32-bit format, which simplifies decoding and execution. The instruction formats are categorized into six types: R, I, S, B, U, and J. Each format serves a specific purpose and has a unique encoding structure
<details>
<summary><b>R-type instructions:
</b></summary>
<br>
The r-type instruction format, which is used to execute arithmetic and logical instructions. The first field in the r-type instruction format is called the opcode field, which is also known as the operation code. 

  Eg:-add rd, rs1, rs2: Add contents of registers rs1 and rs2 and store result in rd</p>
  </details>
<details>
<summary><b>I-type instructions:
</b></summary>
<br>
I-type instructions for immediate and load operations. They include two register operands and a 12-bit immediate value. 
  
  Eg:-addi rd, rs1, imm: Add immediate value to contents of register rs1 and store result in rd.</p>
  </details>
<details>
<summary><b>S-type instructions:
</b></summary>
<br>
S-Type instructions are primarily used for storing data from a register to memory. They operate on a 12-bit immediate value (offset) and use two source registers (rs1 and rs2) to calculate the memory address where the data will be stored.
  
  Eg:-sb rs2, offset(rs1): Store the least significant byte of rs2 at the memory address computed by adding rs1 and offset.</p>
  </details>
<details>
<summary><b>B-type instructions:
</b></summary>
<br>
The B-Type instructions in the RISC-V architecture are branch instructions, which are used for controlling the flow of execution based on certain conditions. They perform conditional branching by comparing the contents of two registers and branching if the condition is satisfied. 
  
  Eg:- beq (compare and label)</p>
  </details>
<details>
<summary><b>U-type instructions:
</b></summary>
<br>
The U-Type instructions in the RISC-V architecture are used for working with immediate values. They allow for the loading of 20-bit immediate values into the upper bits of a register. 
  
  Eg:- lui rd, imm: Load upper immediate - Load the immediate value shifted left by 12 bits into the most significant bits of rd.</p>
  </details>
<details>
<summary><b>J-type instructions:
</b></summary>
<br>
The J-Type instructions in the RISC-V architecture are jump instructions, which are used to change the flow of control unconditionally. They facilitate transferring the control of the program to a different memory location. 
  
  Eg:-jal rd, imm: Jump and link - Jump to the target address and store the address of the next instruction in rd.</p>
</details>

short recap:</p>

R-type instructions for register-register operations, an I-type instructions for immediate and load operations, and S-type instructions for store operations. B-type instructions for conditional branch operations. U-type instructions for long immediate and J-type instructions for unconditional jumps.</p>


# Base Instructions Format

Base instruction format 

<p align="justify">The base instruction format of RISC-V (pronounced "risk-five") is a 32-bit instruction set architecture (ISA) designed to be simple, modular, and extensible. The base instruction format consists of 32 bits divided into:

Opcode (OP): This field specifies the operation to be performed.

RD (Destination Register): This field specifies the destination register where the result of the operation will be stored. 

RS1 (Source Register 1): This field specifies the first source register operand for the operation. 

RS2 (Source Register 2): This field specifies the second source register operand for the operation. 

Immediate: This field contains an immediate value, which is a constant or operand embedded within the instruction itself. 

Funct3 and Funct7: These fields provide additional information about the operation or the specific variant of the instruction. They are typically used in conjunction with the opcode to further specify the operation or variant.</p>


![download](https://github.com/Archanakattii/karchana/assets/160317292/a073abaf-6f33-4793-8075-8f2359e42611)


# RISC-V REGISTER FILE: 


RISC-V register file</p>

 <p align="justify">The RISC-V register file is a fundamental component of the RISC-V architecture, comprising a set of general-purpose registers (GPRs) used for storing data and addresses during program execution. The RISC-V ISA defines a standard set of 32 integer registers, labeled from x0 to x31.The RISC-V register file plays a crucial role in facilitating data manipulation and control flow within RISC-V programs, offering a set of storage locations for holding essential data and addresses during program execution.</p>



</details>




<details>
<summary><b>TASK 3:</p>
</b></summary>

</details>

<details>
<summary><b>TASK 4:</p>
</b></summary>

</details>

<details>
<summary><b>TASK 5:</p>
</b></summary>

</details>

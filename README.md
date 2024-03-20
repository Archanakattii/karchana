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
  
# **By Referring to C-based Lab videos and RISC-V-based lab videos**

**Snapshots of the compiled C code and RISC-V**

**Step 1**: check whether the leafpad is installed in ur machine by using the commands
leafpad sum1ton.c & (sum1ton.c is the file name)
If the leafpad is not installed in your machine then install by using the following command

    sudo snap install leafpad
**Step 2**: Writing the C code in the leafpad editor** using the following command

    leafpad sum1ton.c &
![WhatsApp Image 2024-02-27 at 10 18 53 AM (2)](https://github.com/Archanakattii/karchana/assets/160317292/f1ec3f52-da1b-440a-bc49-bc3c56c1117c)


**Step 3**: After writing the C code save the editor by Ctrl+s

![WhatsApp Image 2024-02-27 at 10 18 53 AM (3)](https://github.com/Archanakattii/karchana/assets/160317292/26c27865-6e1b-496f-bf2b-669470dc9153)

**Step 4**: Check for the errors by using the following command(compilation step)

    gcc sum1ton.c

**Step 5**: Check the output by using the command

    ./a.out

![WhatsApp Image 2024-02-27 at 10 18 53 AM (4)](https://github.com/Archanakattii/karchana/assets/160317292/c0754b2f-3c1c-44ef-adfc-596a1444ae76)


The results will be displayed as</p> 

Sum of numbers from 1 to 250 is 31375

********************************************************RISCV Compilation and Execution*****************************************************

**Step 1: View the C Code in the editor window using the following command**

    cat sum1ton.c

![WhatsApp Image 2024-02-27 at 10 18 53 AM (5)](https://github.com/Archanakattii/karchana/assets/160317292/0ca68e17-8adc-448d-9c89-a7c9397b34e2)

**Step 2: Compile the code in riscv using the following command**

    riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c
**Step 3: The ls ltr command in Linux is used to list the contents of the current directory in long format, sorted by last modified time in reverse order.**

**use the command**

    ls -ltr sum1ton.c
![WhatsApp Image 2024-02-27 at 10 18 53 AM (7)](https://github.com/Archanakattii/karchana/assets/160317292/ef9dd175-272a-43ee-ba91-eb32ecfffb91)




**Search for the Main and check the instructions of the C code execution. It has 15 instructions in the C execution**</p>
Open new tab and type the below command to get the instuctions:

    riscv-unknown-elf-objdump -d sum1ton.o | less
![WhatsApp Image 2024-02-27 at 10 27 15 AM](https://github.com/Archanakattii/karchana/assets/160317292/f0289633-3303-4e06-b3ca-d7a8f916be40)


**Step 4:**

    riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c

![WhatsApp Image 2024-02-27 at 10 36 12 AM](https://github.com/Archanakattii/karchana/assets/160317292/63073724-f86d-4387-a4c9-7e8fdeb09482)
Type this command again

    riscv-unknown-elf-objdump -d sum1ton.o | less
![WhatsApp Image 2024-02-27 at 10 18 55 AM](https://github.com/Archanakattii/karchana/assets/160317292/3c05709d-667e-4bab-b692-b01907c069f4)


![WhatsApp Image 2024-02-27 at 10 18 53 AM (8)](https://github.com/Archanakattii/karchana/assets/160317292/b97a866d-e004-4020-8930-b67623d277c1)

</details>

<details>
<summary><b>TASK 4:</p>
</b></summary>
The code has been broken down into different parts:</p>
<details> 
<summary>They are:</p>
</summary>
1.Instruction fetch stage
  
  ![WhatsApp Image 2024-03-20 at 7 20 19 PM](https://github.com/Archanakattii/karchana/assets/160317292/906fff28-1e83-47b5-bf91-85f29cda645b)
2.Instruction Decode Stage
  ![WhatsApp Image 2024-03-20 at 7 20 19 PM (1)](https://github.com/Archanakattii/karchana/assets/160317292/0a471ef6-d6d9-4904-9e96-619375aa4f08)
3.Registers used
![WhatsApp Image 2024-03-20 at 7 20 21 PM](https://github.com/Archanakattii/karchana/assets/160317292/21e10dac-0d39-4dfe-b278-ab65fbee8c74)
4.Instructions Hardcoded
![WhatsApp Image 2024-03-20 at 7 20 19 PM (2)](https://github.com/Archanakattii/karchana/assets/160317292/69158abd-2623-4b12-b907-414ab14cb607)

</details>
  
**GTKWAVE SIMULATION **
    
    ls  #to check the contents of the folder

    iverilog archana.v archana_tb.v #to simulate the verilog code and to check the errors

    ./a.out  #to get the output and make vcd file to be ready open
after running above commands for gtkwave window to pop up type</p>
    
    gtkwave archana.vcd
![WhatsApp Image 2024-03-20 at 3 30 02 PM](https://github.com/Archanakattii/karchana/assets/160317292/f001eea0-c711-4cb7-9473-d1bf5431d025)

![WhatsApp Image 2024-03-20 at 3 21 22 PM](https://github.com/Archanakattii/karchana/assets/160317292/62ef5c85-054c-4627-aea3-52eaf621f22d)


Execution Stage with Waveforms obtained for running the gtkwave archana.vcd</p>
![WhatsApp Image 2024-03-20 at 3 21 23 PM](https://github.com/Archanakattii/karchana/assets/160317292/54ea93da-4472-4f6d-afe1-412babd0e945)

Upon adding few signals the waves can be seen
![WhatsApp Image 2024-03-20 at 3 21 23 PM (1)](https://github.com/Archanakattii/karchana/assets/160317292/010652c6-441b-480a-affe-48b33495352e)
**ADD operation:**
![WhatsApp Image 2024-03-20 at 7 44 56 PM](https://github.com/Archanakattii/karchana/assets/160317292/7c03b031-6015-4885-9bc1-9736e92cbc66)
**SUB operation:**
![WhatsApp Image 2024-03-20 at 7 47 16 PM](https://github.com/Archanakattii/karchana/assets/160317292/75d79052-b948-4283-94d4-b0f561cccec2)
**OR operation:**
![WhatsApp Image 2024-03-20 at 7 51 05 PM](https://github.com/Archanakattii/karchana/assets/160317292/71f80a5a-efe8-48e9-9010-9e0f34da4579)
**AND operation:**
![WhatsApp Image 2024-03-20 at 7 54 07 PM](https://github.com/Archanakattii/karchana/assets/160317292/0c6bb9eb-150b-4594-81ee-a4f7f6ab9fa1)
**XOR operation:**
![WhatsApp Image 2024-03-20 at 7 56 46 PM](https://github.com/Archanakattii/karchana/assets/160317292/8341be3e-a9da-414c-99df-b0d5479bfdc4)

</details>

<details>
<summary><b>TASK 5:</p>
</b></summary>
  
**GATE LEVEL SIMULATION**</p>
It should contain:</p>
1.Gatelevel netlist</p>
2.standard cell library</p>
3.Yosys Synthesis Script</p>

  ![WhatsApp Image 2024-03-20 at 3 21 23 PM (2)](https://github.com/Archanakattii/karchana/assets/160317292/cc8feb63-62d3-4469-bc75-31fb2546f0fa)
OPERATIONS:</p>
ADD operation
![WhatsApp Image 2024-03-20 at 8 15 14 PM](https://github.com/Archanakattii/karchana/assets/160317292/8c77b478-2605-482e-ad73-b27e069c3e83)
SUB operation
![WhatsApp Image 2024-03-20 at 8 17 26 PM](https://github.com/Archanakattii/karchana/assets/160317292/09a5dd82-848c-4f48-a609-e2c93d51cfee)
AND operation
![WhatsApp Image 2024-03-20 at 8 49 38 PM](https://github.com/Archanakattii/karchana/assets/160317292/39ddc5be-3c0e-43f2-a076-ac881d8396b8)
OR operation
![WhatsApp Image 2024-03-20 at 8 45 07 PM](https://github.com/Archanakattii/karchana/assets/160317292/235aefa1-2a62-4b95-b43c-50ff5fea2e8f)
XOR operation
![WhatsApp Image 2024-03-20 at 8 48 28 PM](https://github.com/Archanakattii/karchana/assets/160317292/daa68605-51af-4a62-994f-10b529f5e0ca)

</details>

# **Various types of RISC-V instructions**
RISC-V instructions are encoded using a fixed-length 32-bit format, which simplifies decoding and execution. The instruction formats are categorized into six types: R, I, S, B, U, and J. Each format serves a specific purpose and has a unique encoding structure
<details>
<summary><b>R-type instructions:
</b></summary>
<br>
The r-type instruction format, which is used to execute arithmetic and logical instructions. The first field in the r-type instruction format is called the opcode field, which is also known as the operation code.. Eg:-add rd, rs1, rs2: Add contents of registers rs1 and rs2 and store result in rd</p>
  </details>
<details>
<summary><b>I-type instructions:
</b></summary>
<br>
I-type instructions for immediate and load operations. They include two register operands and a 12-bit immediate value. Eg:-addi rd, rs1, imm: Add immediate value to contents of register rs1 and store result in rd.</p>
  </details>
<details>
<summary><b>S-type instructions:
</b></summary>
<br>
S-Type instructions are primarily used for storing data from a register to memory. They operate on a 12-bit immediate value (offset) and use two source registers (rs1 and rs2) to calculate the memory address where the data will be stored.. Eg:-sb rs2, offset(rs1): Store the least significant byte of rs2 at the memory address computed by adding rs1 and offset.</p>
  </details>
<details>
<summary><b>B-type instructions:
</b></summary>
<br>
The B-Type instructions in the RISC-V architecture are branch instructions, which are used for controlling the flow of execution based on certain conditions. They perform conditional branching by comparing the contents of two registers and branching if the condition is satisfied. Eg:- beq (compare and label)</p>
  </details>
<details>
<summary><b>U-type instructions:
</b></summary>
<br>
The U-Type instructions in the RISC-V architecture are used for working with immediate values. They allow for the loading of 20-bit immediate values into the upper bits of a register. Eg:- lui rd, imm: Load upper immediate - Load the immediate value shifted left by 12 bits into the most significant bits of rd.</p>
  </details>
<details>
<summary><b>J-type instructions:
</b></summary>
<br>
The J-Type instructions in the RISC-V architecture are jump instructions, which are used to change the flow of control unconditionally. They facilitate transferring the control of the program to a different memory location. Eg:-jal rd, imm: Jump and link - Jump to the target address and store the address of the next instruction in rd.</p>
</details>
<summary><b>short recap:
</b></summary>
<br>
R-type instructions for register-register operations, an I-type instructions for immediate and load operations, and S-type instructions for store operations. B-type instructions for conditional branch operations. U-type instructions for long immediate and J-type instructions for unconditional jumps.</p>
</details>

# Base Instructions Format

<p align="justify">The base instruction format of RISC-V (pronounced "risk-five") is a 32-bit instruction set architecture (ISA) designed to be simple, modular, and extensible. The base instruction format consists of 32 bits divided into:

Opcode (OP): This field specifies the operation to be performed. It typically occupies the most significant bits (MSBs) of the instruction and defines the basic operation or type of instruction.

RD (Destination Register): This field specifies the destination register where the result of the operation will be stored. It usually follows the opcode and occupies a fixed number of bits.

RS1 (Source Register 1): This field specifies the first source register operand for the operation. It comes after the destination register field and occupies a fixed number of bits.

RS2 (Source Register 2): This field specifies the second source register operand for the operation. It follows the RS1 field and occupies a fixed number of bits.

Immediate: This field contains an immediate value, which is a constant or operand embedded within the instruction itself. It can be used as an operand for arithmetic or logical operations, or for specifying offsets in memory access instructions.

Funct3 and Funct7: These fields provide additional information about the operation or the specific variant of the instruction. They are typically used in conjunction with the opcode to further specify the operation or variant.</p>

<details>
<summary><b>Instruction code format </b></summary>
	<br>
![instruction code formats]![download](https://github.com/Archanakattii/karchana/assets/160317292/62e524ad-786e-4900-9e3f-a5a23c4017eb)

</details>

# RISC-V REGISTER FILE: 
 <p align="justify">The RISC-V register file is a fundamental component of the RISC-V architecture, comprising a set of general-purpose registers (GPRs) used for storing data and addresses during program execution. The RISC-V ISA defines a standard set of 32 integer registers, labeled from x0 to x31.The RISC-V register file plays a crucial role in facilitating data manipulation and control flow within RISC-V programs, offering a set of storage locations for holding essential data and addresses during program execution.</p>

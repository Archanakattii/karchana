# **By Referring to C-based Lab videos and RISC-V-based lab videos**

**Snapshots of the compiled C code and RISC-V**

**Step 1**: check whether the leafpad is installed in ur machine by using the commands
leafpad sum1ton.c & (sum1ton.c is the file name)
If the leafpad editor is opened without any errors then type the C code.
If the leafpad is not installed in ur machine then install by using the following command

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

**cat sum1ton.c**

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


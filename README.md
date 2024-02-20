# karchana
**A 4-week Research Internship on RISC-V using VSDSquadron Mini RISC-V Dev Board**
BOARD SPECS:</p>

CH32V003F4U6 chip with 32-bit RISC-V core based on RV32EC instruction set</p>
SRAM 2kb onchip volatile sram 16kb external program memory</p>
Processor 24 MHz</p>
Sink Current per I/O Pin 8 mA</p>
Source Current per I/O Pin 8 mA</p>
Input voltage (nominal) 5 V</p>
I/O voltage 3.3 V</p>
Programmer/debugger Onboard RISC-V programmer/debugger, USB to TTL serial port support</p>
SPI 1x, PC5(SCK), PC1(NSS), PC6(MOSI), PC7(MISO)</p>
I2C 1x, PC1(SDA), PC2(SCL)</p>
USART 1x, PD6(RX), PD5(TX)</p>
External interrupts 8 external interrupt edge detectors, but it only maps one external interrupt to 18 I/O ports</p>
PWM pins 14X</p>
Analog I/O pins 10-bit ADC, PD0-PD7, PA1, PA2, PC4</p>
Digital I/O pins 15</p>
Built-in LED Pin 1X onboard user led (PD6)</p>
USB 2.0 Type-C</p>
TASK 1:</p>
1.To install RISC-V GNU Tool chain </p>
sudo apt install git-all # To install git</p>

sudo apt-get install autoconf automake autotools-dev curl python3 libmpc-dev libmpfr-dev libgmp-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev libexpat-dev</p>
git clone https://github.com/riscv/riscv-gnu-toolchain</p>
![WhatsApp Image 2024-02-20 at 5 26 03 PM](https://github.com/Archanakattii/karchana/assets/160317292/2a265643-d661-4a6a-babf-23f62a907f10)


![WhatsApp Image 2024-02-20 at 5 26 02 PM (2)](https://github.com/Archanakattii/karchana/assets/160317292/5f7e8e8f-57b3-4915-8b6a-d265b292d2c9)


![WhatsApp Image 2024-02-20 at 5 26 02 PM](https://github.com/Archanakattii/karchana/assets/160317292/f4369646-3762-4821-998e-ca4f17e5008e)

2.To install Yosys</p>
git clone https://github.com/YosysHQ/yosys.git</p>
cd yosys </p>
sudo apt-get install build-essential clang bison flex \libreadline-dev gawk tcl-dev libffi-dev git \ graphviz xdot pkg-config python3 libboost-system-dev\libboost-python-dev libboost-filesystem-dev zlib1g-dev</p>
sudo apt-get install tcl-dev</p>
sudo apt-get install libreadline-dev</p>
make config-gcc</p>
make </p>
sudo make install</p>

![WhatsApp Image 2024-02-20 at 5 26 01 PM (2)](https://github.com/Archanakattii/karchana/assets/160317292/74db1bcc-b5b5-4c90-8f0e-b6f4acc77c3d)
![WhatsApp Image 2024-02-20 at 5 26 01 PM (1)](https://github.com/Archanakattii/karchana/assets/160317292/5e37c28e-a048-4d18-b1f4-53fe4edf3375)

![WhatsApp Image 2024-02-20 at 5 26 00 PM (3)](https://github.com/Archanakattii/karchana/assets/160317292/3a2c62e6-c728-45d9-93d7-e9ed310b2232)


3.To install iverilog and gtkwave</p>
sudo apt-get install iverilog</p>
sudo apt update</p>
sudo apt-get install gtkwave</p>
![WhatsApp Image 2024-02-20 at 5 26 00 PM (2)](https://github.com/Archanakattii/karchana/assets/160317292/274ffcf3-ea84-467c-b80a-9ea3d72c3955)
![WhatsApp Image 2024-02-20 at 5 26 00 PM (1)](https://github.com/Archanakattii/karchana/assets/160317292/327420c5-1fb8-4f5d-be1d-b1e6f13b5cac)
![WhatsApp Image 2024-02-20 at 5 26 00 PM](https://github.com/Archanakattii/karchana/assets/160317292/a4ce0873-5d00-4c5a-bd59-b28e64ddceb3)

# FUNCTIONAL SIMULATION
Installing iverilog and gtkwave</p>

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




  Full 5-stage instruction pipeline and pc-increment description Waveform
  
![WhatsApp Image 2024-03-05 at 6 12 31 AM](https://github.com/Archanakattii/karchana/assets/160317292/8b72d733-be71-45d7-8961-49b096b28067)


![WhatsApp Image 2024-03-05 at 6 12 35 AM](https://github.com/Archanakattii/karchana/assets/160317292/f7db13a8-273a-44de-874d-563159f9cac2)






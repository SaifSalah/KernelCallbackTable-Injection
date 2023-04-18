# WinAPI Kernel Callback Table Shellcode Injector

This is a small C program that demonstrates how to use the Windows API to inject shellcode into another process by modifying its Kernel Callback Table. The program takes a PID as input, and then locates the Kernel Callback Table of the corresponding process using the process' PEB (Process Environment Block). Once the table is found, the program overwrites the first 4 bytes of the __fnCOPYDATA callback function with a custom shellcode.
## Usage

To use the program, simply run it from the command line and pass the PID of the target process as an argument:


injector.exe <PID>


For example, to inject shellcode into process with PID 1234, run:


injector.exe 1234
![alt text](https://github.com/SaifSalah/KernelCallbackTable-Injection/blob/main/c.PNG)


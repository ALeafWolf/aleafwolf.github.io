---
title: SYST19207 Final review
category: Self-review
tag: TELE25892
---
# Ture/False
1. Superscalar processing is an architecure that implements ILP.
* [true](https://en.wikipedia.org/wiki/Superscalar_processor)
2. The address bus on Intel's 80386 chip has 32-bits.
* true, it supports 2^32 = 4GB physical memory
3. The system bus is composed of the address bus, the data bus and the control bus.
* [true](https://en.wikipedia.org/wiki/System_bus)
4. The instructions on an IA-32 processor are substantially simpler (hardware implementation) than the instructions on a 32-bit ARM processor.
* false, instructions on RISC (ARM processor) are simpler than CISC(IA-32)'s, it does not have to go through a microcode conversion layer
5. On the 8086 processor there are 16 bits in the status flag register but only 5 of them are used.
* false, 9 of them are used
6. The assembler instruction MOV AL, 5 store the value 5 to the AX register.
* false, value 5 is stored in AL register
7. There are 127 possible characters using the 7-bit ASCII character representation.
* [false, there 128 7-bit ASCII character representation](http://www.neurophys.wisc.edu/comp/docs/ascii/)
8. The Intel Core i7 processor, in general terms, follows the Von Neumann architectural model.
* true
9. IEEE-754 is the name of a standard which describes how to store SIMD data in computers.
* false, it's for regular the floating-point arithmetic implement on the hardware. 
# Multiple Choice
10. Which of the following best represents the number of instructions in the later versions of the IA-32 architecture?

1300    530     30      230     130

11. Suppose a modern Inter processor has two cores, and each core supports hyperthreading. How many separate instruction streams can it execute at the same time?

1   2   3   4   8

12. Which of the following is NOT an advantage of ARM architecture processors?
- small size
- simpler to program than CISC processorss like Inter
- few memory operations, only load/store
- low power usage

13. Which of the following best describes the number of clock cycles required to execute a typical assembler instruction in a superscalar processor?

1       less than 1     100     several     4000000

14. Which of the following computing strategies has not been successfully implemented? 
- SIMD
- MIMD
- SISD
- MISD

15. Which of these registers would you consider to be a 32-bit register?
- AL
- EAX
- RAX
- DX
- AX
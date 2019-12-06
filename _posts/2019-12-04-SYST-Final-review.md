---
title: SYST19207 Final review
category: Self-review
tag: SYST19207
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

1300    **530**     30      230     130
* for IA-32 (Pentium III) it has 545 instructions

11. Suppose a modern Inter processor has two cores, and each core supports hyperthreading. How many separate instruction streams can it execute at the same time?

1   2   3   **4**   8
* one core is addressed into two virtual cores by OS

12. Which of the following is NOT an advantage of ARM architecture processors?
- small size
- simpler to program than CISC processorss like Intel
- **few memory operations, only load/store**
- low power usage
* it's a trait, not the advantage

13. Which of the following best describes the number of clock cycles required to execute a typical assembler instruction in a superscalar processor?

1       **less than 1**     100     several     4000000

14. Which of the following computing strategies has not been successfully implemented? 
- SIMD
- MIMD
- SISD
- **MISD**
- They have all been successfully implemented
* ~~although MISD is the less common one, still it's being implemented on Space Shuttle flight control computers [Source](https://en.wikipedia.org/wiki/MISD#cite_note-1)~~

15. Which of these registers would you consider to be a 32-bit register?
- AL: 8-bit
- **EAX**
- RAX
- DX: 16-bit
- AX: 16-bit

16. Picture with operating modes: User, System, FIQ , Supervisor, Abort, IRQ, Undefined
- IA-32
- 8086
- **ARM**
- Pentium
- none of the above

17. Where is the answer stored after the following code?
```
MOV BX, 1004h
MOV AX, 1232h
MUL BX
```
- AX
- DX
- AX DX
- **DX AX**
* result that over 16-bits is stored in DX AX, refer to Q33

18. What will the following code do?
```
ORG 100h
MOV AX, 0B800h
MOV DS, AX
MOV CL, 'A'
MOV CH, 0Fh
MOV BX, 0000h
MOV [BX], CX
MOV CH, 3Fh
MOV [BX+4], CX
MOV CH, 0F0h
RET
```
- displays 2A's on the screen with one space between each

# Short Answer
19. [ref](https://www.electronics-tutorials.ws/binary/signed-binary-numbers.html)
* 8-bit signed integers (using signed magnitude):
- smallest: -127 (1111 1111)
- largest: 127 (0111 1111)
* 8-bit signed integers (using 2's complement):
- smallest: -128 (-2^7, 1000 0000)
- largest: 127 (2^7 - 1, 0111 1111)

20. 1101001b = 69h

21. 40B79457h is stored in memory location 20000, what's the value at address 20003?
- Big Endian: 40 B7 94 57 -> 57
- Little Endian: 57 94 B7 40 -> 40

22. How many times does JNE Label get executed in following code?
```
MOV AX, 3
Label:
SUB AX, 1
CMP AX, 0
JNE Label
HLT
```
* ax = 3 -> 2 -> JNE 0 -> 1 -> JNE 0 -> 0 -> JNE 0 -> HLT
* 3 times

23. Give the contents of the stack after following code:
```
PUSH 8
PUSH 3
PUSH 7
POP BX
POP BX
PUSH 2
```
* Answer:
```
2
8
bottom
```

24. doing addtion of 10 int
- time slices with a traditional single-processor: 10 - 1 = 9 slices
- time slices with 6 processors: 4 slices
```
        1   2   3   4   5   6   7   8   9   10
slice 1:  a       b       c       d       e
slice 2:      f               g 
slice 3:              h
slice 4:                          i
```

25. 123d = 01111011b
```
  123
   64
 ----
   59
   32
 ----
   27
   16
 ----
   11
    8
 ----
    3
    2
 ----
    1
    1
 ----
    0   
```

26. 1010110b = 64 + 16 + 4 + 2 = 88d

27. 

31. 12.5625 to IEEE-754 binary
```
12.5625 = 0.125625 x 10^2
```

32. 1000000 cycles, CPI 20, number of instructions?
```
1000000/20 = 50000 instructions
```

33. Write an 8086 assembly program to perform 99900 / (277-227) * (44+397)
```
org 100h

mov ax, 9990
mov bx, 10
mul bx       ;99900 in (DX AX)
mov bx, 50   ;277-227
div bx
mov bx, 441  ;44+397
mul bx

RET   
```

34. Write 8086 program using display memory at 0xB8000 for write upper-case alphabet to the screen, start at the second line, text should be black and its background is white
```
org 100h

mov dl, 25        ;loop counter
mov ax, 0xB800  
mov ds, ax  
mov cl, 'A'
mov ch, 11110000b
mov bx, 160       ;default screen width is 80, each char's size is 2
mov [bx], cx  
charLoop:
add bx, 2
add cl, 1
mov [bx],cx 
sub dl, 1 
cmp dl, 0
JNE charLoop


RET  
```
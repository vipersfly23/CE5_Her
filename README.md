CE5_Her
=======

MIP Architecture
TASK #1: Simple MIPS Assembly Program
Write a MIPS assembly program that will initialize registers $S0 and $S1 with the decimal values 44 and -37 
respectively (Code Example 6.10 pretty much gives the problem away). Use a register instruction to add these 
values together and store the result in $S2. Finally you will write an instruction that will store $S2 to the 
hexadecimal memory address x54. If your program has more than 4 lines you are doing it wrong. Include your completed 
program in your README BOC Lesson 37 and include comments. Remember there is no “initialize” instruction so how do you 
go about initializing a register? What is the expected outcome of each step of the program?


  * addi $s0,$0,2c
  
    *  HEX CODE: x"2010002C"
  
  *  addi $s1,$0,bd
 
    *  HEX CODE: x"2011ffdb"
  
 *  add $S2, $S0, $S1

    *  HEX CODE: X"02119020" *used to verify that both have been stored*
    
 *  sw $s2, 0x54($0) 

    *  HEX CODE: x"AC120054"
    
TASK #2: 

This wave form is correct because as can be seen the two add functions are being ouputed to the ALU output. This snip is the full snip, so the full store word is diplayed in task #3, but even observing that, it's clear that the word is proper stored, hence the storage in memore displaying 7, and the memory signal signifying the succesful storage.

Simulation for Task #2:

![alt text](https://github.com/vipersfly23/CE5_Her/blob/master/Task_2.GIF?raw=true "Task 2 Simulation")

In red is the first instruction, in which the ALU outputs 2c. In yellow is the second instruction adds the -37 which is circled and is ffffffdb. In blue is the third instruction adds the two together in which the output is 7. The fourth instruction stores the result into memory, which is represented by the white line, and circle. The red circle indicates the 7 has been written into memory.

Task #3:

* Implement ori $S3, $S2, x8000

    *  HEX CODE: x"AC120054"
    
    
###Codes in Mips Assembly:

1) addi $s0,$0,2c

2) addi $s1,$0,bd

3) add $S2, $S0, $S1

4) sw $s2, 0x54($0) 

5) ori $S3, $S2, x8000
    
###Codes in HEX / Binary:

1) x"2010002C"    /     00100000000100000000000000101100

2) x"2011ffdb"    /     00100000000100011111111111011011

3) X"02119020"    /     00000010000100011001000000100000

4) X"96538000"    /     10010110010100111000000000000000

5) x"AC130054"    /     10101100000100110000000001010100





Simulation:

![alt text](https://github.com/vipersfly23/CE5_Her/blob/master/Simulation.GIF?raw=true "Simulation")

Explanation:

In red is the first instruction, in which the ALU outputs 2c. In yellow is the second instruction adds the -37 which is circled and is ffffffdb. In blue is the third instruction adds the two together in which the output is 7. The fourth instructions in white performs the operation of or immediate which is then results in 8007, and then writes it into memory, which is represented in orange, and the red circle shows that it has been written into memory.

ALU Decoder:

![alt text](https://github.com/vipersfly23/CE5_Her/blob/master/ALU_Decoder.GIF?raw=true "ALU Decoder")

MIPS Design:

![alt text](https://github.com/vipersfly23/CE5_Her/blob/master/MIPS.GIF?raw=true "MIPS Design")

Main Decoder:

![alt text](https://github.com/vipersfly23/CE5_Her/blob/master/main_decoder.GIF?raw=true "Main Decoder")



###Functionality:

Verified with DR. NEEBEL in class that program works in compliance with the assignment.

###Documentation:
Received help from C3C Thompson. After redesigning the mips architecture multiple times, he showed me the more simple way to solve the task. C3C Terragnoli showed me how to implement a MUX. 




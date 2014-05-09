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
  
  *  sw $s2, 0x54($0) 

    *  HEX CODE: x"AC120054"
    
TASK #2: 

This wave form is correct because as can be seen the two add functions are being ouputed to the ALU output. This snip is the full snip, so the full store word is diplayed in task #3, but even observing that, it's clear that the word is proper stored, hence the storage in memore displaying 7, and the memory signal signifying the succesful storage.


Task #3:

* Implement ori $S3, $S2, x8000





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
  
  *  addi $s1,$0,bd
  
  *  sw $s2, 0x54($0) 

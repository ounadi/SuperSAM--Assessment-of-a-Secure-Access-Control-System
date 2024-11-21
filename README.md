
System Review: Analyze the "implementation note" provided, which describes the system architecture, cryptographic choices, and design rationale.
AES Implementation Analysis: Critically evaluate the embedded AES implementation intended for hardware tokens, focusing on potential vulnerabilities like side-channel attacks.
Recommendations: Propose practical and secure solutions to address identified flaws and improve system robustness.

Zip File Overview
Zip folder containing a higher-order masked AES with all files necessary to cross compile with ARM toolchain. 

The implementation can be compiled with just gcc for testing/understanding. 

main.c calls everything that is necessary

maths.c implements some low level field arithmetic (don't pay any attention to it)

rand.c implements a super secure RNG

masked_combined.c implements the actual higher order masking scheme

Cross Compiling
The other files (startu.asm, memmap.ld) are for cross compiling. 

elmo-funcs.h is necessary if you use GILES for power/fault simulations

The Makefile is for use with CMake when you want to crosscompile so you can use GILES. 

# 8 bit-Booth-Multiplier:

This project implements an 8-bit Booth's Multiplier using Verilog. Booth's algorithm is used for efficient multiplication of two signed 8-bit binary numbers by minimizing the number of addition and subtraction operations required.</br>

# Features:

1) Efficient Multiplication: Utilizes Booth's algorithm to perform signed binary multiplication.</br>
2) Behavioral Verilog: The design is implemented using behavioral Verilog, describing the functionality in terms of algorithms and data flow.</br>
3) Synchronous Operation: Operates on a clock signal to synchronize the multiplication process.</br>

# File Structure: 

1)Booths_Multiplier_8bit.v: Verilog module implementing the 8-bit Booth's multiplier.</br>
2)Clk_divider.v: Verilog module to slow down the Clock frequency of FPGA board.</br>

# How it works:

1)Initialization:
Computes the 2's complement of the multiplicand (In1).</br>
Initializes the accumulator with the multiplicand and multiplier.</br>
2)Booth's Algorithm:</br>
Iterates through 8 cycles, checking the least significant bits of the accumulator to determine whether to add, subtract, or shift.</br>
Performs arithmetic right shifts after each operation.</br>
3)Clk divider module:</br>
This module slow downs the in-built clock frequency of the FPGA module because it is high enough that we cant notice its pulse.</br>
4)Result:</br>
The final product is obtained from the upper 16 bits of the accumulator after 8 iterations.</br>

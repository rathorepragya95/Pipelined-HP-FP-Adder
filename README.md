# Pipelined-HP-FP-Adder
Verilog Code For IEEE 754 Half Precision (16 bit) Floating Point Adder
   
   This is a reduced complexity floating point adder.   
   
   
   Format for IEEE 754 HP FP:
   S    Exp     Mantissa
   15   14:10   9:0     

   Note: Number = 0 for exp=0 and mantissa=0

Stage 1: Compare the exponents and determine the amount of shifts required to align the mantissa to make the exponents equal. Then, right-shift the mantissa of the smaller exponent by the required amount (alignment).

Stage 2: Compare the two aligned mantissas and determine which is the smaller of the two. Take 2’s complement of the smaller mantissa if the signs of the two numbers are different. Then, add the two mantissas. (addition).

Stage 3: Determine the amount of shifts required and the corresponding direction to normalize the result (normalization-1).

Stage 4: Shift the mantissa to the required direction by the required amount. Adjust the exponent accordingly and check for any exceptional condition (normalization-2).


I'll be adding source code after May 31st 2019 due to Univeristy policies.  

# full_adder.v
Implemented 1-bit Full Adder RTL design in Verilog using Vivado. Includes source code and simulation testbench.
# Full Adder using Verilog (Vivado)

## Overview
This project implements a 1-bit Full Adder using Verilog HDL.  
The design is created and simulated using Xilinx Vivado.

A Full Adder adds three 1-bit inputs and produces a Sum and Carry output.

## Inputs and Outputs
**Inputs:**
- a
- b
- cin (carry input)

**Outputs:**
- sum
- carry

## Logic Description
- Sum is calculated using XOR operation on inputs a, b, and cin.
- Carry is generated using AND and OR logic.

## Verilog Code
```verilog
module full_adder(input a,b,cin,output sum,carry);
  wire w1,w2;
  xor x1(sum,a,b,cin);
  and a1(w1,a,b);
  and a2(w2,b,cin);
  or o1(carry,w1,w2);
endmodule

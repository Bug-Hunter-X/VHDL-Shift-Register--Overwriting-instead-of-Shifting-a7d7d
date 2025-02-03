# VHDL Shift Register Bug
This repository demonstrates a common error in VHDL when implementing a shift register. The initial code overwrites the register instead of performing a proper shift operation. The corrected version provides a functional shift register.

## Bug Description
The `shift_register` entity is intended to create an 8-bit shift register. However, the provided VHDL code has a logical flaw. The assignment `shift_reg <= data_in;` inside the `rising_edge(clk)` statement overwrites the entire register with the `data_in` value on every clock cycle.  It doesn't shift the data.

## Solution
The solution involves correctly implementing the shift operation using concatenation and signal shifting.  This is detailed in `bugSolution.vhdl`

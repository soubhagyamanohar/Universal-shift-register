# Universal-shift-register
using verilog code
#Introduction 
A Universal shift register is a register which has both the right shift and left shift with parallel load capabilities. Universal shift registers are used as memory elements in computers. A Unidirectional shift register is capable of shifting in only one direction. A bidirectional shift register is capable of shifting in both the directions. The Universal shift register is a combination design of bidirectional shift register and a unidirectional shift register with parallel load provision.
### n-bit universal shift register –
A n-bit universal shift register consists of n flip-flops and n 4×1 multiplexers. All the n multiplexers share the same select lines(S1 and S0)to select the mode in which the shift register operates. The select inputs select the suitable input for the flip-flops.
<details open>
<summary>Basic connections</summary>
<br>The first input (zeroth pin of multiplexer) is connected to the output pin of the corresponding flip-flop.
The second input (first pin of multiplexer) is connected to the output of the very-previous flip flop which facilitates the right shift.
The third input (second pin of multiplexer) is connected to the output of the very-next flip-flop which facilitates the left shift.
The fourth input (third pin of multiplexer) is connected to the individual bits of the input data which facilitates parallel loading.
The working of the Universal shift register depends on the inputs given to the select lines.The register operations performed for the various inputs of select lines are as follows:

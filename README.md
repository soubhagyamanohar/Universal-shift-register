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
![Functional Table](https://github.com/soubhagyamanohar/Universal-shift-register/assets/116057756/37436c74-e572-489e-9c29-210e8a489cc8) 
![Block Diagram Of n-bit Universal Shift Registers](https://github.com/soubhagyamanohar/Universal-shift-register/assets/116057756/5cfc4965-07a1-4f02-96bb-0cdc2b43c4b5)
</details>
<details open>
<summary>Circuit Diagram</summary>
<br>4-bit Universal shift register diagram is shown below.
![Universal-Shift-Register-Diagram 1](https://github.com/soubhagyamanohar/Universal-shift-register/assets/116057756/6d542947-80b4-486a-9237-1906083a0200)
1.Serial input for shift-right control enables the data transfer towards the right and all the serial input and output lines are connected to the shift-right mode. 2.The input is given to the AND gate-1 of the flip-flop -1 as shown in the figure via serial input pin.
3.Serial input for shift-left enables the data transfer towards the left and all the serial input and output lines are connected to shift-left mode.
4.In parallel data transfer, all the parallel inputs and outputs lines are associated with the parallel load.
5.Clear pin clears the register and set to 0.
6.CLK pin provides clock pulses to synchronize all the operations.
7.In the control state, the information or data in the register would not change even though the clock pulse is applied.
8.If the register operates with a parallel load and shifts the data towards the right and left, then it acts as a universal shift register.
</details>

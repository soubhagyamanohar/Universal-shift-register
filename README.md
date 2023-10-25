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

  
  *Serial input for shift-right control enables the data transfer towards the right and all the serial input and output lines are connected to the shift-right mode. *The input is given to the AND gate-1 of the flip-flop -1 as shown in the figure via serial input pin.

  
*Serial input for shift-left enables the data transfer towards the left and all the serial input and output lines are connected to shift-left mode.


*In parallel data transfer, all the parallel inputs and outputs lines are associated with the parallel load.


*Clear pin clears the register and set to 0.


*CLK pin provides clock pulses to synchronize all the operations.


*In the control state, the information or data in the register would not change even though the clock pulse is applied.


* If the register operates with a parallel load and shifts the data towards the right and left, then it acts as a universal shift register.

</details>
<details open>
<summary>Designing</summary>
<br>The design of a 4-bit universal shift register using multiplexers and flip-flops is shown below.
![Universal-Shift-Register-Design 1](https://github.com/soubhagyamanohar/Universal-shift-register/assets/116057756/ef20bc3f-7d61-4a29-8b08-c25b4509662e)

* S0 and S1 are the selected pins that are used to select the mode of operation of this register. It may be shift left operation or shift right operation or parallel mode.


* Pin-0 of first 4×1 Mux is fed to the output pin of the first flip-flop. Observe the connections as shown in the figure.


*Pin-1 of the first 4X1 MUX is connected to serial input for shift right. In this mode, the register shifts the data towards the right.


*Similarly, pin-2 of 4X1 MUX is connected to the serial input for shift-left. In this mode, the universal shift register shifts the data towards the left.


*M1 is the parallel input data given to the pin-3 of the first 4×1 MUX to provide parallel mode operation and stores the data into the register.


*Similarly, remaining individual parallel input data bits are given to the pin-3 of related 4X1MUX to provide parallel loading.


*F1, F2, F3, and F4 are the parallel outputs of Flip-flops, which are associated with the 4×1 MUX.
</details>

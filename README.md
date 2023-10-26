# Universal-shift-register
using verilog code
#Introduction 
A Universal shift register is a register which has both the right shift and left shift with parallel load capabilities. Universal shift registers are used as memory elements in computers. A Unidirectional shift register is capable of shifting in only one direction. A bidirectional shift register is capable of shifting in both the directions. The Universal shift register is a combination design of bidirectional shift register and a unidirectional shift register with parallel load provision.
### n-bit universal shift register –
A n-bit universal shift register consists of n flip-flops and n 4×1 multiplexers. All the n multiplexers share the same select lines(S1 and S0)to select the mode in which the shift register operates. The select inputs select the suitable input for the flip-flops.

<details open>
<summary>Circuit Diagram</summary>
<br>4-bit Universal shift register diagram is shown below.

 ![Universal-Shift-Register-Diagram 1](https://github.com/soubhagyamanohar/Universal-shift-register/assets/116057756/6d542947-80b4-486a-9237-1906083a0200)

  
* Serial input for shift-right control enables the data transfer towards the right and all the serial input and output lines are connected to the shift-right mode.
  

* The input is given to the AND gate-1 of the flip-flop -1 as shown in the figure via serial input pin.

  
* Serial input for shift-left enables the data transfer towards the left and all the serial input and output lines are connected to shift-left mode.


* In parallel data transfer, all the parallel inputs and outputs lines are associated with the parallel load.


* Clear pin clears the register and set to 0.


* CLK pin provides clock pulses to synchronize all the operations.


* In the control state, the information or data in the register would not change even though the clock pulse is applied.


* If the register operates with a parallel load and shifts the data towards the right and left, then it acts as a universal shift register.

</details>
<details open>
<summary>Designing</summary>
<br>The design of a 4-bit universal shift register using multiplexers and flip-flops is shown below.

  ![Universal-Shift-Register-Design 1](https://github.com/soubhagyamanohar/Universal-shift-register/assets/116057756/ef20bc3f-7d61-4a29-8b08-c25b4509662e)

* S0 and S1 are the selected pins that are used to select the mode of operation of this register. It may be shift left operation or shift right operation or parallel mode.


* Pin-0 of first 4×1 Mux is fed to the output pin of the first flip-flop. Observe the connections as shown in the figure.


* Pin-1 of the first 4X1 MUX is connected to serial input for shift right. In this mode, the register shifts the data towards the right.


* Similarly, pin-2 of 4X1 MUX is connected to the serial input for shift-left. In this mode, the universal shift register shifts the data towards the left.


* M1 is the parallel input data given to the pin-3 of the first 4×1 MUX to provide parallel mode operation and stores the data into the register.


* Similarly, remaining individual parallel input data bits are given to the pin-3 of related 4X1MUX to provide parallel loading.


* F1, F2, F3, and F4 are the parallel outputs of Flip-flops, which are associated with the 4×1 MUX.
</details>
<details open>
<summary>Working</summary>
<br>
* From the above figure, selected pins the mode of operation of the universal shift register. Serial input shifts the data towards the right and left and stores the data within the register.
  
* Clear pin and CLK pin are connected to the flip-flop. 

* M0, M1, M2, M3 are the parallel inputs while F0, F1, F2, F3 are the parallel outputs of flip-flops

* When the input pin is active HIGH, then the universal shift register loads / retrieve the data in parallel. In this case, the input pin is directly connected to 4×1 MUX

* When the input pin (mode) is active LOW, then the universal shift register shifts the data. In this case, the input pin is connected to 4×1 MUX via NOT gate.

* When the input pin (mode) is connected to GND (Ground), then the universal shift register acts as a Bi-directional shift register.

* To perform the shift-right operation, the input pin is fed to the 1st AND gate of the 1st flip-flop via serial input for shit-right.

* To perform the shift-left operation, the input pin is fed to the 8th AND gate of the last flip-flop via input M.

* If the selected pins S0= 0 and S1 = 0, then this register doesn’t operate in any mode. That means it will be in a Locked state or no change state even though the clock pulses are applied.

* If the selected pins S0 = 0 and S1 = 1, then this register transfers or shifts the data to left and stores the data.

* If the selected pins S0 = 1 and S1 = 0, then this register shifts the data to right and hence performs the shift-right operation.

* If the selected pins S0 = 1 and S1 = 1, then this register loads the data in parallel. Hence it performs the parallel loading operation and stores the data.

 ![Functional Table](https://github.com/soubhagyamanohar/Universal-shift-register/assets/116057756/37436c74-e572-489e-9c29-210e8a489cc8)  

 From the above table, we can observe that this register operates in all modes with serial/parallel inputs using 4×1 multiplexers and flip-flops
 </details>
 <details open>
<summary>Advantages</summary>
<br>
The advantages of a universal shift register include the following.
   
* This register can perform 3 operations such as shift-left, shift-right, and parallel loading.
Stores the data temporarily with in the register.

* It can perform serial to parallel, parallel to serial, parallel to parallel and serial to serial operations.

* It can perform input-output operations in both the modes serial and parallel.

* A Combination of the unidirectional shift register and bidirectional shift register gives the universe shift register.

* This register acts as an interface between one device to another device to transfer the data.
 </details>
 
 https://github.com/soubhagyamanohar
 https://github.com/SamruddhiHiremath

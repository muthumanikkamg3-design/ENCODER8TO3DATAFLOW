### ENCODER 8TO3 DATAFLOW Modelling

**AIM:**

To implement  Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:** Quartus prime

**THEORY**

**Encoder 8 To 3**

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/0bc242c1-eb9e-4c47-afe5-30428470efc3)

Figure 01  Block Diagram of Encoder 8 * 3

**Truth Table**

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/35496b14-ae6e-4cd1-9abd-d6736b576575)

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

Logical circuit of the above expressions is given below:

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/95acaee6-c873-4c75-89eb-ef09fb158053)

Figure 02  Encoder 8 * 3

**Procedure**

/* write all the steps invloved */
Start the design by identifying the function of the module.
The given module is a 3-bit binary encoder, which converts 8 input lines (y0–y7) into a 3-bit output (a, b, c).

Create a new Verilog module and declare the module name as exp5.

Declare all input and output ports:

Inputs: y0, y1, y2, y3, y4, y5, y6, y7

Outputs: a, b, c

Specify the type of outputs.
Since outputs are directly assigned logical expressions, no register type is needed.

Write the logical expressions for each output bit based on the encoder truth table:

Output a becomes 1 if any of the inputs y4–y7 is 1.

Output b becomes 1 if any of the inputs y2, y3, y6, y7 is 1.

Output c becomes 1 if any of the inputs y1, y3, y5, y7 is 1.

Use assign statements to implement the logic:

assign a = (y4 | y5 | y6 | y7);

assign b = (y2 | y3 | y6 | y7);

assign c = (y1 | y3 | y5 | y7);

End the module using endmodule.

Save and compile the Verilog code using any simulator such as Xilinx ISE, ModelSim, or Vivado.

Run the simulation by applying different input combinations (activating one y input at a time) and verify that the correct 3-bit encoded output is produced.

Observe and record the output waveform from the simulation.

**PROGRAM**
Developed by: G.MUTHU MANIKKAM
RegisterNumber:25016274
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/91b28967-bc81-43b4-8b90-2c0c4484d29d" />
**RTL LOGIC FOR Encoder 8 To 3 in Dataflow Modelling**
<img width="1920" height="1020" alt="exp5 RTL" src="https://github.com/user-attachments/assets/82d803d3-82e9-43f5-baac-7752054c135b" />

**TIMING DIGRAMS FOR Encoder 8 To 3 in Dataflow Modelling**
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/f3debbc4-0266-46e6-b024-1d26b7420399" />

**RESULTS**
The Verilog program for the 8-to-3 binary encoder was successfully written, compiled, and simulated.




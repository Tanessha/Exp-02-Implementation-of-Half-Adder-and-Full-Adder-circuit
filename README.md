## NAME:YENDLURI CHANDANA
## Register no.: 23011258

# Experiment-03 Implementation of Half Adder and Full Adder circuit

# Implementation ofHalf Adder and Full Adder circuit

### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
## Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin
 
### Procedure
1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.
5. Analyze and Fix Errors:
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6. Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.


### Program:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
## HALF ADDER

module Halfadder(sum,a,b,carry);

input a,b;

output sum,carry;

xor(sum,a,b);

and(carry,a,b);

endmodule 

#### RTL REALIZATION

![Screenshot (17)](https://github.com/23011258/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842204/1b533f3a-5e1c-4d36-8faf-c14a86a86e2c)
### TRUTH TABLE

![image](https://github.com/23011258/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842204/ebf41c12-dbdd-49a1-ac03-d4b05dc385aa)
### WAVE FORM:

![Screenshot 2023-11-28 172412](https://github.com/23011258/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842204/a8adbad5-297e-41f5-9800-da7cde5bc749)

### FULL ADDER:
module fulladder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

xor(sum,a,b,c);

assign carry=a&b | b&c| a&c;

endmodule
### RTL REALIZATION:

![Screenshot (23)](https://github.com/23011258/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842204/088086c3-24bd-4f30-a355-5dde6cb4a3e0)





### TRUTH TABLE :

![image](https://github.com/23011258/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842204/646a15a3-9c16-4b43-b4c8-cfbde9e9545a)
### WAVE FORM:

![Screenshot (24)](https://github.com/23011258/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/139842204/c334faf4-99db-49de-a8e6-071f7aa3f316)


### Result:
Thus the given half adder and full adder are verified using verilog programming

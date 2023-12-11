## NAME:Tanessha 
## Register no.: 23006086
## Experiment-03 Implementation of Half Adder and Full Adder circuit
Implementation ofHalf Adder and Full Adder circuit
## AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime

## Theory
Adders are digital circuits that carry out addition of numbers.

## Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

## Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

## Procedure
# Create a New Project:

Open Quartus and create a new project by selecting "File" > "New Project Wizard."
Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).
## Create a New Design File:

Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.
## Write the Combinational Logic Code:

Open the newly created Verilog or VHDL file and write the code for your combinational logic.
## Compile the Project:

To compile the project, click on "Processing" > "Start Compilation" in the menu.
Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.
## Analyze and Fix Errors:

If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
Review and fix any issues in your code if necessary.
View the RTL diagram.
## Verification:

Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.
## Program:
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

## HALF ADDER
module Halfadder(sum,a,b,carry);

input a,b;

output sum,carry;

xor(sum,a,b);

and(carry,a,b);

endmodule

## RTL REALIZATION
![image](https://github.com/Tanessha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140876194/1816d767-e58f-4297-b0de-ced9113facc7)


## TRUTH TABLE
![image](https://github.com/Tanessha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140876194/13934724-e9fe-4081-b84a-860baf08a01c)


## WAVE FORM:
![image](https://github.com/Tanessha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140876194/fe36ba28-ff9c-4ff0-ad36-e09818bc7f62)


## FULL ADDER:
module fulladder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

xor(sum,a,b,c);

assign carry=a&b | b&c| a&c;

endmodule

## RTL REALIZATION:
![image](https://github.com/Tanessha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140876194/4a2783bc-71fa-48a7-ae4f-f63036afb0a6)


## TRUTH TABLE :
![image](https://github.com/Tanessha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140876194/0465a530-c7e0-4d7c-9df4-73b174a2b7e8)


## WAVE FORM:
![image](https://github.com/Tanessha/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/140876194/2d2fdc98-d594-4742-a7a2-091b459cc156)


## Result:
Thus the given half adder and full adder are verified using verilog programming

## Experiment--02-Implementation-of-combinational-logic
## Implementation of combinational logic gates

## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming. 
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

1.AND gate The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB Y= A.B

2.OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation. Y= A+B

## Procedure:
 1.Use module projname(input,output) to start the Verilog programmming.
 2.Assign inputs and outputs using the word input and output respectively.
 3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression. 
 4.Use each output to represent one for F1 and the other for F2. 5.End the verilog program using keyword endmodule.

 
## LOGIC DIAGRAM:
![263515606-09ff1f1e-833a-4530-9148-77f0ff065212](https://github.com/JAYAVARTHAN-P/Experiment--02-Implementation-of-combinational-logic-/assets/121369281/d1f31acc-809d-4da8-b470-b0f5c663790f)


## Program:
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
## Developed by: JAYAVARTHAN P RegisterNumber: 212222100015
```
module exp2(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire x1,x2,x3,x4,x5;
assign x1 = (~A )& (~B) & (~C) & (~D);
assign x2= (A) & (~C) & (~D);
assign x3= (~B) & (C) & (~D);
assign x4= (~A) & (B) & (C) & (D);
assign x5= (B) & (~C) & (D);
assign F1 = x1 | x2 | x3 | x4 | x5;
endmodule
```
## TRUTHTABLE:
![EXP2 TT](https://github.com/JAYAVARTHAN-P/Experiment--02-Implementation-of-combinational-logic-/assets/121369281/09c75f2e-01f5-41c9-aa75-27ba884e5042)


## RTL realization
## Output:
## RTL:
![263515619-c9569732-6a5d-4ba9-b5e7-21c4e60fa748](https://github.com/JAYAVARTHAN-P/Experiment--02-Implementation-of-combinational-logic-/assets/121369281/a697066a-37ec-4a91-9e3c-54d25ba60be1)


## Timing Diagram:

![263515627-1057c174-518b-41bb-9d76-8ecf1f538ec7](https://github.com/JAYAVARTHAN-P/Experiment--02-Implementation-of-combinational-logic-/assets/121369281/224c0e18-1ff1-43d6-8509-a5623a6474c3)



## Result:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

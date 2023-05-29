# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
1.Hardware – PCs, Cyclone II , USB flasher
2.Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

# Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

# Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'
 

## Logic Diagram
![image](https://user-images.githubusercontent.com/113497680/233377544-293c2478-902a-4a55-bd97-1c98181a3fb8.png)

## Procedure

1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by:Harini.M.D
RegisterNumber: 212222230043

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

module exp2f1(A,B,C,D,f1);
input A,B,C,D;
output f1;
assign f1=(~B&~D)|(A&B&~C)|(~A&B&D);
endmodule

F2=xy’z+x’y’z+w’xy+wx’y+wxy

module exp2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=(~y&z)|(x&y)|(w&y);
endmodule
```
## RTL realization

## Output:
### RTL
### F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
![image](https://github.com/harinidq/Experiment--02-Implementation-of-combinational-logic-/assets/113497680/7fd0eeec-e545-4f1c-8d89-63ac784f0128)
### F2=xy’z+x’y’z+w’xy+wx’y+wxy
![image](https://github.com/harinidq/Experiment--02-Implementation-of-combinational-logic-/assets/113497680/84a30327-02da-4d31-bb0a-ea5cbd8ff548)
### Timing Diagram
### F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
![image](https://github.com/harinidq/Experiment--02-Implementation-of-combinational-logic-/assets/113497680/c9934fa4-fc5d-4382-a6ff-dd98af0c6345)
### F2=xy’z+x’y’z+w’xy+wx’y+wxy
![image](https://github.com/harinidq/Experiment--02-Implementation-of-combinational-logic-/assets/113497680/9c2d82cd-54f2-4cd6-b3da-b395e22a792a)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.

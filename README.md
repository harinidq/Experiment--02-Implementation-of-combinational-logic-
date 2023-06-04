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
```
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.Combinational logic gates are digital circuits that produce outputs based solely on the current inputs. These gates are the building blocks for implementing digital systems and are used in a wide range of applications, including arithmetic and logic operations, memory devices, and control circuits.The two functions, F1 and F2, can be implemented using a combination of logic gates such as AND gates, OR gates, and NOT gates.
```
## Procedure
```
1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output(RTL Viewer and Timing Diagram) to represent F1 and F2.

5.End the verilog program using keyword endmodule.
```
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

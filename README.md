# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
### Hardware – PCs, Cyclone II , USB flasher
### Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.   `      

### Using NAND gates :

NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram



### Using NOR gates : 

NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram



## Procedure

1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.


## Program:

```
Program to implement the given logic function using NAND and NOR gates and to verify its operations in 
quartus using Verilog programming.

Developed by: P.Sri Varshan
RegisterNumber:  22008051

FOR NAND GATE

module combo1(A,B,C,D,F);
input A,B,C,D;
output F;
wire p,q,r;
assign p=(~C & B & A);
assign q=(~D & C & ~A);
assign r=(C & ~B & A);
assign F=(~(~p & ~q & ~r));
endmodule

FOR NOR GATE

module combo2(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r;
assign p=( c & ~b & a);
assign q=( d & ~c & a);
assign r=( c & ~b & a);
assign f=((( p | q | r)));
endmodule

```


## Output:
### RTL realization :

Using NAND Gate :

![combo 1 nand](https://user-images.githubusercontent.com/114944059/211162942-3f214ced-62fc-4712-b96e-e2f5548659ae.jpg)

Using NOR Gate :

![rtlnand](https://user-images.githubusercontent.com/114944059/211164386-0c78299a-0262-45b9-914f-7a6056585fd7.png)


## Timing Diagram :

Using NAND Gate :

![time nand](https://user-images.githubusercontent.com/114944059/211164435-89df4f44-3798-4bc3-9a51-da026ff36da8.png)


Using NOR Gate :

![time nor](https://user-images.githubusercontent.com/114944059/211164441-ea5049b4-6fa5-47f6-8b4d-f4bd366e1a2f.png)


## Truth Table :

Using NAND Gate :

![TT NAD](https://user-images.githubusercontent.com/114944059/211163871-4614e97f-303c-4790-91aa-a0ba544f5091.png)

Using NOR Gate :

![tt NOT](https://user-images.githubusercontent.com/114944059/211164169-ca1946e8-2474-404c-a16a-e1e107e9b2ea.png)


## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.

# TITLE: Implementation of Ex-NOR Gate using NOR Gate only
## THEORY:
An Ex-NOR gate, also known as an Exclusive-NOR gate, is a logic gate that produces a HIGH output only when the number of HIGH inputs is even. It behaves like an equality comparator, producing a HIGH output when the inputs are equal.

To implement an Ex-NOR gate using only NOR gates, we can use De Morgan's theorem. De Morgan's theorem states that the complement of a logic function (AND, OR, or XOR) is obtained by complementing each input and changing the function to its dual (i.e., changing AND to OR, OR to AND, and XOR to XNOR).

The truth table for an Ex-NOR gate is as follows:

A	B	Y
0	0	1
0	1	0
1	0	0
1	1	1
To implement an Ex-NOR gate using NOR gates only, we can use the following logic:

Complement both inputs A and B using NOR gates individually.
Connect the output of the complemented A and complemented B to a NOR gate.
The output of the final NOR gate will be the Ex-NOR output.

## LOGIC DIAGRAM

![image](https://github.com/lathika-sunder/Simulation-project--Digital-Electronics/assets/95066409/af3c63d0-99e8-4b28-a299-386ee41912f6)


## NETLIST DIAGRAM
![image](https://github.com/lathika-sunder/Simulation-project--Digital-Electronics/assets/95066409/357aa6da-31e4-48b4-945f-5c24757fa750)

## TIMING DIAGRAM
![image](https://github.com/lathika-sunder/Simulation-project--Digital-Electronics/assets/95066409/4b8ffa4c-ea3d-44b8-a981-3664e6bb6d9b)


## PROGRAM

```
Name : Lathika Sunder
Reg No.: 212221230054
```

```
// Ex-NOR Gate using NOR gates only

module ExNOR_gate (A, B, Y);
  input A, B;
  output Y;
  
  wire NA, NB;
  
  // Complementing inputs using NOR gates
  nor (NA, A, A);
  nor (NB, B, B);
  
  // Final NOR gate for Ex-NOR output
  nor (Y, NA, NB);
  
endmodule
```
## RESULT

Hence the Ex-Nor gate is sccesfullyt implemented using nor gate only in Quartus.

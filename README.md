# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

Implementing Boolean functions in Verilog HDL (Hardware Description Language) involves translating the simplified Boolean expressions into Verilog code to describe the behavior of digital circuits. The basic building blocks in Verilog is module. The module represent a combinational circuit. Use logical operators (&, |, ~, ^) to implement Boolean functions directly. Use built-in gate primitives for basic functions. Use University program VWF to verify the functionality of your Verilog modules. Create waveform and check outputs against expected results

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
module minimization(a, b, c, d, w, x, y, z, f1, f2);
 input a, b, c, d, w, x, y, z;
 output f1, f2;
 wire x1, x2, x3, x4, x5, x6, x7, x8, x9, x10;
 assign x1 = (~a) & (~b) & (~c) & (~d);
 assign x2 = (a) & (~c) & (~d);
 assign x3 = (~b) & (c) & (~d);
 assign x4 = (~a) & (b) & (c) & (d);
 assign x5 = (b) & (~c) & (d);
 assign f1 = x1 | x2 | x3 | x4 | x5;
 assign x6 = (x) & (~y) & (z);
 assign x7 = (~x) & (~y) & (z);
 assign x8 = (~w) & (x) & (y);
 assign x9 = (w) & (~x) & (y);
 assign x10 = (w) & (x) & (y);
 assign f2 = x6 | x7 | x8 | x9 | x10;
 endmodule

```
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: Mitran R

RegisterNumber:24006381


**RTL realization**

![2](https://github.com/user-attachments/assets/70b50dbe-912e-4378-878d-741943a9039c)

**Timing Diagram**
![2 1](https://github.com/user-attachments/assets/40b9aa33-82d2-4d1c-9bd0-c354a3810b4f)

**Truth Table**

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

![tt](https://github.com/user-attachments/assets/872fb103-17d8-48da-9de9-54c84abf9952)

F2=xy’z+x’y’z+w’xy+wx’y+wxy

![tt 1](https://github.com/user-attachments/assets/316827c9-c6c3-4b2f-87db-42d9e15a5042)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.


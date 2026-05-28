# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Full Adder**

![alt text](<Truth Table Full Adder.png>)

**Full Subtractor**

![alt text](<Truth Table Full Subtractor.png>)

**Procedure**

Write the detailed procedure here

**Program:**

```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: Thaarakeshwar 

RegisterNumber: 212225040466

```
**Full Adder**
```
module exp31(A,B,Cin,Sum,Carry);
Input A,B,Cin;
Output Sum,Carry;
assign Sum=A^B^Cin;
assign Carry=((A^B)&Cin)|(A&B);
endmodule
```
**Full Subtractor**
```
module expfs(a,b,bin,difference,borrow);
  input a,b,bin;
  output difference,borrow;
  assign difference= ( (a ^ b)^bin);
  assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
  endmodule
```
**RTL Schematic**

**Full Adder**

![alt text](<Full Adder .png>)

**Full Subtractor**

![alt text](<Full Subtractor.png>)

**Output Timing Waveform**

**Full Adder**

![alt text](<Full Adder Waveform.png>)

**Full Subtractor**

![alt text](<Full Subtractor Waveform.png>)

**Result**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




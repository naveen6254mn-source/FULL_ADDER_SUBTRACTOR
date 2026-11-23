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

**Truthtable FULL ADDER**
<img width="429" height="395" alt="image" src="https://github.com/user-attachments/assets/80abb662-d002-49d9-94c6-0286b5bf6471" />

**Full Subtractor**
<img width="438" height="393" alt="image" src="https://github.com/user-attachments/assets/a8a257a3-bc2b-46be-97af-b28c1b28ec3c" />



**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:NAVEEN M
RegisterNumber:212225230197
*/
```
**Full Adder**
```
module exp4(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```

**Full Subtractor**
```
module full_subtractor(diff, borrow, a, b, bin);
  output diff;
  output borrow;
  input a;
  input b;
  input bin;
  assign diff = a ^ b ^ bin;
  assign borrow = (~a & b) | (~(a ^ b) & bin);
endmodule

```

**RTL Schematic Full Adder**
<img width="1177" height="744" alt="image" src="https://github.com/user-attachments/assets/73ac16af-4650-46ed-89f0-cb8135a646c0" />

**Full Subtractor**
<img width="1351" height="542" alt="image" src="https://github.com/user-attachments/assets/90c4693f-f089-4fc6-bf52-66652ba1744e" />


**Output Timing Waveform Full Adder**

<img width="1920" height="1201" alt="image" src="https://github.com/user-attachments/assets/6fe1f766-cc9a-4786-9b51-d5e518be1d7b" />


**Full Subtractor**

<img width="1921" height="1201" alt="image" src="https://github.com/user-attachments/assets/a9b58edf-1fb6-422f-9d2e-30a3d9b285ee" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




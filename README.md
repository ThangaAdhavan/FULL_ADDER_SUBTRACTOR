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


<img width="804" height="832" alt="image" src="https://github.com/user-attachments/assets/51da3c92-24e8-4e61-b701-6425a8b1860e" />
<img width="987" height="834" alt="image" src="https://github.com/user-attachments/assets/da2cf87b-b0fd-497f-8e79-b4dc6aedd2ab" />


**Procedure**
Write the detailed procedure here
```
Full Adder:

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.

Full Subtractor:

1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR, AND, OR gates to perform subtraction.

4.Compile, simulate, implement, and program the design similarly to the full adder.
```

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:THANGA ADHAVAN S RegisterNumber:2507124*/


**Full Adder**
```
module Fulladder(a,b,c,sum,carry);
 input a,b,c;
 output sum,carry;
 xor(sum,a,b,c);
 assign carry=a&b | b&c | a&c;
 endmodule
```
**RTL Schematic**


<img width="838" height="644" alt="Screenshot 2025-11-19 104614" src="https://github.com/user-attachments/assets/ee9e0810-0a2b-4ccb-9b48-745ab7227d9a" />

**Output Timing Waveform**
<img width="1920" height="1080" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/04bfd5ec-cf9e-44e5-8bd2-c4940c14da0a" />

**Full Subractor**
```
module Fullsubtractor(diff,borrow,a,b,c);
input a,b,c;
output diff,borrow;
xor(diff,a,b,c);
assign borrow= (~a)&c | (~a)&b | (b&c);
endmodule
```
**RTL Schematic**


<img width="788" height="627" alt="Screenshot 2025-11-19 105748" src="https://github.com/user-attachments/assets/b4ea6562-3911-4f87-a7dd-6fad18a53e96" />

**Output Timing Waveform**
<img width="1920" height="1080" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/b73c1b1d-cc68-461b-b62d-e4decf6ca116" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




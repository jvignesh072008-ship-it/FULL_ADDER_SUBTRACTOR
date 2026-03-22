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

**Procedure**

Write the detailed procedure here

**Program:Full Adder**
//Full Adder in verilog
```
module full_adder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule
```
Full Sub
//Full Sub in verilog
```
module full_subtractor (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule
```
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:VIGNESH J 
RegisterNumber:212225230297
```

**RTL Schematic output timing waveform full adder**
<img width="1032" height="555" alt="image" src="https://github.com/user-attachments/assets/2ab41013-e45b-436d-8222-8ddcf1942976" />

<img width="1543" height="729" alt="image" src="https://github.com/user-attachments/assets/ba91aebb-9d65-4911-8461-5427a1245678" />


**RTL Schematic output timing waveform full subractor**
<img width="1035" height="452" alt="image" src="https://github.com/user-attachments/assets/eeddff42-bc48-4f18-a121-d29f952eaabb" />

<img width="1548" height="734" alt="image" src="https://github.com/user-attachments/assets/a4773e50-e891-40ef-aa59-ce7177b23276" />


**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



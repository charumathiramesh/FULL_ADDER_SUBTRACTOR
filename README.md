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
## FULL ADDER:

![318405960-7116d2bf-8e90-4e96-bfd5-d62af11a317a](https://github.com/charumathiramesh/FULL_ADDER_SUBTRACTOR/assets/120204455/0037c4f9-597b-4a5d-8c5e-1f5afe7cb7d8)

## FULL SUBTRACTOR:
![318405667-33d8ba16-9169-40b0-8696-3bb8e5c3a0b7](https://github.com/charumathiramesh/FULL_ADDER_SUBTRACTOR/assets/120204455/18d18ab4-901f-459f-92a9-07138aec665f)


**Procedure**
```C
**Full Adder:**
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.
```
Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: CHARUMATHI R
RegisterNumber: 212222240021
*/
```C
.
## Full_adder
module fulladd_top(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule 

## Full_subtractor
module fullsub_top(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule

```

**RTL Schematic**

![318405073-2e45d893-4f83-4a98-8bc2-d0d30b70e7e2](https://github.com/charumathiramesh/FULL_ADDER_SUBTRACTOR/assets/120204455/54e7b835-a2fd-4655-9135-4309f0f06d6a)

**Output Timing Waveform**
## FULL ADDER:

![318405216-5d286c1d-e62e-454a-a389-00ba2c2a91fc](https://github.com/charumathiramesh/FULL_ADDER_SUBTRACTOR/assets/120204455/6e023809-8f99-497a-9a4b-f9d1f40022e3)

## FULL SUBTRACTOR:
![318405344-03d5d030-815e-4847-a976-2fd282cf0333](https://github.com/charumathiramesh/FULL_ADDER_SUBTRACTOR/assets/120204455/b1542ab1-bb37-4601-b158-4093e3738820)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




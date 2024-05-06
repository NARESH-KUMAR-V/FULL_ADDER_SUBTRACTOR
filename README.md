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
FULL-ADDER :
![img 21](https://github.com/NARESH-KUMAR-V/FULL_ADDER_SUBTRACTOR/assets/145842937/e0fff7d1-a2f7-4fa0-b9c4-1a49aee2be8f)

FULL-SUBTRACTOR:
![img 22](https://github.com/NARESH-KUMAR-V/FULL_ADDER_SUBTRACTOR/assets/145842937/826f852d-ba60-4cd5-8e91-fd30cf327e8b)

**Procedure**

STEP-1 Open Quartus Prime software.

STEP-2 Create a new project and select the target FPGA device.

STEP-3 Design and implement the full adder/subtractor using Verilog or VHDL within a new HDL file.

STEP-4 Add the HDL file to the project and compile the design.

STEP-5 Program the FPGA with the compiled design to test the functionality of the full adder/subtractor.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:Naresh Kumar v RegisterNumber:212223040126
*/
```
module fulladdsub(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry= a&b | a&c | b&c;
wire a0;
not (a0,a);
assign BO= b&c | a0&c | a0&b;
assign DIFF=a^b^c;
endmodule
```
**RTL Schematic**
![img 23](https://github.com/NARESH-KUMAR-V/FULL_ADDER_SUBTRACTOR/assets/145842937/99cb12ac-0a5a-4fb9-b02c-d5a25572e54d)

**Output Timing Waveform**
![img 24](https://github.com/NARESH-KUMAR-V/FULL_ADDER_SUBTRACTOR/assets/145842937/f07e90dc-cbcd-4dee-865d-87c12d8347c5)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




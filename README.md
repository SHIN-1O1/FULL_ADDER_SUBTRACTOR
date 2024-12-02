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
![image](https://github.com/user-attachments/assets/985a178c-d5e5-4424-aaa8-b96ebe1466b8)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**1.full adder**
**Program:**
---
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
---
**RTL Schematic**
![WhatsApp Image 2024-12-02 at 09 01 59_49d683e5](https://github.com/user-attachments/assets/da2b7957-c8b5-4212-a961-c5c6dd3b983c)

**Output Timing Waveform**
![WhatsApp Image 2024-12-02 at 09 02 00_69223a95](https://github.com/user-attachments/assets/4cdae630-aa58-4c9c-b253-3648d3469bd8)


**2.full subractor**
**Program:**
---
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
---
**RTL Schematic**
![WhatsApp Image 2024-12-02 at 09 02 00_819b9442](https://github.com/user-attachments/assets/addfd8bd-c7f2-4f48-81d8-e9977a6e8106)

**Output Timing Waveform**
![WhatsApp Image 2024-12-02 at 09 02 01_0b752e2d](https://github.com/user-attachments/assets/cdc0464c-3f15-4bcc-8310-938d4061fe4a)

**Result:
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




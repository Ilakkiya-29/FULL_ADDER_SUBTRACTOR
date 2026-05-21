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

FULL ADDER

<img width="733" height="706" alt="image" src="https://github.com/user-attachments/assets/6173adc8-7aa1-4f7b-a14b-1246e4a288fe" />


FULL SUBTRACTOR


<img width="654" height="667" alt="image" src="https://github.com/user-attachments/assets/dc35861d-b4f3-4a68-8eaf-15f17d96aa54" />


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

```
module FULL_addsub(a,b,cin,sum,carry,BO,DIFF);
input a,b,cin;
output sum,carry,BO,DIFF;
wire a0;
not(a0,a);
assign sum=a^b^cin;
assign carry=(a&b)|(b&cin)|(a&cin);
assign DIFF=a^b^cin;
assign BO=(a0&b)|(b&cin)|(a0&cin);
endmodule
```

i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule



**RTL Schematic**

FULL ADDER

<img width="1920" height="1080" alt="Screenshot (33)" src="https://github.com/user-attachments/assets/cb13156b-632c-48ad-b416-da0e3f5d6194" />


FULL SUTRACTOR

<img width="1920" height="1080" alt="Screenshot (35)" src="https://github.com/user-attachments/assets/cd162984-a95c-4022-856b-62bd3d7cd7d3" />


**Output Timing Waveform**

FULL ADDER

<img width="1920" height="1080" alt="Screenshot (34)" src="https://github.com/user-attachments/assets/ff54d134-7da7-4295-9bd7-1073cf6c554d" />


FULL SUTRACTOR

<img width="1920" height="1080" alt="Screenshot (36)" src="https://github.com/user-attachments/assets/ef0b2aa0-94d2-40f4-8345-6a5d0bd9efbc" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




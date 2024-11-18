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
**Truth Table**
![Screenshot (3)](https://github.com/user-attachments/assets/15eeb76c-df14-4b72-b763-2deb57cfaec3)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
![Screenshot (4)](https://github.com/user-attachments/assets/3c3ce696-7d99-44d0-ad7b-0fc665d089c9)


Write the detailed procedure here

**Program:**
module unit22(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire s1,c1,c2;
xor (s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule

module unit23 (df,bo,a,b,bin); 
output df; 
output bo; 
input a; 
input b; 
input bin; 
wire w1,w2,w3; 
assign w1=a^b; 
assign w2=(~a&b); 
assign w3=(~w1&bin); 
assign
df=w1^bin; 
assign bo=w2|w3; 
endmodule



/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:Ajmal Ali.S RegisterNumber:24009653
*/

**RTL Schematic**
![Screenshot (5)](https://github.com/user-attachments/assets/ec0d85bc-79ab-402a-a577-3af1456a206a)
![Screenshot (6)](https://github.com/user-attachments/assets/f72bbde9-18ae-4f32-b246-0c024a6a392f)


**Output Timing Waveform**
![WhatsApp Image 2024-11-18 at 2 24 05 PM](https://github.com/user-attachments/assets/32197666-5a0e-4311-8dbb-57049725381b)
![WhatsApp Image 2024-11-18 at 2 24 27 PM](https://github.com/user-attachments/assets/c9089645-8e2e-4eac-988f-721f74253ca0)


**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




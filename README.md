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

![WhatsApp Image 2024-12-08 at 4 43 21 PM (2)](https://github.com/user-attachments/assets/631c07cf-cf02-43db-adb3-88d35bc7cb48)


![WhatsApp Image 2024-12-08 at 4 43 21 PM (3)](https://github.com/user-attachments/assets/bffaebdb-8436-4321-b4a8-549aedfaccb5)


**Procedure**
 
 1.Type the program in quartus software
 
 2.Compile and run the program
 
 3.Generate the RTL schematic and save the logic diagram
 
 4.Create nodes for inputs and outputs to generate the things diagram
 
 5.For different input combinations generate the timing diagram


**Program:**
//full adder

module ex04(sum, cout, a, b, cin);

output sum;

output cout;

input a;

input b;

input cin;

//internal nets

wire sl,cl,c2;

//Instantiate logic gate primitives xor (sl,a,b);

and(cl,a,b);

xor (sum, sl, cin);

and(c2, sl, cin);

or(cout, c2,cl);

endmodule

Full subractor

module ex04a (df, bo, a, b, bin);

output df;

output bo;

input a;

input b;

input bin;

wire w1,w2, w3;

assign w1=a^b;

assign w2=(~a&b);

assign w3=(-w1&bin);

assign df-w1^bin;

assign bo-w2/w3;

endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: supriya S J

RegisterNumber:24001109
*/

**RTL Schematic**

![WhatsApp Image 2024-12-08 at 8 50 09 PM (1)](https://github.com/user-attachments/assets/14e01744-4085-460d-9a17-f416431f6843)

![WhatsApp Image 2024-12-16 at 7 36 36 PM](https://github.com/user-attachments/assets/04b5b3f5-6875-4466-84a0-547ca8c03be9)


**Output Timing Waveform**

![WhatsApp Image 2024-12-08 at 8 51 58 PM (1)](https://github.com/user-attachments/assets/e8fb0a10-a7a2-4f22-af97-10562248886b)

![WhatsApp Image 2024-12-08 at 8 54 31 PM (1)](https://github.com/user-attachments/assets/cd8fba26-ee1c-43bb-aad7-026b7451b8ed)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




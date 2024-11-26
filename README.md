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
![image](https://github.com/user-attachments/assets/7d761ef3-05be-44ff-95fb-ada1fbe3aa57)


**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin
**figure -1 FULL SUBTRACTOR**
![image](https://github.com/user-attachments/assets/847d8dda-d80f-4ca3-8aee-ffcfaa86c585)

**Truthtable**
FULL ADDDER
![image](https://github.com/user-attachments/assets/45ca17e8-1e6f-43ec-8982-0fc6e6b3d0f9)
FULL SUBTRACTOR
![image](https://github.com/user-attachments/assets/e1789cff-aaad-4e61-9cb0-5c855416904c)



**Procedure**

Write the detailed procedure here

**Program:**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
 ```
FULL ADDER

module experiment4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;

//internal nets
wire s1,c1,c2;

//Instantiate logic gate primitives
xor (s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule
FULL SUBTRACTOR
module experiment4a (df, bo, a, b, bin);
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
```
```
Developed by:Mohana K.V.S.L RegisterNumber:24900659
```


**RTL Schematic**
FULL ADDER
![exp4](https://github.com/user-attachments/assets/d0d45014-a225-45cc-8b34-42741644e41e)
FULL SUBTRACTOR
![exp4a](https://github.com/user-attachments/assets/5d377d31-775a-4f4d-88f2-b91c3ab9c73b)






**Output Timing Waveform**
FULL ADDER
![exp4rtl](https://github.com/user-attachments/assets/753468d1-f9a2-4524-8dbe-e3fccec666a4)
FULL SUBTRACTOR
![exp4atrl](https://github.com/user-attachments/assets/a22e7138-467a-4d60-b2a7-d5c1ef61d6af)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




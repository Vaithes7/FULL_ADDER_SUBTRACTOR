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
 ![WhatsApp Image 2024-12-01 at 21 08 40_7b9187c0](https://github.com/user-attachments/assets/a6bd6077-5b2f-4c5d-98ac-485a0d32d528)

FULL SUBTRACTOR
![WhatsApp Image 2024-12-01 at 21 09 09_da55d246](https://github.com/user-attachments/assets/c700f021-e3ee-439c-931e-a00305d14d98)


**Procedure**

1.Type the program in Quartus software.
2.Compile and run the program.
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram.
5.For different input combinations generate the timing diagram

**Program:**
```
i)FULL ADDER 
module fa(a,b,cin,sum,carry); 
input a,b,cin; 
output sum,carry; 
assign sum=( (a ^ b)^cin); 
assign carry= ( (a & b)| ( cin &(a ^ b ))); 
endmodule
```
```
ii)FULL SUBTRACTOR 
module fs(a,b,bin,difference,borrow); 
input a,b,bin; 
output difference,borrow; 
assign difference= ( (a ^ b)^bin); 
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )))); 
endmodule
```


/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:Vaitheswaran N RegisterNumber:24901212
*/

**RTL Schematic**
FULL ADDER
![Screenshot (40)](https://github.com/user-attachments/assets/7a295def-051d-4252-b6e5-665e8cd65e48)

FULL SUBTRACTOR
![Screenshot (42)](https://github.com/user-attachments/assets/aeb6eeb4-c672-4814-b779-6e01bf341e37)


**Output Timing Waveform**
FULL ADDER
![Screenshot (41)](https://github.com/user-attachments/assets/be139cfd-b283-4fcf-b5b7-95208d9c6411)

FULL SUNTARCTOR
![Screenshot (44)](https://github.com/user-attachments/assets/08663c8d-3f7e-4dab-83fe-d14b39233e26)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




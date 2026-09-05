FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin  +  A’BCin’  +  ABCin  +  AB’Cin’  =  A ⊕ B ⊕ Cin 

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

<img width="267" height="189" alt="image" src="https://github.com/user-attachments/assets/3d0195a6-ae23-4cd7-92da-8a4383d8cb5b" />

FULL SUBRACTER:

OUTPUT TIMING WAVEFORM

<img width="340" height="148" alt="image" src="https://github.com/user-attachments/assets/528f07f5-c0b9-44eb-97a2-55f38b05b12f" />

**Procedure**


Write the detailed procedure here

Program:

FULL ADDER:

module exp4(a,b,cin,sum,carry);   

input a,b,cin; output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

FULL SUBTRACTOR:

module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

endmodule 

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

DEVOLOPED BY:Darunbala.S

REGISTER NO:212225230040

RTL Schematic

FULL ADDER:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/312ae537-3524-4394-b56e-52905d798a85" />




FULL ADDER:

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/fc8b623d-582c-44da-a083-57250510266a" />


FULL SABRACTOR:

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/53e85c37-7ed1-4760-9ad1-e2f95070e22e" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




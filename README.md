# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

AIM:

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

Half Adder:

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

Half Subtractor:

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

Truthtable:

![WhatsApp Image 2024-12-02 at 9 21 12 PM](https://github.com/user-attachments/assets/11fd681e-286c-40ae-b236-258311524c03)

Procedure:

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


Program:

```
Half Adder:
module halfadder(a, b, s, ca);
 input a;
 input b;
 output s;
 output ca;
 assign s=a^b;
 assign ca=a&b;
 endmodule

Half Subtractor:
 module halfsubtractor(a, b, dif, bor); 
input a; 
input b; 
output dif; 
output bor; 
wire abar; 
assign abar=~a; 
assign dif=a^b; 
assign bor=b&abar; 
endmodule

```

 Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Shyam kumar.S

RegisterNumber:24001160

RTL Schematic:
Half Adder:
![3](https://github.com/user-attachments/assets/45db3b63-4ccd-4301-a3ae-14809b2985b3)

Half Subtractor:
![3(hs)](https://github.com/user-attachments/assets/e45e951f-e9d0-4ac4-be97-6038ce2f3965)


Output/TIMING Waveform:
Half Adder:
![3 3](https://github.com/user-attachments/assets/2dc042e4-af55-4409-b607-8edfda2c4883)

Half Subtractor:
![3 1(hs)](https://github.com/user-attachments/assets/e71cb622-3ef9-473d-b06d-abe34bd6bc68)


Result:
THUS THE BASIC LOGIC GATES ARE STUDIED AND THE TRUTH TABLES ARE VERIFIED

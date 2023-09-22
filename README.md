# Exp-03 Implementation of Half Adder and Full Adder circuit:

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### Program:
```
Developed by: Sham Rathan.S
RegisterNumber: 212221230093  
```
### Half Adder:
```
module Experiment03(A,B,S,C);
input A,B;
output S,C;
assign S=A^B;
assign C=A&B;
endmodule
```
### Full Adder:
```
module EX03(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=a^b^c;
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```

#### Half Adder:
![image](https://github.com/ShamRathan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93587823/7a37f1bf-762f-4aa5-b808-760ddfe1e266)
#### Full Adder:
![image](https://github.com/ShamRathan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93587823/2a21db5d-2ddb-4a98-ad62-cfb2df769c85)

### TRUTH TABLE::
#### Half Adder:
![image](https://github.com/ShamRathan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93587823/75c45f39-d6f2-4e0c-9cec-4393047efb9f)
#### Full Adder:
![image](https://github.com/ShamRathan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93587823/455cb998-8ada-4abb-9aac-52ad695591c0)

### OUTPUT WAVEFORM:
#### Half Adder:
![image](https://github.com/ShamRathan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93587823/5cb59096-d0ef-43c8-be9a-5fa5a1c1864e)
#### Full Adder:

![image](https://github.com/ShamRathan/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/93587823/0bf258bd-2184-4f6a-a8c5-271478b7371a)



### Result:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Half subtractor:
```
module halfsub(a,b,di,bo);
input a,b;
output di,bo;
assign di=(a^b);
assign bo=((~a)&b);
endmodule 
```
Full subtractor:
```
module fs(a,b,bin,di,bo);
input a,b,bin;
output di,bo;
assign di=a^b^bin;
assign bo=((~a&b))|(b&bin)|((~a)&bin);
endmodule
```
Developed by: Santhosh D M 
RegisterNumber: 23013934
*/

## Output:
HALF SUBTRACTOR
![267694022-f4f042c0-7a73-4ea2-a004-fbeea417cde3](https://github.com/Sandy-56/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152118022/2470e628-bf61-40a2-b14a-e763b06330e8)
HALF SUBTRACTOR
![267694145-4308edc9-98ba-4b5c-af9b-1c129530535b](https://github.com/Sandy-56/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152118022/966b93f2-172e-4e6d-9ebc-f8dd684f2d63)

## Truthtable
HALF SUBTRACTOR
![267692671-6fc6d4d8-5411-4b2a-88f2-622698d2b64e](https://github.com/Sandy-56/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152118022/1303d953-3ad4-4cb8-997b-3822d3f1f7de)
FULL SUBTRACTOR
![267693009-82ea8260-0ab9-4635-b0a7-8f0ee2764b7d](https://github.com/Sandy-56/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152118022/5ae27a82-8f41-440d-b05d-644936cd8463)


Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.



## Timing diagram 
HALF SUBTRACTOR 
![267694523-4bb27be4-4192-46fd-aa4c-7e6f72016d2b](https://github.com/Sandy-56/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152118022/3bb17243-4173-44b7-8984-0275277af0b7)

FULL SUBTRACTOR 
![267694585-67088219-cdb4-4a54-823a-066a0e1c0b49](https://github.com/Sandy-56/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/152118022/0947d00e-4d55-4f7f-8668-8a47a3d7ab1c)

## NAME : AVINASH T
## ROLL NO : 23914109

# Experiment 04 Implementation of Half subtractor and Full subtractor circuit
 
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.
 
## Equipments Required:

 Hardware – PCs, Cyclone II , USB flasher
 
 Software – Quartus prime
 
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
The combinational circuit of a full subtractor executes the operation of subtraction on three binary bits generating outputs for the difference D and borrow B-out. Exactly like the binary adder circuit, the full subtractor can also be imagined as two half subtractors connected together as shown below.
A full subtractor can be realized using two half subtractors. It will take two half-subtractors and one OR gate. The logic circuit diagram of the full subtractor using two half subtractors 
A Half subtractor is a combination circuit with two inputs and two outputs that are different and borrow. It produces the difference between the two binary bits at the input and also produces an output (Borrow) to indicate if a 1 has been borrowed.


## PROGRAM

HALF SUBTRACTOR

module experiment4(diff,borrow,a,b);

input a,b;

output diff,borrow;

assign diff = a^b;

assign borrow = ~a&b;

endmodule 


FULL SUBTRACTOR 

module experiment4(diff,borrow,a,b,c);

input a,b,c;

output diff,borrow;

assign diff = a^b^c;

assign borrow = (~a)&c | (~a)&b | (b&c);

endmodule 


##  RTL realization

HALF SUBTRACTOR 

![image](https://github.com/AVINASH05T/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151514286/c86c6c67-9acb-496c-a0fd-86d8d243e876)


FULL SUBTRACTOR

![image](https://github.com/AVINASH05T/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151514286/d2d467b3-0031-468c-a428-666d481a816d)


## Truthtable

HALF SUBTRACTOR

![image](https://github.com/AVINASH05T/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151514286/62b75058-86a3-46f8-b26e-e899c0b56c12)

FULL SUBTRACTOR

![image](https://github.com/AVINASH05T/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151514286/703bbaec-506a-4786-b1e1-1d89c84e7ef5)



## Timing diagram 

HALF SUBTRACTOR

![image](https://github.com/AVINASH05T/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151514286/fefde97d-ccfd-4005-abbd-5dcfdbe88f67)


FULL SUBTRACTOR

![image](https://github.com/AVINASH05T/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/151514286/95ad070b-4c93-48d1-a2a0-5d636dd496f8)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.

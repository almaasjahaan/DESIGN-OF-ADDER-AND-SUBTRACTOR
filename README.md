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
1 full adder

![image](https://github.com/user-attachments/assets/a08a2863-e8eb-45ea-aa74-0fb70cbcb2c2)

2 Full susbtractor

![image](https://github.com/user-attachments/assets/4a8c982e-958d-4608-9f78-5b84344369f6)

Developed by   : Almaas jahaan  
RegisterNumber : 212224230016



**Procedure**
1.Type the program in Quartus software.
2.Compile and run the program.
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram.
5.For different input combinations generate the timing diagram.

Write the detailed procedure here

**Program:**
```//Full adder

module full_add(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=(a^b^cin);
assign carry=((a&b)|((a^b)&cin));
endmodule
```

```
//Full subtractor

module full_sub(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=((~a&b)|(~(a^b)&bin));
assign borr=((~a&b)|(b&bin)|(~a&bin));
endmodule
```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**
1. FULL ADDER

![image](https://github.com/user-attachments/assets/715fd21c-6aa9-4f74-9e88-70224323c579)

2. FULL SUBSTRACTOR

![image](https://github.com/user-attachments/assets/91de6630-e9df-417a-ae26-759bd28f0200)


**Output Timing Waveform**

1. FULL ADDER

![image](https://github.com/user-attachments/assets/c735d513-d6d6-4f70-b2ed-97d5cb0ae49a)

2. FULL SUBTRACTOR

![image](https://github.com/user-attachments/assets/48694781-6b17-4907-99c7-1781cb068cb7)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




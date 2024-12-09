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

![Screenshot 2024-12-09 201848](https://github.com/user-attachments/assets/e9c69d2e-8803-4e5d-a517-0991e0b9f47f)


   FULL SUBTRACTOR
 ![Screenshot 2024-12-09 201856](https://github.com/user-attachments/assets/13a539e6-ae45-42f1-a054-952dfed71bfa)



**Procedure**
```
1 Type the program in Quartus software.
2 Compile and run the program.
3 Generate the RTL schematic and save the logic diagram.
4 Create the RTL schematic and save the logic diagram.
5 For different input combinations generate the timing diagram.
```

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

*/
```
i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^c);
assign carry= ( (a & b)| ( cin &(a ^ b ));
endmodule

ii)FULL SUBTRACTOR

module fs(a,b,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));
endmodule

```


Developed by: VISHAL.V


RegisterNumber:24900179


**RTL Schematic**

   FULL ADDER


![Screenshot 2024-12-09 201945](https://github.com/user-attachments/assets/8b792c2d-8bca-4553-b116-c9ac48862649)


   FULL SUBTRACTOR


![Screenshot 2024-12-09 201951](https://github.com/user-attachments/assets/6f2365bf-cdeb-46d4-a961-9bac567c8900)




**Output Timing Waveform**

   FULL ADDER

![Screenshot 2024-12-09 202006](https://github.com/user-attachments/assets/7285a028-ab06-4009-851b-7aca9a0c7ecc)

   FULL SUBTRACTOR


![Screenshot 2024-12-09 203013](https://github.com/user-attachments/assets/ff5cb32d-66a6-4379-b010-20cf8550c105)




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




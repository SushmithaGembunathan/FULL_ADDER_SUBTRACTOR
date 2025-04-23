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
![WhatsApp Image 2025-04-23 at 20 42 56_80cdeda5](https://github.com/user-attachments/assets/d005c781-c8c5-4a48-98e4-f0565b1e31d4)
![WhatsApp Image 2025-04-23 at 20 43 08_9a00aa66](https://github.com/user-attachments/assets/1bf29b26-41ae-4588-9ea2-29eeec8cdb05)

**Procedure**
```
1.Type the program in Quartus software.
2.Compile and run the program.
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram.
5.For different input combinations generate the timing diagram Program:
```
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
i)full adder
module exp4(
input a,b,c,
output sum,carry);
wire w1,w2,w3;
assign sum=a^b^c;
assign w1=a&b;
assign w2=b&c;
assign w3=c&a;
assign carry=w1|w2|w3;
endmodule

ii)full subtractor
module experiment4(a,b,c,diff,borr);
input a,b,c;
output diff,borr;
wire w1,w2,w3,w4,w5,w6;
xor g1(diff,a,b,c);
and g2(w4,w1,b);
and g3(w5,w1,b);
and g4(w6,b,c);
or g5(borr,w4,w5,w6);
endmodule

```



Developed by: Sushmtiha Gembunathan 
RegisterNumber:212224040342
*/

**RTL Schematic**

**Output Timing Waveform**
![WhatsApp Image 2025-04-23 at 20 43 31_aa7d79f9](https://github.com/user-attachments/assets/ddc23263-c1de-4209-9e98-fd7ec546b1bc)
![WhatsApp Image 2025-04-23 at 20 43 41_ad78b50f](https://github.com/user-attachments/assets/55180cb0-d628-4afb-abed-76242fa599b2)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




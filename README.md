# Developed by:Sanjushri.A
# Register number:212223040187
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

Full Adder
![image](https://github.com/Sanjushri13/FULL_ADDER_SUBTRACTOR/assets/164732231/61b75bae-0721-4fbf-b2d6-94faee3b5654)

Full Subtractor
![image](https://github.com/Sanjushri13/FULL_ADDER_SUBTRACTOR/assets/164732231/4451ea61-2bea-4709-b3b8-6446b5f01d6e)






**Procedure**
Full Adder:

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.

Full Subtractor:

1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR, AND, OR gates to perform subtraction.

4.Compile, simulate, implement, and program the design similarly to the full adder.




**Program:**
```
## Full_adder

module fullas(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        
and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);
or(carry,w2,w3,w4);
endmodule

## Full_subtractor

module fullas1(a, b, bin, diff, borrow);
input a, b, bin;
output diff, borrow;
wire w1, w2, w3, w4;   
xor(w1, a, b);
xor(diff, w1, bin);
and(w2, w1, bin);
and(w3, a, ~b);
and(w4, ~b, bin);
or(borrow, w2, w3, w4);
endmodule
```

**RTL Schematic**

# Full Adder
![image](https://github.com/Sanjushri13/FULL_ADDER_SUBTRACTOR/assets/164732231/606e7f68-5283-4fb1-a659-7a9b8c095953)
# Full Subtractor
![image](https://github.com/Sanjushri13/FULL_ADDER_SUBTRACTOR/assets/164732231/2d8ad317-3360-41fd-8c91-fe40150c236e)


**Output Timing Waveform**
# Full Adder
![image](https://github.com/Sanjushri13/FULL_ADDER_SUBTRACTOR/assets/164732231/18b71944-9748-4f93-b6ac-1b189353b8c2)
# Full Subtractor
![image](https://github.com/Sanjushri13/FULL_ADDER_SUBTRACTOR/assets/164732231/d30cabe9-e6e2-4248-afc0-f1f3f9376f70)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




## DEVELOPED BY:SANJUSHRI A
## REGISTER NO:212223040187
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

# Full Adder
![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/164732231/109a3099-ea5b-4650-960d-5c49e27b1955)

# Full Subtractor
![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/164732231/4d0ffacb-033c-416e-ae11-f45ce8224015)




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
## DEVELOPED BY:SANJUSHRI A
## REGISTER NO:212223040187
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
## Full Adder
![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/164732231/72f4c331-2502-44f7-8797-a52036895a1b)
## Full subtractor
![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/164732231/5debf799-f603-48cc-b549-49523a8a174a)




**Output Timing Waveform**
## Full Adder
![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/164732231/e2a733d1-5e52-4e15-8b61-38099a462dc9)
## Full Subtractor
![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/164732231/c52a20c5-51e6-4946-b355-a3369dc0f571)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**


**Procedure:**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by  : Ashwin Kumar A
RegisterNumber: 212223040021

```
module BOOLEAN(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
not(ydash,y);
and(s,ydash,z);
and(t,x,y);
and(u,w,y);
or(f2,s,t,u);
endmodule

```

**Truth Table:**

![image](https://github.com/AshwinKumar-Saveetha/BOOLEAN_FUNCTION_MINIMIZATION/assets/155129814/9555c47a-829a-4dd9-a3c6-eb01a6b69dd7)

![image](https://github.com/AshwinKumar-Saveetha/BOOLEAN_FUNCTION_MINIMIZATION/assets/155129814/8deb0241-f4f8-4555-acc5-2fbecdda3450)


**RTL:**
![image](https://github.com/AshwinKumar-Saveetha/BOOLEAN_FUNCTION_MINIMIZATION/assets/155129814/02963ae0-359f-4883-9cb6-f0d48d116a03)


**Output:**

![image](https://github.com/AshwinKumar-Saveetha/BOOLEAN_FUNCTION_MINIMIZATION/assets/155129814/f455a2c2-52cf-44de-aff6-9795f130fa7c)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.


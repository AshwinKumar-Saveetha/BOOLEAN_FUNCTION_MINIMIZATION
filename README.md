# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
Developed by: ASHWIN KUMAR A
RegisterNumber: 212223040021
//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
module boolean(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,p,q,r;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
wire ybar,M,N,O;
not(ybar,y);
and(M,w,y);
and(N,x,y);
and(O,z,ybar);
or(f2,M,N,O);
endmodule
```

**Output:**
![image](https://github.com/AshwinKumar-Saveetha/BOOLEAN_FUNCTION_MINIMIZATION/assets/155129814/e430862e-298a-4567-8a43-7b524470cf0f)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

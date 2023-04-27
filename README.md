# Experiment--02-Implementation-of-combinational-logic
# AIM:
To implement the given logic function and verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

F2=xy’z+x’y’z+w’xy+wx’y+wxy

# Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime

## Program:
~~~.py
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: NIROSHA.S
RegisterNumber:212222230097  

module logic(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire  A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1= (~a&(~b)&(~c)&(~d));
assign A2= (a&c&(~d));
assign A3= ((~b)&c&(~d));
assign A4= (~a&b&c&d);
assign A5= (b&(~c)&d);
assign F1= A1|A2|A3|A4|A5;
assign B1= (x&(~y)&z);
assign B2= (~x&(~y)&z);
assign B3= (~w&x&y);
assign B4= (w&(~x)&y);
assign B5= (w&x&y);
assign F2= B1|B2|B3|B4|B5;
endmodule	
~~~
## Output:
## RTL:

![image](https://user-images.githubusercontent.com/121418437/234773695-a001b973-165e-495d-9c14-1fe2766ff089.png)

![image](https://user-images.githubusercontent.com/121418437/234773778-5de0348f-12bb-489e-8492-61c9c97d884d.png)

## Timing Diagram:

![image](https://user-images.githubusercontent.com/121418437/234774005-15fe7a76-a2a2-42df-ae7c-71518f6505a8.png)

# Truth Table:


## Result:
Thus the given logic functions are implemented using logic gates.

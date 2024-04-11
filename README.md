# SIMULATE AND SYNTHESIS SR, JK, T, D - FLIPFLOP, COUNTER DESIGN USING VIVADO.
## AIM: 
  To simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using VIVADO.

 ## APPARATUS REQUIRED:
 VIVADO 2023.2

## PROCEDURE:
 STEP:1 Start the Vivado, Select and Name the New project.<br>
 STEP:2 Select the device family, device, package and speed. <br>
STEP:3 Select new source in the New Project and select Verilog Module as the Source type.<br>
STEP:4 Type the File Name and Click Next and then finish button. Type the code and save it.<br>
STEP:5 Select the Behavioural Simulation in the Source Window and click the check syntax.<br>
 STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.<br>











                

## SR FLIPFLOP:

![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/9bc25f0c-eacc-48f2-a0a9-d8eb5b90711d)


## PROGRAM:
module sr_ff(clk,q,rst,s,r);<br>
input s,r,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
begin<br>
case({s,r})<br>
2'b00:q=q;<br>
2'b01:q=1'b0;<br>
2'b10:q=1'b1;<br>
2'b11:q=1'bx;<br>
endcase<br>
end<br>
end<br>
endmodule<br>



## OUTPUT:               
                   
![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/c3b77772-5456-497c-9382-8db273e9448e)


## JK FLIPFLOP:

![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/f836cdf2-8f95-403b-b4b7-ed1a1fb8aec4)


## PROGRAM:
module jk_ff(clk,q,rst,j,k);<br>
input j,k,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
begin<br>
case({j,k})<br>
2'b00:q=q;<br>
2'b01:q=1'b0;<br>
2'b10:q=1'b1;<br>
2'b11:q=~q;<br>
endcase<br>
end<br>
end<br>
endmodule<br>

## OUTPUT:

![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/76d60cab-41f8-4e76-bc5c-2b9abb6eb335)


## T FLIPFLOP
	
![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/af11bd82-5024-4f61-b501-94e2e9e5c93c)


## PROGRAM: 
module t_ff(clk,q,rst,t);<br>
input t,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
if(t==0)<br>
q=q;<br>
else<br>
q=~q;<br>
end<br>
endmodule


## OUTPUT

 ![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/4dd88f8c-dd4e-4dc8-82ba-68f30dc35ddd)

                

## D FLIPFLOP:

![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/35cf7925-dc51-40b1-9e61-abef0abebf67)


## PROGRAM:
module d_ff(clk,q,rst,d);<br>
input d,clk,rst;<br>
output reg q;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1)<br>
q=1'b0;<br>
else<br>
q=d;<br>
end<br>
endmodule<br>

## OUTPUT:

![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/5e737a39-bbf3-47b8-8597-b02e386c3145)

## MOD 10 COUNTER
![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/f4343463-ce11-48a7-b325-44a0ef91db43)

## PROGRAM
module mod_10(clk,rst,out); <br>
input clk,rst; <br>
output reg[3:0]out;<br>
always@(posedge clk)<br>
begin<br>
if(rst==1|out==9)<br>
out=4'b0;<br>
else<br>
out=out+1;<br>
end<br>
endmodule<br>
## OUTPUT
![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/a0f63022-675d-4e0b-930b-c33e7b72960c)


## UP-DOWN-COUNTER
![image](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/bc7ff926-96b7-4e09-97f1-ac520feff5f3)
## PROGRAM
module updown_counter(clk,rst,ud,out); 
input clk,rst,ud; 
output reg[3:0]out;
always@(posedge clk)
begin
if(rst==1)
out=4'b0;
else if (ud==1)
out=out+1;
else if(ud==0)
out=out-1;
end
endmodule


## OUTPUT
![Screenshot 2024-04-02 134922](https://github.com/Udayabharathim/VLSI-LAB-EXP-4/assets/160568654/1a85e872-b2f8-4488-8d18-d9604d92bdde)



## RESULT:
	The simulate and synthesis SR, JK, T, D - FLIPFLOP, COUNTER DESIGN using VIVADO is successfully verified.


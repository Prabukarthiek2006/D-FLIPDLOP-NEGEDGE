# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

 1.Type the program in Quartus software.
 
 2.Compile and run the program.
 
 3.Generate the RTL schematic and save the logic diagram.
 
 4.Create nodes for inputs and outputs to generate the timing diagram.
 
 5.For different input combinations generate the timing diagram

**PROGRAM**
```
module Dflipflop(d, clk, rst, q, qbar); 
    input d; 
    input clk; 
    input rst; 
    output q; 
    output qbar; 
  reg q; 
  reg qbar; 
    always @ (posedge(clk) or posedge(rst)) begin 
    if (rst==1'b1) 
  begin 
  q=1'b0; 
  qbar=1'b1; 
  end 
   else if (d==1'b0) 
  begin 
  q=1'b0; 
  qbar=1'b1; 
  end 
   else 
  begin 
  q=1'b1; 
  qbar=1'b0; 
  end   
  end    
  endmodule
```
 Developed by:Prabu Karthiek B RegisterNumber:24010663


**RTL LOGIC FOR FLIPFLOPS**
![WhatsApp Image 2024-12-20 at 10 19 20 PM](https://github.com/user-attachments/assets/fe6fc9f8-c7b4-4022-8255-bedeeb907b53)


**TIMING DIGRAMS FOR FLIP FLOPS**
![WhatsApp Image 2024-12-20 at 10 19 20 PM (1)](https://github.com/user-attachments/assets/d987fc58-b15f-4f26-a603-5debe150656d)



**RESULTS**
Hence ,program for flipflops and its truthtable is verified. Hence the program to verify flipflops and its truth table using verilog programming is verified.

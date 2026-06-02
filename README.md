# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

1.Increment count on each positive edge of the clock.

2.Reset count to zero when it reaches 15.

3.Generate clock signal (clk).

4.Instantiate the RippleCounter module.

5.Conduct functional testing by displaying the count at each clock cycle for 16 cycles.



**PROGRAM**
```
/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by: PRAVEEN KUMAR K
 RegisterNumber: 212225230216
 module bitripple(
   input  wire clk,      
   input  wire reset_n,  
   output reg  [3:0] q   
);


   always @(negedge clk or negedge reset_n) begin
       if (!reset_n)
           q[0] <= 1'b0;
       else
           q[0] <= ~q[0];
   end


   always @(negedge q[0] or negedge reset_n) begin
       if (!reset_n)
           q[1] <= 1'b0;
       else
           q[1] <= ~q[1];
   end


   always @(negedge q[1] or negedge reset_n) begin
       if (!reset_n)
           q[2] <= 1'b0;
       else
           q[2] <= ~q[2];
   end


   always @(negedge q[2] or negedge reset_n) begin
       if (!reset_n)
           q[3] <= 1'b0;
       else
           q[3] <= ~q[3];
   end

endmodule

*/
```

**RTL LOGIC FOR 4 Bit Ripple Counter**

<img width="1045" height="553" alt="image" src="https://github.com/user-attachments/assets/65e55e00-4914-48fe-ae91-c2007c301362" />


**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

<img width="1058" height="546" alt="image" src="https://github.com/user-attachments/assets/f7aa45c2-d43c-43a0-82c4-33c5658b9e8f" />


**RESULTS**

Thus the program executed succesfully

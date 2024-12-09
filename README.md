### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

/* write all the steps invloved */

1.Open quartus II and create New project wizard.
2. Write the program in Verilog HDL file and run the program.
3. Download the RTL viewer 
4. Now open university program VWF and download waveform after the execution.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

module exp_11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @(posedge clk)
begin
  if(!rstn)
    out<=0;
  else
    out<= out+1;
end 
endmodule

Developed by: V.Shriyha 
RegisterNumber: 24007606

**RTL LOGIC UP COUNTER**

![WhatsApp Image 2024-12-09 at 13 27 38_f0b25b02](https://github.com/user-attachments/assets/48f4ec55-1d85-4fde-899c-1d210fe392b6)


**TIMING DIAGRAM FOR IP COUNTER**

![WhatsApp Image 2024-12-09 at 13 27 38_f0b25b02](https://github.com/user-attachments/assets/31ccdcf2-a3d9-4cd8-ae77-5ed51bf9106a)


**RESULTS**

Thus the 4 bit synchronous up counter is executed and the truth table is verified.

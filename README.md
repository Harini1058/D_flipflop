# D_flipflop
# AIM:

To implement D flipflop using verilog and validating their functionality using their functional tables

# SOFTWARE REQUIRED:

Quartus prime

# THEORY

# D Flip-Flop

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

<img width="749" height="382" alt="Screenshot 2025-12-15 175120" src="https://github.com/user-attachments/assets/61d00a52-119f-4ed9-801e-6787eb13784b" />


This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

<img width="495" height="199" alt="Screenshot 2025-12-15 175127" src="https://github.com/user-attachments/assets/af8a5f0d-00f8-4e75-8463-553867909412" />


Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

<img width="482" height="268" alt="Screenshot 2025-12-15 175135" src="https://github.com/user-attachments/assets/bef4301c-97ea-4f5e-b8c1-edf517b2db5a" />


Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

# Procedure

1.Define Module: Define a Verilog module for the D flip-flop with inputs (D, CLK) and outputs (Q, Q_bar).

2.Declare Inputs and Outputs: Declare input and output ports for the module.

3.Implement Flip-Flop Logic: Write Verilog code to implement the D flip-flop logic based on its functional table. Use a synchronous always @(posedge CLK) block to trigger the flip-flop on the positive edge of the clock signal.

4.Simulate Using Testbench: Write a Verilog testbench to simulate the behavior of the D flip-flop under different input conditions.

5.Apply Input Stimuli: In the testbench, apply various combinations of input stimuli (D, CLK) to cover all possible input states.

6.Verify Output Behavior: Verify that the output behavior of the D flip-flop matches the expected behavior defined by its functional table.

7.Check for Race Conditions: Ensure that there are no race conditions or undefined states in the design by analyzing the timing and sequence of input changes.

# PROGRAM

# Developed by: HARINI G
# RegisterNumber: 25015377

module D_flipflop (

    input  wire clk, rst, D,
    
    output reg  Q
    
);

    always @(posedge clk or posedge rst) begin
    
        if (rst)
        
            Q <= 1'b0;  
            
        else
        
            Q <= D;      
            
    end
    
endmodule

# RTL LOGIC FOR FLIPFLOPS

<img width="1127" height="663" alt="Screenshot 2025-12-15 110002" src="https://github.com/user-attachments/assets/adb2ac15-03cc-4282-9df1-ef2e6d817442" />


# TIMING DIGRAMS FOR FLIP FLOPS

<img width="1878" height="951" alt="Screenshot 2025-12-15 114808" src="https://github.com/user-attachments/assets/bd2f3623-005b-42d4-bc5e-d8b221223fc4" />

# RESULTS

Thus the program to implement a D flipflop using verilog and validating their functionality using their functional tables

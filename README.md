# JK_FLIPFLOP
# Aim:
To simulate and synthesis JK flipflop using vivado

# Apparatus Required:
Vivado 2023.3

# Procedure:
STEP:1 Start the Xilinx navigator, Select and Name the New project.
STEP:2 Select the device family, device, package and speed.
STEP:3 Select new source in the New Project and select Verilog Module as the Source type.
STEP:4 Type the File Name and Click Next and then finish button. Type the code and save it. 
STEP:5 Select the Behavioral Simulation in the Source Window and click the check syntax.
STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.
STEP:7 Select the Implementation in the Sources Window and select the required file in the Processes Window.
STEP:8 Select Check Syntax from the Synthesize XST Process. Double Click in the FloorplanArea/IO/Logic-Post Synthesis process in the User Constraints process group. UCF(User constraint File) is obtained.
STEP:9 In the Design Object List Window, enter the pin location for each pin in the Loc column Select save from the File menu.
STEP:10 Double click on the Implement Design and double click on the Generate Programming File to create a bitstream of the design.(.v) file is converted into .bit file here. 
STEP:11 On the board, by giving required input, the LEDs starts to glow light, indicating the output.

![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/094e9d55-5f30-4984-90b9-dd51d5297974)
# Circuit Diagram
![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/5b973ee8-9ee2-402d-8cba-1adfa2e4d5f2)
# Truth Table
![image](https://github.com/RESMIRNAIR/JK_FLIPFLOP/assets/154305926/04d4ff52-ae20-4e08-bd70-58137b129890)

# Program:
```
module jkff(clk,j,k,rst,q );
input j,k,clk,rst;
output reg q;
always@(posedge clk)
begin
if(rst==1)
q=1'b0;
else
begin
case({j,k})
2'b00: q=q;
2'b01:q=1'b0;
2'b10:q=1'b1;
2'b11:q=~q;
endcase
end
end
endmodule
```
# Output:
![WhatsApp Image 2024-05-11 at 21 46 33_636d2f9e](https://github.com/S-Mohankumar/JK_FLIPFLOP/assets/163832108/9abe765a-a432-4a89-ac15-56d16e048518)
# Result:
Thus the verilog program for JK flipflop has been simulated and verified successfully.


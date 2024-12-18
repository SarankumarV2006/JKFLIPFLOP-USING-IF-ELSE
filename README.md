# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.


![Screenshot 2024-12-18 202817](https://github.com/user-attachments/assets/6ff996ee-c366-48d5-b3e9-796a39c69f54)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![Screenshot 2024-12-18 203046](https://github.com/user-attachments/assets/57bae1a4-f678-446e-aa73-f26d8a64682d)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 

![Screenshot 2024-12-18 203057](https://github.com/user-attachments/assets/1356d18d-6a66-4362-9ddc-fcb316c32859)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![Screenshot 2024-12-18 203109](https://github.com/user-attachments/assets/225779ec-4bb8-48b3-b8a2-946b463038d6)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.


**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by:Sarankumar.V RegisterNumber:24010668
```
module jkflipflop(j,k,clk,q,qbar);
input j,k,clk;
output reg q,qbar;
initial
begin
q=1'b0;
q=1'b1;
end
always @(posedge clk)
begin
q<=(j&~q)|(~k&q);
qbar<=~q;
end
endmodule
```


**RTL LOGIC FOR FLIPFLOPS**

**TIMING DIGRAMS FOR FLIP FLOPS**

![Screenshot 2024-12-18 203123](https://github.com/user-attachments/assets/eba41f55-34e7-49ae-be7f-b3eee8bacf70)

**RESULTS**
Thus the truth table of JKFLIPFLOP in Quartus II using Verilog programming are studied, verified and executed successfully.

🔄 Pipelined ALU with Two-Phase Non-Overlapping Clocks in Verilog
This project implements a 4-stage pipelined ALU (Arithmetic Logic Unit) in Verilog using non-overlapping two-phase clocks (clk1 and clk2). The design demonstrates fundamental concepts of digital system design, pipelining, data forwarding, and memory/register interfacing — ideal for computer architecture or VLSI-based academic labs and simulations.

This project demonstrates a **4-stage pipelined ALU** (Arithmetic Logic Unit) implemented in **Verilog** using **non-overlapping two-phase clocks**. It showcases key digital design principles such as pipelining, clock domain separation, and ALU operation modeling. Perfect for academic labs in VLSI or computer architecture courses.

## ⚙️ Features

- 🔀 **4-stage pipeline** with clean data flow and register hand-off  
- ⏱️ **Two-phase non-overlapping clocks** (clk1 and clk2)  
- 🧮 Supports **12 ALU operations**
- 📥 Register file → ALU → Register file → Memory
- 🧪 Complete **testbench** with memory dump for verification

⚠️ Operation structure
Stage 1 Stage 2 Stage 3 Stage 4

Reg Read → ALU Compute → Reg Write → Memory Write
(clk1) (clk2) (clk1) (clk2)

📁 Project Structure
pipeline_ALU.v     // Main pipelined ALU design
pipe_ALU_tb.v      // Testbench to simulate and verify functionality

⚙️ Key Features
4-stage pipelined design:

Stage 1: Register fetch (reads operands from register bank)

Stage 2: Execution (performs ALU operations)

Stage 3: Write-back to register bank

Stage 4: Memory write

Functional coverage for common ALU operations: ADD, SUB, MUL, AND, OR, XOR, NOT, SHIFT, etc.

Two-phase clocking: Uses non-overlapping clocks clk1 and clk2 for modeling pipelined behavior without hazards.

Simulation-Ready Testbench: Fully functional testbench with:

Register file initialization

Sequence of ALU instructions

Final memory dump for validation

🧠 ALU Operation Codes (func input)
Code	Operation
0:	A + B
1:	A - B
2:	A * B
3:	A
4:	B
5:	A & B
6:	A | B
7:	A ^ B
8:	~A
9:	~B
10:	A >> 1
11:	A << 1

🧪 How to Run
Open the files in a Verilog simulator like ModelSim, Vivado, Icarus Verilog, or EdaPlayground.

Compile both files:

📊 Sample Output
bash
Copy
Edit
mem[125] =  8
mem[126] = 24
mem[128] = -16
mem[127] = 14
mem[129] = -16
mem[130] = 38

✅ Learning Outcomes
Pipelining in digital systems

Clock domain modeling with two-phase clocks

ALU operation implementation in hardware description languages

Understanding of register-memory data transfer

Simulation and debugging of RTL code

🧠 Author
LIJIN WILSON
MTech - VLSI Design
Experienced in Verilog, Cadence, Visual TCAD

📌 License
This project is open-source and free to use for academic and educational purposes.

🎯 Learning Objectives
✅ Understand pipelined hardware design

✅ Learn two-phase clock synchronization

✅ Implement ALU operations in Verilog

✅ Register/memory interface modeling

✅ Verilog testbench and simulation




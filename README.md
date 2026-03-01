# 32-bit-ALU-with-RAM-PC-CU
1) ALU (Arithmetic Logic Unit)

What it is: A digital circuit that performs arithmetic (add/sub) and logical (AND/OR/XOR) operations.

Role: Takes two 32-bit inputs and a control code, computes the result based on the opcode.

Why it matters: This is where all the “math and logic” happens in your processor.

2) RAM (Memory)

What it is: Temporary storage where data values (like results of ALU operations) can be stored and retrieved.

Role in your design: Stores ALU results at an address; always outputs the value at that address.

Why it matters: Without memory you can’t save or reuse results across cycles.

3) Program Counter (PC)

What it is: A register that holds the address of the next instruction to execute.

Role: On reset sets PC to 0; otherwise increments by 4 each clock tick to simulate instruction sequencing.

Why it matters: It keeps track of where you are in the instruction stream.

4) Control Unit

What it is: Logic that decodes the opcode and tells the ALU what operation to perform.

Role: Maps 3-bit instruction opcodes to ALU control codes (ADD, SUB, AND, OR, etc.).

Why it matters: It translates instruction bits into actual functional behavior.

5) Top Module (Integration)

What it is: Your CPU “system” wiring together ALU, RAM, Control Unit, and PC.

Role:

ALU computes results based on opcode and inputs,

RAM writes and reads those results,

PC tracks instruction flow,

Control Unit drives ALU selection.

Why it matters: This is a simplified CPU datapath — the essential hardware that executes instructions.

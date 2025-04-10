### **Day 30: RAM Design (Read/Write Operations)**

#### **Concept Overview**  
**RAM (Random Access Memory)** is a volatile memory where data can be **read from and written to at random addresses**. It is a fundamental memory component in digital systems. RAM modules are synchronous and use control signals like `write enable (we)` and `chip enable (ce)`.

#### **Types of RAM**  
- **Static RAM (SRAM):** Faster, used in caches  
- **Dynamic RAM (DRAM):** Slower but denser, used in main memory  
For this design, we focus on a basic **synchronous SRAM** model in Verilog.

#### **Features of RAM**  
- **Addressable locations**  
- **Read and Write operations**  
- **Synchronous with clock**  
- Data width and address width define the size

#### **Block Diagram Description**  
Inputs: `clk`, `we`, `addr`, `data_in`  
Outputs: `data_out`  
Behavior:  
- When `we=1`, data is written to the memory location  
- When `we=0`, data is read from the memory location

#### **Applications**  
- Caches and buffers  
- Registers and lookup tables  
- Any temporary storage in computing systems

#### **Execution Steps**  
1. Define the memory array  
2. Create read/write logic  
3. Use control signals (`we`, `clk`)  
4. Test with various read/write scenarios  


#### **Expected Output Behavior**  
- Writes `AA`, `55`, `FF` to locations 0, 1, 2  
- Reads the same values back when `we=0`

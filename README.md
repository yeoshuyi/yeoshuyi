# Welcome to my GitHub Repository :)
> I am a freshman EEE student interested in RTL and embedded systems design.

## Current Projects (Hardware Discriptive Language)
### Custom RISC-V Processor Core on Xilinx Spartan-7 FPGA with SystemVerilog
* Implemented all basic RV32I instructions in testbench.
* Not able to meet timing closure yet, undergoing optimization.
> Currently uses single cycle datapath (Planning to pipeline to 5 stages).

### Custom 6M Baud Rate UART Transciever on Xilinx Spartan-7 FPGA with Verilog
* Uses 16x Oversampling with PLL synthesized 288MHz clock.
* Uses asynchronous speculative FIFO with FWFT with 2-FF CDC.
* Speculative FIFO operates with a 3 pointer system, with commit and rollback.
* Pointers are gray-coded before crossing between 288MHz to 100MHz domain.
* Field tested against ESP-32 as communication master. Signals measured on logic analyzer.
> Currently working to reduce BER, possibly through implmenetation of 32x oversampling with majority.

## Current Projects (NOT HDL hahaha)
### Maze Encoder and Solver
* Experimented with creating my own instruction set that encodes instructions to construct a 30x30 maze with gems, monsters and hearts.
* Maze encoder convers a 30x30 pixel .png file to a .bin file based on the custom 32-bit instruction set.
* Maze solver that takes in the .bin file and solves the maze via BFS, DFS and A*STAR.

### AI Application in ESP-32 (For BeyondBinary Hackathon)
* Handled high-throughput memory management for the project on ESP-32.
* Implemented pseudo FIFO buffer with FWFT and bypass for incoming UART data.
* Implemented interrupt code for high-priority alert signals from UART recieve.

### Optimized Random Number List Generator
* Random project to optimize time complexity of RNG.
* Produced a O(log N) C++ buffer based random list generator.
* Reduced time to execution from 1600us to 0.3us

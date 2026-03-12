# Welcome to my GitHub Repository :)
> I am a freshman EEE student interested in RTL and embedded systems design.

## Current Projects
### 25GbE Ethernet Header Ascon-Hash at Line Rate for Post-Quantum HashDos Protection on Kintex UltraScale+ SmartNIC
* Implemented 7-Clock Cycle Ascon-Hash, verified agaist golden results using cocotb and known Ascon library.
* Ascon-Hash uses Ascon-p[12], with 2 rounds of absorbtion for the 104bit header, and squeezes the first H0 for arbiter.
* Algorithm runs parallel to NIC's hot path, with sufficient performance to avoid backpressure even at worst case transmissions.
* Built upon Corundum's Open Source NIC project for the AS02MC04 card.
* Currently working on wrapper for Corundum integration.

### RISC-V Processor Core on Xilinx Spartan-7 FPGA with SystemVerilog
* Implemented all basic RV32I instructions in testbench.
* Not able to meet timing closure yet, undergoing optimization.

### 6M Baud Rate UART Transciever on Xilinx Spartan-7 FPGA with Verilog
* Uses 16x Oversampling with PLL synthesized 288MHz clock.
* Uses asynchronous speculative FIFO with FWFT with 2-FF CDC.
* Speculative FIFO operates with a 3 pointer system, with commit and rollback.
* Pointers are gray-coded before crossing between 288MHz to 100MHz domain.
* Field tested against ESP-32 as communication master. Signals measured on logic analyzer.

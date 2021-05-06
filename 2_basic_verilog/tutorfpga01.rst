###################
FPGA and Red Pitaya
###################

In a project of a digital system the developer studies a problem and builds a combination of logic gates, registers, flip-flops, and more complex blocks like RAM, ROM, processors, etc.  Today with the advance of the technology we can implement the project with a FPGA (Field Programmable Gate Array). The FPGA is made with lots of logic blocks and each block contains logic gates, multiplexers, registers, etc. To implement the project the user of the FPGA has to make connections between these logic blocks and this is done with a HDL (Hardware Description Language). 

Red Pitaya uses Verilog and System Verilog as a HDL. The Red Pitaya board has a programmable logic made by Xilinx and to write it to describe your digital system you must use the software Vivado. Vivado is used to write your digital system with a HDL and to implement your system in the programmable logic. The result of the implementation of a Vivado project is a file called bitstream that has an extension .bit, that has the information about the connections of logic blocks that will be used and the connections between them.

Every application of Red Pitaya (Osciloscope, Signal Generator, etc) uses a specific bitstream file, that implements the digital system needed for the application.
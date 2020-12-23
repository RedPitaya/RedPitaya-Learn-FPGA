################
Simple Examples
################

=====================
A simple LED blinker
=====================

This is the simplest example – a hardware equivalent of the Hello World – LED blink. There is no need to know any 
hardware description language ( HDL ), like VHDL or verilog for this example.

More details can be found `here <http://antonpotocnik.com/?p=487360>`__.

====================
Knight Rider Lights
====================

This example introduces the basic concepts of FPGA programming, you  will get familiar with Verilog language which
will be used to create your own module. Testing will be done in Vivado’s simulator.

More details can be found `here <http://antonpotocnik.com/?p=488784>`__.

==========
Stopwatch
==========
This example shows how communication between the Linux processing system and the programmable logic works. 

More details can be found `here <http://antonpotocnik.com/?p=489265>`__.

==================
Frequency Counter
==================
This example demonstraits how to use Red Pitaya’s 125 Msamples/s 14-bit ADC and DAC peripherals with the FPGA.

More details can be found `here <http://antonpotocnik.com/?p=519284>`__.

================
Pulse generator
================

This example demonstraits how to build a simple pulse generator for the Red Pitaya. The design uses standard Xilinx IP
blocks and a custom Verilog core that outputs a signal valid that is driven high when the pulse is played on the DAC.

Pulse shape is stored in a Block RAM that can be written from Linux. ADC data is written in a FIFO that can be read 
from Linux. The FIFO only accepts ADC data when a pulse is played on the DAC.

More details can be found `here <https://www.koheron.com/blog/2016/10/13/pulse-generator.html>`__.


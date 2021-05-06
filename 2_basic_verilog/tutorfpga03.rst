################
Values
################

Port Types
==========

The port types can be, **input**, **output** and **inout**.

Data Types
==========

There are two types of data in Verilog, one is called **net** and the other is called **reg**.  A reg declaration is used to store some temporary data and a net is used to connect blocks and processes. 

Net
---

Net declarations can be **wire** , **tri**, **supply0** and **supply1**. 

=======   ===============================
wire      represents a node or connection
tri       represents a tri-state node
supply0   represents the logic 0
supply1   represents the logic 1
=======   ===============================

Reg
---

Reg declarations can be **reg** , **integer**, **time** and **realtime**. A variable of type reg can be designated only by a procedure statement, task, or function. A variable of type reg cannot be the output of a port or an **assign** statement.

Data Input Output Rules
=======================

If you have a variable of type net, it can be declared as **input**, **output**, or **inout**. A variable of type **reg** can only be declared of type **output**.

Assign Values
=============

In Verilog numbers can be assigned with size or not. If it is not declared the size it defaults to 32 bits. Also you must choose the base of the number and the options are decimal, hexadecimal, octal and binary. If not specified the base it defaults to the decimal base.

Examples:

122 - Unsized number with no base, so it is a 32 bit wide number with the value 122 in the decimal base.

3'b010 - 3 bit wide with the value 010 in base two or 2 in decimal base.

8'hAA- 8 bit wide with the value AA in the hexadecimal base.

6'o77 - 6 bit wide with the value 77 in the octal base.

'b010 - 32 bit wide with the value 2 in the decimal base.

'd2 - Same as before.

Negative Numbers
================

Negative numbers are stored as compliment two and the minus sign must be included before the specification of size.

Example: 

-10'd5 10 bit number stored as complement two of 5.

10'd-5 Illegal representation.

Special Number Characters 
=========================

========= ============================  ===============
Character Function                      Example
_         used for readability          16'h15_ab_cd_ef
x or X    specify unknown bits          16'h15abx
z or Z    specify high impedance value  16'hz
========= ============================  ===============


References
==========

Verilog HDL Basics - Altera

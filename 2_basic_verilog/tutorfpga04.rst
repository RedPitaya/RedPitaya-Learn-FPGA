###################
Operators
###################

Arithmetic Operators
====================

For the FPGA, division and multiplication are very expensive and sometimes you cannot synthesize division. If you use Z or X for values the result is unknown. The operations treat the values as unsigned. If a = 5, b=10, c=2'b01 and d = 2'b0Z . 

========= ============================  ==================
Character Operation performed           Example
\+        Add                           b + c = 11
\-        Subtract                      b - c = 9, -b=-10
\/        Divide                        b / a = 2
\*        Multiply                      a * b = 50
%         Modulus                       b % a = 0
========= ============================  ==================

Bitwise Operators
=================

Each bit is operated, result is the size of the largest operand and  the smaller operand is left extended with zeroes to the size of the bigger operand. If a = 3'b101, b=3'b110 and c=3'b01X .

========= ============================  ==================
Character Operation performed           Example
\~        Invert each bit               ~a = 3'b010
\&        And each bit                  b & c = 3'b010
\|        Or each bit                   a | b = 3'b111
\^        Xor each bit                  a ^ b = 3'b011
\^~ or ~^ Xnor each bit                 a ^~ b = 3'b100
========= ============================  ==================

Reduction Operators
===================

These operators reduces the vectors to only one bit. If there are the characters z and x the result can be a known value. If a = 5'b10101, b = 4'b0011, c = 3'bz00 and d = 3'bx011 .

========= ============================  ====================
Character Operation performed           Example
\&        And all bits                  &a = 1'b0, &d = 1'b0
\~&       Nand all bits                 ~&a = 1'b1
\|        Or all bits                   |a = 1'b1, |c = 1'bX
\~|       Nor all bits                  ~|a= 1'b0
^         Xor all bits                  ^a = 1'b1
\^~ or ~^ Xnor all bits                 ~^a = 1'b0
========= ============================  ====================

Relational Operators
====================

These operators compare operands and results a 1 bit scalar boolean value. The case equality and inequality operators can be used for unknown or high impedance values (z or x) and if the two operands are unknown the result is a 1. If a = 3'b010, b = 3'b100, c = 3'b111, d = 3'b01z and e = 3'b01X .

========= ============================  ====================
Character Operation performed           Example
\>        Greater than                  a > b = 1'b0
\<        Smaller than                  a < b = 1'b1
\>=       Greater than or equal         a >= d = 1'bX
\<=       Smaller than or equal         a <= e = 1'bX
\==       Equality                      a == b = 1'b0
\!=       Inequality                    a != b = 1'b1
\===      Case equality                 e === e = 1'b1
\!===     Case inequality               a !== d = 1'b1
========= ============================  ====================

Logical Operators
=================

These operators compare operands and results a 1 bit scalar boolean value. If a = 3'b010 and b = 3'b000.

========= ============================= ====================
Character Operation performed           Example
\!        Not true                      !(a && b) = 1'b1
\&&       Both expressions true         a && b = 1'b0
\||       One ore both expressions true a || b = 1'b1
========= ============================= ====================

Shift Operators
===============

These operators shift operands to the right or left, the size is kept constant, shifted bits are lost and the vector is filled with zeroes. If a = 4'b1010 and b = 4'b10X0.

=========  ============================= ======================
Character  Operation performed           Example
\>>        Shift right                   b >> 1 results 4'b010X
\<<        Shift left                    a << 2 results 4'b1000
=========  ============================= ======================

Other Operators
===============

These are operators used for condition testing and to create  vectors. If a = 4'b1010 and b = 4'b10X0.

=========  ============================= ======================
Character  Operation performed           Example
?:         Conditions testing            test cond. ? if true do this : if not do this
{}         Concatenate                   c = {a,b} = 8'101010x0
{{}}       Replicate                     {3{2'b10}}= 6'b101010
=========  ============================= ======================

Operators Precedence
====================

The order of the table tells what operation is made first, the first ones has the highest priority. The () can be used to override default.

+---------------------+
|Operators precedence |
+=====================+
| +, -, !, ~ (Unary)  |
+---------------------+
| +,- (Binary)        |
+---------------------+
| <<, >>              |
+---------------------+
| <,>,<=,>=           |
+---------------------+
| ==, !=              |
+---------------------+
| &                   |
+---------------------+
| ^, ^~ or ~^         |
+---------------------+
| \|                  |
+---------------------+
| &&                  |
+---------------------+
| ||                  |
+---------------------+
| ?:                  |
+---------------------+

References
==========

Verilog HDL Basics - Altera

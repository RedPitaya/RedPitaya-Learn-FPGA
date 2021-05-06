Mathematical Operations with the Binary Base
############################################


Operations with binary base are equal the decimal base. The difference is when we need to store numbers in a finite amount of bits. Let’s do some operations with 8 bits, where the MSB is the signal bit and the others 7 bits are the bits of numerical value.

Sum
===

104\ :sub:`10`\ + 2\ :sub:`10`\ = 0110 1000\ :sub:`2`\ + 0000 0010\ :sub:`2`\ = 0110 1010\ :sub:`2`\ = 106\ :sub:`10`\  

As the result isn’t greater than 0111 1111\ :sub:`2`\ , for this operation didn’t occurred overflow.

104\ :sub:`10`\ + 24\ :sub:`10`\ = 0110 1000\ :sub:`2`\ + 0001 1000\ :sub:`2`\ =  1000 0000\ :sub:`2`\ = 0\ :sub:`10`\  

As the result is greater than 0111 1111\ :sub:`2`\ the result is wrong and occurred overflow.

Subtraction
===========

-104\ :sub:`10`\ - 2\ :sub:`10`\ = -(104\ :sub:`10`\ + 2\ :sub:`10`\ )= -(0110 1000\ :sub:`2`\ + 0000 0010\ :sub:`2`\) = 1110 1010\ :sub:`2`\= - 106\ :sub:`10`\    

As the result isn’t greater than 0111 1111\ :sub:`2`\ , for this operation didn’t occurred overflow.

-104\ :sub:`10`\ - 24\ :sub:`10`\ = -(104\ :sub:`10`\ + 24\ :sub:`10`\ ) = -(0110 1000\ :sub:`2`\ + 0001 1000\ :sub:`2`\) = 1000 0000\ :sub:`2`\   

As the result is greater than 0111 1111\ :sub:`2`\  the result is wrong and occurred overflow.

-104\ :sub:`10`\ + 24\ :sub:`10`\ = -(104\ :sub:`10`\ - 24\ :sub:`10`\ ) = -(0110 1000\ :sub:`2`\ - 0001 1000\ :sub:`2`\) = 1101 0000\ :sub:`2`\   

Multiplication
==============

2\ :sub:`10`\ * 60\ :sub:`10`\ = 0000 0010\ :sub:`2`\ * 0011 1100\ :sub:`2`\ = 0111 1000\ :sub:`2`\ = 120\ :sub:`10`\

-2\ :sub:`10`\ * 60\ :sub:`10`\ = -0000 0010\ :sub:`2`\ * 0011 1100\ :sub:`2`\ = -0111 1000\ :sub:`2`\ = 1111 1000\ :sub:`2`\ = - 120\ :sub:`10`\

In none of the cases occurred overflow.

Division
========

60\ :sub:`10`\/2\ :sub:`10`\ = 0011 1100\ :sub:`2`\ / 0000 0010\ :sub:`2`\ = 0001 1110\ :sub:`2`\ = 30\ :sub:`10`\

If the division results in a decimal number, the decimal places are discarded.

Two Complement
==============

The way we do arithmetic operations in a paper, adding transport numbers and deciding which number is greater to change the signal and perform a subtraction, is difficult to implement in a digital system. To overcome that there is another way to represent finite binary numbers and it’s called two complement. It is easier to perform calculations of sum and subtraction using two complement representation.

First we define with how many bits we are working. After that we perform an operation to find the two complement of a negative number. If you have to do the complement of a number x of n bits, the operation is this, y\ :sub:`2`\ = ( :math:`2^n` - x)\ :sub:`2`\. For example we are working with 3 bits and we want to know the two complement of -010\ :sub:`2`\, doing the operation,

y\ :sub:`2`\  = 1000\ :sub:`2`\  – 010\ :sub:`2`\  = 110\ :sub:`2`\ , and this is -010\ :sub:`2`\  represented in two complement.

Adding and subtracting numbers is easy.

3\ :sub:`10`\  – 2\ :sub:`10`\  = 011\ :sub:`2`\  – 010\ :sub:`2`\  = 011\ :sub:`2`\  + (1000\ :sub:`2`\  - 010\ :sub:`2`\ ) =011\ :sub:`2`\  + 110\ :sub:`2`\  = 1001\ :sub:`2`\  = 010\ :sub:`2`\ , in this case we have to discard the MSB, the result is correct as the operands had different sign.

3\ :sub:`10`\  +2\ :sub:`10`\  = 011\ :sub:`2`\  + 010\ :sub:`2`\  = 101\ :sub:`2`\  , the result is wrong as the sign of the operand are equal and the sign of the result is different, occurred overflow.

-3\ :sub:`10`\  – 2\ :sub:`10`\  = 101\ :sub:`2`\  + 110\ :sub:`2`\  = 1011\ :sub:`2`\  , the result is wrong as the sign of the operand are equal and the sign of the result is different, occurred overflow.

-3\ :sub:`10`\  – 1\ :sub:`10`\  = 101\ :sub:`2`\  + 111\ :sub:`2`\  = 1100\ :sub:`2`\  = 100\ :sub:`2`\ , the result is correct as the sign of the operand are equal and the sign of the result is equal.

=============   =====================
Binary number	3 bits complement two
=============   =====================
011	        011
010	        010
001	        001
000	        000
100	        111
101	        110
110	        101
111	        100
=============   =====================

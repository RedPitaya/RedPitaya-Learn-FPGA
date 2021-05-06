Digital Information and Numerical Bases
#######################################


Digital Information
===================

The information is represented by numbers written in a digital way. Why digital? When you have finite components to store information, it must be written digitally, that is what your calculator does. It always store a finite amount of numbers, so for infinite numbers like 5.444… and if your calculator has 3 significant digits it rounds to 5.44. Otherwise if you represent a number infinitely it is represented analogically, and that is the case of the infinity number 5.444… .

Representation of Numbers
=========================

We commonly store the numbers in a decimal base, because of our ten fingers. But the numbers can be represented in other bases like binary, octal and hexadecimal. These bases are multiple of two and have many advantages to be used. Our computers, processors and digital systems stores the numbers in a binary base. In a digital system the bases are represented by voltage levels, like 0, 3.3V, 5V. The algorism that has more value, the one that is written in the left is said as the most significant algorism. The one of less value that is written in the right is the less significant algorism. In the binary base these names are called often and the most significant algorism is the most significant bit (MSB) and the less significant algorism is the less significant bit (LSB). First let’s start with the decimal base.

Decimal Base
------------

0, 1, 2, 3, 4, 5, 6, 7, 8 and 9 forms the decimal base. To represent this base in an electrical system we would have ten different voltage levels. A number greater than nine and numbers smaller than one need others algorisms to be represented. For example let’s write the number 11.5.

:math:`1*10^1 + 1*10^0 + 5*10^{-1}` =  11.5\ :sub:`10`\

In base ten the number is wrote like this, 11.5\ :sub:`10`\.

Binary Base
-----------

0 and 1 forms the binary base. These are called bits and if a number in this base has n algorisms then it is said that it have n bits. To represent this base in an electrical system we would have two different voltage levels. A number greater than one and smaller than one need more than one algorism to be represented. For example 11.5\ :sub:`10`\  in base two is represented as 1011.1\ :sub:`2`\,

:math:`1*2^3+0*2^2+1*2^1+1*2^0 + 1*2^{-1}` = 1011.1\ :sub:`2`\ = 11.5\ :sub:`10`\

Multiplications and divisions in this base by two are simple. If you multiply by two you rotate the number to the left and if you divide by two you rotate it to the right, for example:

:math:`(1*2^3+0*2^2+1*2^1+1*2^0 + 1*2^{-1})*2 = 1*2^4+0*2^3+1*2^2+1*2^1 + 1*2^0 =` 10111\ :sub:`2`\  = 23\ :sub:`10`\

:math:`(1*2^3+0*2^2+1*2^1+1*2^0 + 1*2^{-1})/2 = 1*2^2+0*2^1+1*2^0+1*2^{-1} + 1*2^{-2}` = 101.11\ :sub:`2`\  = 101.11\ :sub:`2`\  = 5.75\ :sub:`10`\

Octal Base 
----------

0, 1, 2, 3, 4, 5, 6 and 7 forms the octal base. To represent this base in an electrical system we would have eight different voltage levels. A number greater than seven and smaller than one need more than one algorism to be represented. For example 11.5\ :sub:`10`\  in octal base is represented as 13.4\ :sub:`8`\ ,

:math:`1*2^3+0*2^2+1*2^1+1*2^0 + 1*2^{-1} + 0*2^{-2} + 0*2^{-3} =1*8^1 + (2+1)*8^0 + 4*8^{-1} = 1*8^1+3*8^0+4*8^{-1} =` 13.4\ :sub:`8`\  = 11.5\ :sub:`10`\

As 8 is :math:`2^3` you can group three algorisms in a number written in a binary base to form a number in a octal base. Example: 

100 001 111\ :sub:`2`\ = 417\ :sub:`8`\

Hexadecimal Base
----------------

0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E and F forms the hexadecimal base. To represent this base in an electrical system we would have sixteen different voltage levels. A number greater than sixteen and smaller than one need more than one algorism to be represented. For example 11.5\ :sub:`10`\  in the hexadecimal base is represented as B.8\ :sub:`16`\ ,

:math:`1*2^3+0*2^2+1*2^1+1*2^0 + 1*2^{-1} + 0*2^{-2}+0*2^{-3} + 0*2^{-4} = 11*16^0 + 8*16^{-1}` = B.8\ :sub:`16`\  = 11.5\ :sub:`10`\

In this case 11 quantities represent the letter B. As 16 is :math:`2^4` you can group four algorisms in a number written in a binary base to form a number in a hexadecimal base. Example:

1000 1111\ :sub:`2`\ = 8F \ :sub:`16`\

Numbers in Different Bases
--------------------------

==============  =============  ==============  =============== 
Number base 10	Number base 2	Number base 8	Number base 16
==============  =============  ==============  ===============
0	        0000	       0               0
1	        0001	       1	       1
2	        0010	       2	       2
3	        0011	       3	       3
4	        0100	       4	       4
5	        0101	       5	       5
6	        0110	       6	       6
7	        0111	       7	       7
8	        1000	       10	       8
9	        1001	       11	       9
10	        1010	       12              A
11	        1011	       13	       B
12	        1100	       14	       C
13	        1101	       15	       D
14	        1110	       16	       E
15	        1111	       17	       F
==============  =============  ==============  ===============

Negative Numbers
----------------

To represent a negative number in any base you only need to add the “-“ symbol in front of the number, but how to store it in a memory? As we store numbers in a binary base we could add one bit in the number, one element of memory, to say if it is negative or positive. The bit 0 represent the positive signal and the bit 1 the negative signal. For example:

+11.5\ :sub:`10`\ = +1011.1\ :sub:`2`\ = 01011.1\ :sub:`2`\

-11.5\ :sub:`10`\ = -1011.1\ :sub:`2`\ = 11011.1\ :sub:`2`\

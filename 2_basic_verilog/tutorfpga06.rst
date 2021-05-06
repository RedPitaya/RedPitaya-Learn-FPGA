##############################
Statements and Loops
##############################

Behavioral statements are declared inside an **always** or **initial** block. There are three possible statements, **if-else** **case** and **loop**.

If-else Statements
==================
It has the same format as many programming languages. It tests a condition and executes the code inside the **if** block and if the condition isn't met the code inside the **else** block is executed. Example of a multiplexer:

.. code-block:: Verilog
    
    always@(a or b or sel) begin 
        if (sel) 
            out = a;
        else 
            out = b;
    end

Case Statements
===============
Case the variable or expression is equal some value inside the case block the statement where it is true is executed. 

.. code-block:: Verilog
    
    reg a;
    case (a)
        1'b0 : statement1;
        1'b1 : statement2;
        1'bx : statement3;
        1'bz : statement4;
    endcase

There are also the forms of the case block that are **casez** and **casex**. The **casez** treats the values as don't cares and all 'z' is represented by '?' . The casex is the same but treats 'x' and 'z' as don't cares. The **default** option is used when any other condition is met.

.. code-block:: Verilog

    always @(irq) begin
        {int2, int1, int0} = 3'b000;
        casez (irq)
            3'b1?? : int2 = 1'b1;
            3'b?1? : int1 = 1'b1;
            3'b??1 : int0 = 1'b1;
            default: {int2, int1, int0} = 3'b000;
        endcase
    end

Forever and Repeat Loops
========================

They are used for test and simulation and cannot be synthesized. The **forever** loop executes continuously and don't stop. The loop **repeat** executes in a finite amount of time.

forever
-------

.. code-block:: Verilog

    initial
    begin
        forever 
        #25 clock = ~clock;  //executes forever and at 25 periods of time clock changes state
    end

repeat
------
  
.. code-block:: Verilog

    if(rotate == 1)
    repeat(8)            // if rotates = 1 rotates data 8 times
    begin
        tmp = data[15];
        data = data << 1 + tmp;
    end    

While Loop
==========

Executes the block if the condition is true, repeats the test and executes again until the condition is not met.

.. code-block:: Verilog

    always@(a or b) begin

    while(count < 12) begin  // count 12 times and terminate
    count = count + 1;
    end

    end

For Loop
========

Executes the code a finite amount of time. If the condition is true it enters the block, after the end it repeats the test and executes again until the condition is not met. In the example the condition is i < 16. In the beginning the i variable is declared as zero and it increases by one at the end of every loop.

.. code-block:: Verilog

    always@(a or b) begin
    for (i = 0; i < 16; i = i +1) begin
        a <= a + 1; // executes this code 16 times
    end
    end

References
==========

Verilog HDL Basics - Altera
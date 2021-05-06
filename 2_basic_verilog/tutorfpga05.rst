#####################
Assignments
#####################

Continuous Assignment Statements
================================

In Verilog the statements that are outside an always or initial block are called continuous. For example in the next code the **net** out changes when a or b changes:

.. code-block:: Verilog
    
    wire out = a + b; // Implicit statement

Wich is equal to:

.. code-block:: Verilog
    
    wire out;
    assign out = a + b;

When the right-hand side (RHS) changes the left-hand side updates immediately. RHS can be a **net**, **reg**, or functions calls and LHS must be a **net**.

Procedural Statements
=====================

There are two types of procedural statements, the **always** block and the **initial** block. In Verilog there may be several **always** blocks and they are executed in parallel. The **initial** block is used for simulation, it can't be synthesized and it executes only once in the start a simulation. 

The **always** block executes when its pre-defined funtions, or its inputs changes. The pre-defined functions are **posedge** and **negedge**, and they are used with clock variables to detect when it rises to 1 or decays to 0. Example:

.. code-block:: Verilog
    
    initial begin  // used for simulation
    a = 3'b101;
    b = 3'b001;
    end

    always@(a or b) begin  //executes when a or b changes
    c = a + b;
    end

    always@(posedge clock) begin //executes in the positive edge of clock
    c = a + b;
    end
    
Blocking vs Non-blocking Assignments
====================================

If the assignments inside an **always** or **initial** block are made with the (=) symbol they are executed sequentially. If they are made with the (<=) they are executed in parallel. They are used to update **reg**, **integer**, **real**, **time** and **realtime** values. The **real**, **time** and **realtime** values are used in simulation and are not synthesizable. Examples:

Blocking
--------

.. code-block:: Verilog

    reg a [1:0] = 2'b01;
    reg b [1:0] = 2'b10;
    reg c [3:0] = 4'b0000;
    reg d [3:0] = 4'b0000;

    always@(posedge clock) begin  //executes on clock
    c = a + b;        // statements in sequence
    d = c + a;        // after the clock rising c = 4'0011
    end               // and d = 4'0100;

Non-Blocking
-------------

.. code-block:: Verilog

    reg a [1:0] = 2'b01;
    reg b [1:0] = 2'b10;
    reg c [3:0] = 4'b0000;
    reg d [3:0] = 4'b0000;

    always@(posedge clock) begin  //executes on clock
    c <= a + b;        // statements in parallel
    d <= c + a;        // after the clock rising c = 4'0011
    end                // and d = 4'0001;

References
==========

Verilog HDL Basics - Altera

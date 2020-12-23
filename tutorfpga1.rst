######################
Installation of Vivado
######################

This installation tutorial is intended for who want to use the FPGA of the Red Pitaya board. You will need to install the OS Ubuntu or the OS Linux Mint on your computer or on a virtual machine. After that follow the instructions to install Vivado.

**************
Install Vivado
**************

Download `Vivado HLx 2017.2: WebPACK and Editions - Linux Self Extracting Web Installer <Vivado HLx 2017.2: WebPACK and Editions - Linux Self Extracting Web Installer>`_ . If you don't have an Xilinx account you will have to create one, it's free. 

.. image:: img/Screenshot%20from%202018-05-16%2010-45-53.png
    :width: 30%
    :align: center


Now you have to run the downloaded file for installation. Open a terminal, go to the downloaded file directory (cd Downloads/) and insert the following commands. The first command is to make the file executable and the second to run the file.

chmod +x Xilinx_Vivado_SDK_2017.2_0616_1_Lin64.bin 

sudo ./Xilinx_Vivado_SDK_2017.2_0616_1_Lin64.bin 

.. image:: img/Screenshot%20from%202018-05-16%2010-49-38.png
    :width: 30%
    :align: center



It will open this installation wizard. Click Next.

.. image:: img/Screenshot%20from%202018-05-16%2010-52-12.png
    :width: 30%
    :align: center



Insert your Xilinx ID and password. Check **Download and install Now**. Click Next.

.. image:: img/Screenshot%20from%202018-05-16%2010-52-18.png
    :width: 30%
    :align: center



Check all the boxes. Click Next.

.. image:: img/Screenshot%20from%202018-05-16%2010-52-24.png
    :width: 30%
    :align: center


Check **Vivado HL WebPACK**. Click Next.

.. image:: img/Screenshot%20from%202018-05-16%2010-52-33.png
    :width: 30%
    :align: center

Check all the boxes in the next image. Uncheck Ultrascale and Ultrascale+ you don't need them. Click Next.

.. image:: img/Screenshot%20from%202018-05-16%2010-54-02.png
    :width: 30%
    :align: center

The default installation directory is **/opt/Xilinx**, so install there. Click Next.

.. image:: img/Screenshot%20from%202018-05-16%2010-53-07.png
    :width: 30%
    :align: center

Check the information and click Install. Now wait for the download and Installation.

.. image:: img/Screenshot%20from%202018-05-16%2010-54-13.png
    :width: 30%
    :align: center


It will open the license manager, and you will have to get the free WebPACK license file. Click **Connect Now** or **Save Link As**. This will open the Xilinx license manager site and you have to follow instructions to generate the **ISE WebPACK license**. You will receive the license file on your registered e-mail. After that click in **Load License** and click **Copy License** to copy your **.lic** file to register Vivado.

.. image:: img/Screenshot%20from%202018-05-16%2010-16-33.png
    :width: 30%
    :align: center


After installing Vivado install additional libraries by executing following command in Terminal

.. code-block:: bash

    apt-get install libxft2 libxft2:i386 lib32ncurses5
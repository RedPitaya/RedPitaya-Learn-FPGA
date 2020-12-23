##################
Advanced Examples
##################

=============
SDR Receiver
=============

The implementation of the SDR receiver is quite straightforward:

 * An antenna is connected to one of the high-impedance analog inputs.
 * The on-board ADC (125 MS/s sampling frequency, 14-bit resolution) digitizes the RF signal from the antenna.
 * The data coming from the ADC is processed by a in-phase/quadrature (I/Q) digital down-converter (DDC) running on 
   the Red Pitaya’s FPGA.
 * The I/Q data is transmitted via TCP to the SDR programs such as SDR# and HDSDR.

The tunable frequency range covers from 0 Hz to 50 MHz.

The I/Q data rate is configurable and four settings are available: 50, 100, 250 and 500 kSPS.

More details can be found on Pavel Demins `site <http://pavel-demin.github.io/red-pitaya-notes/sdr-receiver/>`__.

================
SDR Transceiver
================
The SDR transceiver consists of two SDR receivers and of two SDR transmitters.

The implementation of the SDR receivers is quite straightforward:

 * An antenna is connected to one of the high-impedance analog inputs.
 * The on-board ADC (125 MS/s sampling frequency, 14-bit resolution) digitizes the RF signal from the antenna.
 * The data coming from the ADC is processed by a in-phase/quadrature (I/Q) digital down-converter (DDC) running on 
   the Red Pitaya’s FPGA.

The SDR receiver is described in more details at `this link <http://pavel-demin.github.io/red-pitaya-notes/sdr-receiver/>`__.

The SDR transmitters consist of the similar blocks but arranged in an opposite order:

 * The I/Q data is processed by a digital up-converter (DUC) running on the Red Pitaya’s FPGA.
 * The on-board DAC (125 MS/s sampling frequency, 14-bit resolution) outputs RF signal.
 * An antenna is connected to one of the analog outputs.

The tunable frequency range covers from 0 Hz to 60 MHz.

The I/Q data rate is configurable and five settings are available: 20, 50, 100, 250, 500 and 1250 kSPS.

The basic blocks of the digital down-converters (DDC) and of the digital up-converters (DUC) are shown on the 
following diagram:

More details can be found on Pavel Demins `site <http://pavel-demin.github.io/red-pitaya-notes/sdr-transceiver/>`__.

======================================
SDR Transceiver Compatible With HPSDR
======================================

The `High Performance Software Defined Radio <http://openhpsdr.org/>`__ (HPSDR) project is an open source hardware and
software project that develops a modular Software Defined Radio (SDR) for use by radio amateurs and short wave 
listeners.

This version of the Red Pitaya SDR transceiver makes it usable with the software developed by the HPSDR project and 
other SDR programs that support the HPSDR/Metis communication protocol.

This SDR transceiver emulates a HPSDR transceiver with one `Metis <http://openhpsdr.org/metis.php>`__ network 
interface module, two `Mercury <http://openhpsdr.org/mercury.php>`__ receivers and one 
`Pennylane <http://openhpsdr.org/penny.php>`__ transmitter.

The HPSDR/Metis communication protocol is described in the following documents:

 * `Metis - How it works <http://svn.tapr.org/repos_sdr_hpsdr/trunk/Metis/Documentation/Metis-%20How%20it%20works_V1.33.pdf>`__
 * `HPSDR - USB Data Protocol <http://svn.tapr.org/repos_sdr_hpsdr/trunk/Documentation/USB_protocol_V1.58.doc>`__

More details can be found on Pavel Demins `site <http://pavel-demin.github.io/red-pitaya-notes/sdr-transceiver-hpsdr/>`__.

==================================
Pulsed Nuclear Magnetic Resonance
==================================

The system consists of one in-phase/quadrature (I/Q) digital down-converter (DDC) and of one pulse generator.

The tunable frequency range covers from 0 Hz to 60 MHz.

The I/Q data rate is configurable and five settings are available: 25, 50, 250, 500, 2500 kSPS.

More details can be found on Pavel Demins `site <http://pavel-demin.github.io/red-pitaya-notes/pulsed-nmr/>`__.

===================================
Multichannel Pulse Height Analyzer
===================================

Spectrometry example.

Some interesting links on spectrum analysis:
 * `Spectrum Analysis Introduction <http://www.canberra.com/literature/fundamental-principles/pdf/Spectrum-Analysis.pdf>`_
 * `Gamma Spectrometry Software <https://www.youtube.com/watch?v=bBG_m4akFts>`_

More details can be found on Pavel Demins `site <http://pavel-demin.github.io/red-pitaya-notes/mcpha/>`__.

========================
Vector Network Analyzer
========================

Some interesting links on network analyzers:

 * `VNA Operating Guide <http://www.wetterlin.org/sam/SA/Operation/VNA_Guide.pdf>`_
 * `Three-Bead-Balun Reflection Bridge <http://www.wetterlin.org/sam/Reflection/3BeadBalunBridge.pdf>`_
 * `Ham VNA <http://dxatlas.com/HamVNA/>`_
 * `Fundamentals of Vector Network Analysis Primer <http://rohde-schwarz-scopes.com/designcon/VNA%20fundamentals%20primer.pdf>`_
 * `Introduction to Network Analyzer Measurements <http://download.ni.com/evaluation/rf/Introduction_to_Network_Analyzer_Measurements.pdf>`_



More details can be found on Pavel Demins `site <http://pavel-demin.github.io/red-pitaya-notes/vna/>`__.

=================================
Debian With Red Pitaya Ecosystem
=================================
More details can be found on Pavel Demins `site <http://pavel-demin.github.io/red-pitaya-notes/vna/>`__.

=================================================
Signal decimation using a compensated CIC filter
=================================================

Decimation is the process of converting a time-domain signal sampled at frequency f\ :sub:`s` into a signal sampled at
frequency f\ :sub:`s`\/R, where R is the decimation rate. Downsampling alone, i.e. keeping one sample every R samples 
is not sufficient. A low-pass filtering step must precede downsampling to prevent aliasing.

More details can be found `here <https://www.koheron.com/blog/2016/10/03/decimator-cic-filter.html>`__.

========================
Pulse-Density Modulator
========================

Pulse-density modulation (PDM) is an attractive alternative to pulse-width modulation (PWM) in applications where the 
PWM technique creates unwanted spikes in the signal spectrum.

More details can be found `here <https://www.koheron.com/blog/2016/09/27/pulse-density-modulation.html>`__.


=====================================
Synchronize a cluster of Red Pitayas
=====================================

In its standard configuration, the Red Pitaya uses an on-board 125 MHz crystal to feed the 125 MSPS ADC and the 125 
MSPS DAC. This example shows how to synchronize multiple Red Pitayas on the same clock using the SATA connector
(daisy-chain) available on the Red Pitaya.

More details can be found `here <https://www.koheron.com/blog/2016/11/29/red-pitaya-cluster.html>`__.

====================================
Examples Utilizing Extension Boards
====================================

Red Pitaya becomes even more versatile with when custom extension boards are attached to it, hence we show a couple of
examples that utilize extension boards below.

-----------------------------
Simple Coherent Laser Sensor
-----------------------------

The guys at `Koheron <https://www.koheron.com/>`_  designed a small laser board which fits on top of the Red Pitaya.

More details can be found `here <https://www.koheron.com/blog/2015/09/10/laser-control.html>`__.

--------------------------
Doppler lidar velocimeter
--------------------------

Doppler effect is what we experience when hearing the siren of a moving vehicle: the tone gets higher when the 
vehicle is approaching.

The frequency of the acoustic wave emitted by the siren is affected by the movement of the vehicle. This effect is not
only true for sounds but also for optical waves: when a laser beam with frequency f\ :sub:`0` is reflected off a 
moving target with velocity v, its frequency is shifted of a quantity

    Δf=2v/c*f\ :sub:`0`\,

where c is the speed of light. The factor 2 occurs because the light is not emitted by the target but reflected off 
it. In this example laser emits at a frequency of 193.5 THz (i.e. a wavelength of 1550 nm). A target moving at 1 m/s 
would shift the laser frequency by 1.29 MHz.

More details can be found `here <https://www.koheron.com/blog/2015/11/15/doppler-lidar-velocimeter.html>`__.

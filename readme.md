# Isolated Quad Serial Adapter

This is an open-source KiCAD design files for a four-channel isolated USB-to-Serial adapter based on CH344Q IC from WCH.

## Pictures

![](pics/isolated_serial_adapter_assy.jpg)

![](pics/isolated_serial_adapter_front_rev2.png)

## Features

This adapter is convenient when you want to connect multiple serial devices to your computer simultaneously, while also provides isolation between your computer and those devices.

- Four USB-to-Serial channels
	- CH344Q IC: Only one USB required to communicate with all fours channels at the same time at maximum speed of 6Mbps.
	- 1024 bytes of RX FIFO buffer and 512 bytes of TX FIFO buffer per channel.
	- Configured as 2x RS485, 1x RS232, and 1x 5V UART channels.
	- Modem flow control signals for RS232 and UART.
	- Auto direction control for RS485.
	- RS485 120 Ohms termination resistors (on/off)
- Full Isolation
	- All power and data signals are fully isolated between the USB and the serial side.
	- CA-IS3088 dedicated RS485 isolation IC.
	- MAX3243 dedicated RS232 isolated IC (250kbps max).
	- Digital Isolator ICs for other signals.
	- UART voltage level selector (2.5/2.7/3.0/3.3/5.0 V)
	- 1W 5V isolated DC/DC converter.
- Other Protection
	- TVS diodes on all signals line, including the USB.
	- Polyfuse on USB VBUS.
- Intuitive Interfaces
	- USB Type-C Connector
	- Degson 3.5mm terminal blocks for serial channels
	- Pin header breakout for modem signals
	- RX/TX indicators
	- USB connection good indicator
	- Power indicators on both side of the isolation
	- USB reset and flow control mode buttons
	- Design to fit a 90x125x40mm PLC project box
	
## Revisions

We are currently at Revision 2. Changelog is below:

**Revision 1 (November 2022)**
 - Initial Design
 - U9 has wrong footprint (could still be soldered with some difficulties)
 
**Revision 2 (March 2024)**
 - Updated design for new enclosure
 - Updated circuit for more functionalities.
 - U11 has wrong Vref connection (do not populate)

## What is provided

The goal of this repository is to enable you to build this on your own as easy as possible. **The schematics, PCB design, and an interactive BOM is provided.**

Hardware is licensed under `SPDX-License-Identifier: CERN-OHL-S-2.0`

Contains no software

Documentation is licensed under `SPDX-License-Identifier: CC-BY-SA-4.0`

## Ordering

You can export gerbers from this project and order the board yourself. Noted that this board must be manufactured with 1.2mm thickness to fit the enclosure.

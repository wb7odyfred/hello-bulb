Hello,   Saw this project and decided to help correct the errors in the schematic files for hello-bulb project.

This project is loosely based on USBTiny  from website http://dicks.home.xs4all.nl/avr/usbtiny/

Moved the 3.6V zener diodes to the USB side of the 68 ohms resistors.    Left the on 1.5K ohm resistor connected to a VBUS connection to the USB port.   Added a second 1.5K ohm resistor from USB port side of D- trace back to input PD3 on the U1 Attiny 2313. This resistor can be not solder in, if not needed in your design.    Added a 3 pin power jack connector for powering board externally (  disconnecting and not using the USB power source ).   Maybe add a 2 pin port to VCC and GND.

Added  the 6 pin  AVR-ISP-6  connector for programming in circuit this ATTiny2313 from a ICSP cable or from another Arduino.
Added a  8 pin connector to bring the unused pins from the microcontroller to a connector.
Added another LED diode and resistor to output PD5 pin 9.  You can omit these parts, when building the board.

Used the KiCAD ATMEL.LIB library  to import the AVR-ISP-6 connector.   Used the KiCAD CONN.LIB library (modified name to conn-flf.lib)  add / import to hello-bulb progect and not conflict with exsiting conn.lib library.

The  USB_Plug component module ATTiny2313 had a couple pin wires aligned with the right hand side of the chip.
Pin 11 PD6 and  PD??  Pin ??
 
Added folder "mylib"  to contain  new atmel.lib  and conn-flf.lib  schematic symbol libraries
Added folder "documents"  to contain document files related to ATTiny2313 and this hello-bulb PCB Board
Added folder "documents/images"  to contain .PNG and .JPG image files related to ATTiny2313 and this schematic.

Used the KiCAD ATMEL.LIB library  to import the AVR-ISP-6 connector.   Used the KiCAD CONN.LIB library (modified name to conn-flf.lib)  add / import to hello-bulb progect and not conflict with exsiting conn.lib library.

TODO:

route the board, from the schematic.
find and use the footprints for the PCB layout

WB7ODY Fred  July 19, 2014

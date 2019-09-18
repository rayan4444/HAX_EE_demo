# ATMEGA32u4 Breakout v1

The ATEGA32u4 is the main microcontroller on the Arduino Leonardo and Micro. Its main advantage over the standard ATMEGA328P chip from the UNO lies in its native USB support, which makes it very easy to communicate with from a PC or SBC. This module breaks out most of the ATMEGA32u4 peripherals and is meant to be used in a Distributed Control System architecture.

## Ordering the PCB
Gerber files, Drill files and BOM for this board are provided in this repo.
If you don't know how to order PCBs, check out the HAX Wiki: [making a PCB (prototyping)](https://wiki.hax.co/Making_a_PCB_(prototyping)#Ordering_the_Board)

## Features
* Native USB
* RS-485 bus
* I2C breakout x 2
* SPI breakout x 1
* Analog pins breakout x 5 (ADC)
* PWM pins breakout x 4
* Programmable LED (on digital pin 13)
* Digital I/O breakout x 4 with optional MOSFETs:
  * solder a 0 ohm resistor where designated to use standard digital output
  * solder N-MOSFET circuitry to use it to toggle higher voltage outputs
* Optional High voltage input (for the N-MOSFET outputs)

## Programming Instructions
* The native USB port cannot be used immediately after assembling the PCB. You need to burn the Arduino Leonardo or Micro bootloader on the MCU first.
* You can use another Arduino and the SPI breakout 3x2 header to burn the bootloader ([tutorial](https://www.arduino.cc/en/tutorial/arduinoISP))
> Tip: If you have issues burning the bootloader, try connecting the receiver's (aka the new PCB) RST line to pin 10 of the programmer Arduino (aka Arduino you are using to burn the bootloader). On some boards the ICSP header's RST is not connected to pin 10 by default.

* After burning the bootloader, you can connect your ATMEGA32u4 breakout to your PCB/SBC with standard Micro USB cable and use the Arduino IDE to flash it.

## Examples
* *Short description of code in "examples" folder*
* *Link description/projects/photos where people have used this*

## Datasheets
* MCU: [ATMEGA32u4](http://ww1.microchip.com/downloads/en/devicedoc/atmel-7766-8-bit-avr-atmega16u4-32u4_datasheet.pdf)
* RS-485 transceiver: [MAX485](https://datasheets.maximintegrated.com/en/ds/MAX1487-MAX491.pdf)
* MOSFET: [IRLHM630TRPBF](https://www.infineon.com/dgdl/irlhm630pbf.pdf?fileId=5546d462533600a401535663951725a5)

## References
* [RS-485 basics](https://learn.sparkfun.com/tutorials/ast-can485-hookup-guide/introduction-to-rs485)
* Writing a custom RS485 protocol (*add link*)

## Feedback and Questions
Feel free to open an issue to report bugs, ask questions, suggest features, etc.   

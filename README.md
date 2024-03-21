# EPROM 27-series Arduino-based programmer

Work in-progress of a project of easy-to-use programmer for EPROM 27-series based on Arduino.

*Download GUI application and Arduino sketch from "Releases".*

Supported chips:
 * 27C16 (connects from 3 to 26 leg DIP28 socket)
 * 27C32 (connects from 3 to 26 leg DIP28 socket)
 * 27C64
 * 27C128
 * 27C256
 * 27C512
 * Dallas DS1225 NVRAM

## Installation

Order PCB from gerber files, assemble the board. Use BOM to find components.

If first time assembled you have to load sketch.ino into Arduino IDE and flash your Arduino.

Always check programming voltage before inserting new chip to program.

Run GUI application and choose serial port.

## Schematics

[Initial project](<https://github.com/bouletmarc/BMBurner>):
* Was made in DIP packages.
* No sources.
* Windows-only application.

[Walhi project](<https://github.com/walhi/arduino_eprom27_programmer>):
* Made in Eagle.
* 50/50 SMD/DIP.
* New Arduino sources.
* Windows/Linux Qt-based light GUI application.

[Radionews fork](<https://github.com/Radionews/arduino_eprom27_programmer>):
* Refactored in EasyEDA.
* Uses SPI for logic.
* Mostly SMD components.
* Uses GUI application from above.

[This project](<https://github.com/kab01m/arduino_eprom27_programmer>):
* Translated to KiCad EDA.
* SMD components whereever it was possible.
* Arduino is now not detachable.
* No schematic difference from above.
* Previous software used.

Schematics

![Schematic](https://github.com/Radionews/arduino_eprom27_programmer/blob/master/imgs/sch.png)

Assembled picture

![PCB](https://github.com/Radionews/arduino_eprom27_programmer/blob/master/imgs/pcb.png)

## Software

Software is taken from [Walhi project](<https://github.com/walhi/arduino_eprom27_programmer>).

Functions:

 * Read EEPROM/NVRAM.
 * Write EEPROM/NVRAM.
 * Verify chip and check if it is zeroed.
 * Programming voltage check (available for AVR in TQFP case)

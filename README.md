# Mighty 1284P: An Arduino core for the ATmega1284P #
  

## What is it? ##

Everything you need to run Arduino on ATmega1284P.

## Revision history ##

**03May2014 Jack Christensen**
- An attempt to bring the mighty-1284p core up to Arduino 1.0.5 level. In researching the changes I came to the conclusion that the core was originally based on Arduino 1.0 and that since then all the changes in maniacbug's core files necessary to support the ATmega1284P had been worked into subsequent Arduino releases. This may have occurred as early as Arduino 1.0.1. Nevertheless, this update is working with Arduino 1.0.5 and while it may work with earlier releases, I do not plan to test them, so there is no guarantee.
- The initial commit is therefore just a matter of removing the cores directory and updating the boards.txt file to point at the cores directory in the Arduino distribution.

**23Jun2012 maniacbug**
- Everything is here and has been initially tested.  It should work fine.  There is more detailed testing which must be completed before calling it completely 'done' though.
- The platform now includes optiboot.  This bootloader is better in every way than the previous version, so it is recommended in all cases.  The prior one is included for reference.

## Installation

1. Download the [ZIP File](https://github.com/maniacbug/mighty-1284p/zipball/master)
2. Unzip it a folder called 'hardware' off your sketches directory, e.g. /Users/maniacbug/Source/Arduino/hardware/mighty-1284p
3. Restart the IDE
4. Select Tools > Board > Mighty 1284p 16MHz using Optiboot
5. To burn the bootloader, follow the Arduino [Bootloader](http://arduino.cc/en/Hacking/Bootloader) instructions.

## Requirements

* Works only on Arduino >= 1.0
* Cannot be burned using [USBtinyISP](http://www.ladyada.net/make/usbtinyisp/).  That programmer cannot flash to chips with >64k flash size.

## See also

http://maniacbug.wordpress.com/2011/11/27/arduino-on-atmega1284p-4/

## Supported Boards

* 'Mighty 1284p 16MHz using Optiboot'.  The main board.  Use this unless you have some clear reason to use another board.  This uses a straightforward pinout that is especially helpful on a breadboard-built unit.
* 'avr-developers.com pinouts 16MHz using Optiboot'.  Some people prefer the pinouts from avr-developers.com.  The classic pinouts.
* 'Bobuino'.  CrossRoads' board built for maximum compatibility with Arduino Uno-class shields.
* 'Original Mighty 1284p 16MHz'.  The very first bootloader I ever got working.  Not recommended for use, but here as historical record.
* 'Original Mighty 1284p 8MHz'.  Ditto, but runs at 8MHz.
# lame-o-kernal
Allows customization of the C64 KERNAL ROM.

The original v0.1 version was downloaded from CSDB.dk ( http://csdb.dk/release/?id=108616 )

Versions:

* 2012-05-08: v0.1: Original version coded and released by Martin 'Enthusi' Wendt of Onslaught.
* 2015-05-21: v0.2: Updated by Tim Locke to support changing the startup character mode from upper/graphics to upper/lower, to support lower/upper case in startup messages, added a flag to choose whether to display amount of bytes free, and adjusted message to allow removal of initial carriage return.

Documentation

This is a Python script. It currently accepts no command line arguments, nor configuration file, but has customizations hard-coded in it. The script settings are self documenting. When run, it creates a customized kernal file named kernal.bin.

Here are the currently supported customizations:

 * Border Color - Permitted values are: black, white, red, cyan, violet, green, blue, yellow, orange, brown, lightred, darkgrey, midgrey, lightgreen, lightblue, lightgrey. Original kernal: lightblue.
 * Background Color - Permitted values are the same as for the border color. Original kernal: blue.
 * Font color - Permitted values are the same as for the border color. Original kernal: lightblue.
 * Character case mode - Permitted values are 0x14 (upper/graphics), 0x16 (lower/upper). Original kernal: 0x14.
 * Key repeat speed - Permitted values are uncertain, probably 0x00-0xFF. Original kernal: 0x04.
 * Key repeat delay - Permitted values are uncertain, probably 0x00-0xFF. Original kernal: 0x10.
 * Drive default - Permitted values are uncertain. 0x01, 0x08-0x0B are acceptable. Original kernal: 0x01.
 * Power on message - Permitted ASCII values are 32 to 122 with a length limit of 55 characters. The script converts these to PETSCII. The first 40 characters will be displayed on screen line 2, with the rest at the beginning of screen line 3.
 * Power on message2 - Permitted values are the same as Power on message, but with a limit of 17 characters. These characters will be displayed after the Power on message.
 * BASIC BYTE FREE message - Permitted values are True and False. False means the amount of bytes free will not be displayed between message and message2.

Ideas for the future:

* Create a lame-o-basic for the C64 BASIC ROM, allowing modifications such as changing the READY. prompt.

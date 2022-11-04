--------------------------------------------------------------------------------
MSX-EQ PSG Spectrolyzer Cartridge
Copyright (c) 2021-2022 RBSC
Developer: Pyhesty
Last update: 04.11.2022
--------------------------------------------------------------------------------

About the project
-----------------

The MSX-EQ PSG Spectrolyzer is a simple cartridge for the MSX platform that visualizes the spectrum of notes played by the
programmable sound generator, such as the AY-3-8910 or YM2149 (PSG). The cartridge board is intended for the standard MSX
cartridge slot. The board shows the effect of measuring the signal's level, in which each reproduced frequency (or frequency
range) corresponds to one of 9 vertical LED indicators.

All files of the MSX-EQ project are available in the RBSC's Github repository: 

 - https://github.com/RBSC/MSX-EQ


Hardware
--------
 
The MSX-EQ cartridge is based on the PLD Altera EPM7128, that has 128 logical units. The PLD intercepts PSG port I/O, identifies
the played note/frequency and displays its representation on the dedicated LED indicator. The cartridge doesn't need any special
setup. It can be installed into any standard MSX slot that allows an unobstructed view of the cartridge's LED indicators.

The cartridge visualizes the played notes/frequencies in games and demos in real time. After a note/frequency fades out, the LED
indicators automatically switch off.

The cartridge may be assembled in 2 different ways:

 - With discrete LED elements - simple, but allowing various color combinations
 - With LED assemblies - the so-called "bars", mostly single-colored

The following color combinations are possible (those were tested and were found suitable for the project, however other color
combinations are possible):

 - One color LEDs or LED assemblies: blue, red or green
 - Multi-colored LEDs or LED assemblies: blue with red or green with red (red LEDs are placed on top)


Firmware uploading
------------------

The freshly-assembled MSX-EQ cartridge needs the firmware to be uploaded into the PLD chip. For updating/uploading the firmware
into the cartridge you will need:

 - Quartus II Web Edition (Free) v15.0 or later software
 - Byte Blaster or USB Blaster programmer (can be purchased on Ebay or AliExpress)

The procedure is simple - supply 5v onto the cartridge board, connect the USB Blaster to the JTAG connector's placeholder (mind
the orientation of the connector!). Auto-detect the Altera chip with Quatrus software and then upload the POF file from the
"Firmware" folder into the PLD chip.

The Quartus Programmer software can be downloaded from here:

 - https://mirrors.pdp-11.ru/_msx/_carnivore2/quartus/

IMPORTANT!
If the LED assemblies with inverted polarity were used to assemble the cartridge, please use the "MSX_EQ_inv_led.pof" firmware
instead of the standard one.


Assembling notes
----------------

It's highly recommended to install all ceramic capacitors (100nF) onto the board. In addition, at least one tantalum capacitor should
be installed.


Cartridge case
--------------

Any factory-made MSX cartridge manufactured from semi-transparent or transparent plastic is suitable for the MSX-EQ cartridge board.
For example, the following quality MSX cartridge cases can be obtained from Overrich (South Korea) and Retro Game Restore (Taiwan):

 - https://retrogamerestore.com/store/msx_cart_shell/
 - https://www.msx.org/news/en/black-white-and-transparent-msx-cartidge-cases-overrich

Also, there's a 3D model of the cartridge case in the repository. The case should be printed with semi-transparent filament.


Where to buy parts
------------------

All parts for assembling the MSX-Eq cartridge can be purchased from varios sellers on AliExpress:

1. PLD: EPM7128STC100
2. LEDs: single 0805 size LEDs or LED assemblies
3. Resistors: 0805 1k
4. Capacitors: 0805 0.1uF
5. Tantalum capacitors: TypeB or TypeC, 10-100uF

See the partslist.txt document for more info.


Visual Effects
--------------

You can check how the cartridge visualizes various PSG effects by watching these videos:

 - Games: https://youtu.be/E50GIDputWo
 - Demo 1: https://youtu.be/SXDI22wPhJE
 - Demo 2: https://youtu.be/Vhv5bKJgaLk


IMPORTANT!
----------

The RBSC provides all the files and information for free, without any liability (see the disclaimer.txt file). The provided information,
software or hardware must not be used for commercial purposes unless permitted by the RBSC. Producing a small amount of bare boards for
personal projects and selling the rest of the batch is allowed without the permission of RBSC.

When the sources of the tools are used to create alternative projects, please always mention the original source and the copyright!

If you would like to commercially produce this cartridge, please contact the administrator of the RBSC (see info below).


Contact information
-------------------

The members of RBSC group Tnt23, Wierzbowsky, Pyhesty, Ptero, GreyWolf, SuperMax, VWarlock è DJS3000 can be contacted via the group's e-mail
address:

info@rbsc.su

The group's coordinator could be reached via this e-mail address:

admin@rbsc.su

The group's website can be found here:

https://rbsc.su/
https://rbsc.su/ru

The RBSC's hardware repository can be found here:

https://github.com/rbsc

The RBSC's 3D model repository can be found here:

https://www.thingiverse.com/groups/rbsc/things

-= ! MSX FOREVER ! =-


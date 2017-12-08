# All about the Arduino nano

This section takes a deeper look into the arduino and programming it. As the eChook kit uses an Arduino nano, that will be the focus however much of it is relevant to other Arduinos.

## **Introduction to the Arduino Nano**

The Arduino is a very popular microcontroller board with a large hobbyist and developer community online. It allows simple coding and quick prototyping of systems. It is also an open source project, one perk of which is that it is possible to get very cheap clones or ‘Arduino Compatible’ boards, mainly from China. These are some of the reasons it was chosen as the ‘brain’ for the eChook Nano board.

The Arduino Nano is based on an Atmel AVR ATMega328 microprocessor. Further information on the Nano can be found [here](https://www.arduino.cc/en/Main/ArduinoBoardNano). For interest, the datasheet and reference manual for the ATMega328 microprocessor can be found [here](http://www.atmel.com/images/atmel-8271-8-bit-avr-microcontroller-atmega48a-48pa-88a-88pa-168a-168pa-328-328p_datasheet_complete.pdf).

### Arduino Nano Variants

Two variants of the arduino nano were made, one with an ATMega168 processor and one with a ATMega328 processor. It is rare to find one with the ATMega168 processor, but this is clocked at half the speed \(8MHz\) and has significantly less memory, so is not recommended.

Many of the cheaper Nanos available to buy on the internet use an alternate USB to Serial interface chip. This will be the CH340, and is due to this chip being cheaper than the one specified in the official Arduino design. This does not change the functionality of the arduino for the user, however does require a different driver. The CH340 Driver Installer can be downloaded from [here](https://drive.google.com/file/d/0B8NB2ERSryMSdlQxNFpPM1BGenc/view?usp=sharing).

NB: Personally I have never experienced any problems with cheap nano’s ordered from China, however I know people have had issues with them not working out the box. Occasionally they have been recoverable by reflowing some solder or reflashing the bootloader.

One issue that does seem consistent with cheap nanos is that the pins aren’t soldered in at a perfect 90° so a pair of pliers is required to straighten them before they will fit into bread board or a socket.

  



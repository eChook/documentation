# Troubleshooting

We'll add articles here as and when issues become apparent. If you have an issue please let us know on the forum or the Slack channel.

## PCB Issues

#### Power not getting to the Tracopower DCDC Module

24V is being supplied at the input but isn't seen at the pins of the DCDC power module. The most likely cause for this is that the rectifier diode is the wrong way around. This triggers the short circuit protection when the voltage supply is correct - the diode creates a short circuit between 24V and ground and causes the polyfuse to activate, stopping any voltage going to the rest of the board. To fix, reverse the diode on the PCB.

## Bluetooth Troubleshooting

If the eChook Companion app connects the the module but gets no data through, it will continuously disconnect and reconnect in an effort to correct the problem. If this is occurring there is an issue with the data rather than with the bluetooth itself.

* Check that the Tx light on the Arduino is flashing periodically \(should be a flash every 0.25 seconds\). This indicates that the Arduino is sending data out. If it is not, try re-programming the Arduino.
* Check that the baud rate of the Arduino and the HC-05 bluetooth module match. If the HC-05 has been auto configured by the Arduino, they will be the same. For the auto configuration procedure, see [here](https://docs.echook.uk/configuring-the-bluetooth-module/configuring-the-bluetooth-module.html).

## Arduino Compiling and Uploading

While we have tested the code that we provide, there are lots of seemingly random factors that can stop it compiling and uploading on different computers. 

The error log given in the Arduino IDE is not much help by default. Go into preferences and [enable verbose logging](programming-the-arduino/programming-the-arduino.md#compilation-errors) to get more detailed logs.

The most common issues can be addressed with the following:

* Have you got the latest [Arduino IDE](https://www.arduino.cc/en/Main/Software) Installed?
* Have you got the [CH340 Drivers](programming-the-arduino/arduino-ch340-drivers.md) installed?
* Have you selected the [correct board and COM port](programming-the-arduino/)?
* Have you got the [Bounce2 Library](programming-the-arduino/download-the-echook-arduino-code.md) installed?
* Re-Download the [eChook code](https://github.com/eChook/eChook-Arduino-Nano) to ensure no local changes have been made.

If it still fails, take a copy of the errors and post it on the [forum,](https://echook.boards.net) we'll give you a hand deciphering it.


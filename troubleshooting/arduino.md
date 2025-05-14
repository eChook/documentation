# Arduino

## Arduino Failure

Occasional failures have been reported with the Arduino on eChook boards, and we suspect these might be more common than we are currently aware of. A key indicator of such a failure is the Arduino chip becoming hot to the touch. If you experience this, we would really appreciate an email to info@echook.uk with any supporting details, including which eChook PCB version you have, which Arduino you have, when the kit was purchased, the duration of use, and the circumstances under which the failure occurred.&#x20;

If the Arduino is getting hot to the touch (too hot to comfortably hold a finger against) a new Arduino is required.

## Arduino Compiling and Uploading

While we have tested the code that we provide, there are lots of factors that can stop it compiling and uploading on different computers.&#x20;

The error log given in the Arduino IDE is not much help by default. Go into preferences and [enable verbose logging](../programming-the-arduino/programming-the-arduino.md#compilation-errors) to get more detailed logs.

The most common issues can be addressed with the following:

* Have you got the latest [Arduino IDE](https://www.arduino.cc/en/Main/Software) Installed?
* Have you got the [CH340 Drivers](../programming-the-arduino/arduino-ch340-drivers.md) installed?
* Have you selected the [correct board and COM port](../programming-the-arduino/)?
* Have you got the [Bounce2 Library](../programming-the-arduino/download-the-echook-arduino-code.md) installed?
* Re-Download the [eChook code](https://github.com/eChook/eChook-Arduino-Nano) to ensure no local changes have been made.

If it still fails, take a copy of the errors and post it on the [forum,](https://echook.boards.net) we'll give you a hand deciphering it.

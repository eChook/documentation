# Arduino

## Arduino Failure

Occasional Arduino failures have been reported on eChook V1 boards, and we suspect they may be more common than currently reported. A key indicator is the Arduino chip becoming hot to the touch.

If you see this, please email info@echook.uk with supporting details, including your eChook PCB version, Arduino model, purchase date, duration of use, and the circumstances under which the failure occurred.

If the Arduino is getting hot to the touch (too hot to comfortably hold a finger against) a new Arduino is required.

## Arduino Compiling and Uploading

While we have tested the code we provide, there are many factors that can stop it compiling and uploading on different computers.

The error log given in the Arduino IDE is not much help by default. Go into preferences and [enable verbose logging](../programming-the-arduino/programming-the-arduino.md#compilation-errors) to get more detailed logs.

The most common issues can be addressed with the following checks:

* Install the latest [Arduino IDE](https://www.arduino.cc/en/Main/Software).
* Install the [CH340 Drivers](../programming-the-arduino/arduino-ch340-drivers.md).
* Select the [correct board and COM port](../programming-the-arduino/).
* Install the [Bounce2 Library](../programming-the-arduino/download-the-echook-arduino-code.md).
* Re-download the [eChook code](https://github.com/eChook/eChook-Arduino-Nano) to ensure no local changes have been made.

If it still fails, take a copy of the errors and post it on the [forum](https://echook.boards.net), or contact us on webchat, and we'll help you decipher it.

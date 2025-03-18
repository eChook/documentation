# Troubleshooting

We'll add articles here as and when issues become apparent. If you have an issue please let us know on the forum or the webchat.

## Power Issues

#### Power not getting to the Tracopower DCDC Module

24V is being supplied at the input but isn't seen at the pins of the DCDC power module. The most likely cause for this is that the rectifier diode is the wrong way around. This triggers the short circuit protection when the voltage supply is correct - the diode creates a short circuit between 24V and ground and causes the polyfuse to activate, stopping any voltage going to the rest of the board. To fix, reverse the diode on the PCB.

## Arduino Failure

Occasional failures have been reported with the Arduino on eChook boards, and we suspect these might be more common than we are currently aware of. A key indicator of such a failure is the Arduino chip becoming hot to the touch. If you experience this, we would really appreciate an email to info@echook.uk with any supporting details, including which eChook PCB version you have, which Arduino you have, when the kit was purchased, the duration of use, and the circumstances under which the failure occurred.&#x20;

If the Arduino is getting hot to the touch (too hot to comfortably hold a finger against) a new Arduino is required.

## Current Sensor Troubleshooting

If you are not receiving a current reading from the eChook, or are getting an obviously wrong reading, i.e. multiple Amps when there is no current flowing, we first need to isolate where in the system the problem is:

1. Test the Current Sensor: \
   With no current flowing (ideally no cable passing through the sensor) and the eChook powered from 24v, measure the voltages on the eChook board connector to the current sensor relative to ground. You should see 5V on the 5V supply connection, and very close to 2.5v on both the Reference and Sense wires. \
   If the Ref and/or Sense wires aren't reading 2.5v, disconnect the offending wire from the eChook board (Just that single wire, keeping power to the current sensor) and measure the voltage again.
   1. If the voltage returns to 2.5v when disconnected, there is a hardware issue on the telemetry board.
   2. If the voltage is unchanged when disconnecting the wire, the current sensor has failed and requires replacing, however continue testing to check that there isn't a cascade failure on the board.
   3. If both wires read 2.5V as expected the current sensor is most likely working. If you have the ability to pass a current through it for it to measure, and check the voltage readings, you should see the Sense voltage rising above the Reference voltage.
2. Test the Op-Amp:\
   The Op-Amp circuit, component U3 on the V1.3 Telemetry Board, compares Reference and Sense voltages from the current sensor and outputs the voltage difference multiplied by 2. This voltage output can be checked by measuring the voltage between GND and the Current Test Point on the bottom of the board.\
   With the current sensor plugged in and no current flowing, after verifying that the Ref and Sense connections show \~2.5v, measure the voltage at the Current Test Point. If this is not very close to 0v (there will normally be a few mV present) the Op-Amp has failed and needs replacing. The required component is a [Microchip 6002 PDIP](https://octopart.com/mcp6002-i%2Fp-microchip-96737).

If you have experienced a current sensor failure, we would be very interested to know the circumstances - When the kit was purchased, how long it has been in use, what was happening when the failure was noted etc. We are aware of a few failures and are trying to gather as much data around them as possible. Please email us at info@echook.uk.

## Bluetooth Troubleshooting

If the eChook Companion app connects the the module but gets no data through, it will continuously disconnect and reconnect in an effort to correct the problem. If this is occurring there is an issue with the data rather than with the bluetooth itself.

* Check that the Tx light on the Arduino is flashing periodically (should be a flash every 0.25 seconds). This indicates that the Arduino is sending data out. If it is not, try re-programming the Arduino.
* Check that the baud rate of the Arduino and the HC-05 bluetooth module match. If the HC-05 has been auto configured by the Arduino, they will be the same. For the auto configuration procedure, see [here](setting-up-the-bluetooth/).

## Arduino Compiling and Uploading

While we have tested the code that we provide, there are lots of factors that can stop it compiling and uploading on different computers.&#x20;

The error log given in the Arduino IDE is not much help by default. Go into preferences and [enable verbose logging](programming-the-arduino/programming-the-arduino.md#compilation-errors) to get more detailed logs.

The most common issues can be addressed with the following:

* Have you got the latest [Arduino IDE](https://www.arduino.cc/en/Main/Software) Installed?
* Have you got the [CH340 Drivers](programming-the-arduino/arduino-ch340-drivers.md) installed?
* Have you selected the [correct board and COM port](programming-the-arduino/)?
* Have you got the [Bounce2 Library](programming-the-arduino/download-the-echook-arduino-code.md) installed?
* Re-Download the [eChook code](https://github.com/eChook/eChook-Arduino-Nano) to ensure no local changes have been made.

If it still fails, take a copy of the errors and post it on the [forum,](https://echook.boards.net) we'll give you a hand deciphering it.

## Wrong values being shown on Phone

If there are obviously wrong values being reported by the phone, i.e. voltages when the batteries aren't plugged in, or high current when the motor is off the most likely cause is a wrong resistor in the circuit for that sensor. Use a multimeter and compare the values to those on the schematics [here](circuit-schematics/).

If the value is far higher than anything you'd expect, it's best to power off the board quickly as an incorrect circuit could be sending more voltage to the Arduino than it is designed for with potential to cause damage.

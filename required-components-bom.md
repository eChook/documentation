# The eChook Nano Kit

Greenpower sell an eChook Nano kit that contains all the hardware and sensors needed to get eChook telemetry running on a greenpower car.

This comprises of the eChook PCB, all components required to populate the PCB as well as sensors for Current, Temperature (x2) and Rotation (Wheel and motor shaft).

The complete list of items included in the kit is below:

| **Quantity** | **Component**                                          | **Use**                                                        |
| ------------ | ------------------------------------------------------ | -------------------------------------------------------------- |
| 1            | 470r Resistor                                          | Voltage drop for LED                                           |
| 12           | 1k Resistor                                            | Protection for Arduino pins                                    |
| 2            | 4k7 Resistor                                           | Input Resistors for current differential amplifier             |
| 4            | 10k Resistor                                           | Feedback on Differential amp and pull ups for Thermistors      |
| 2            | 16k Resistor                                           | 24v and 12v Potential Dividers                                 |
| 1            | 47k Resistor                                           | Post amp current filter                                        |
| 2            | 82k Resistor                                           | 24v and 12v Potential Dividers                                 |
| 1            | Green LED, 5mm                                         | Indicator LED on PCB                                           |
| 1            | BC547 NPN Transistor                                   | Amplification stage of PWM output on PCB                       |
| 3            | Ceramic Capacitor 1uF                                  | Low Pass filtering on some sensors                             |
| 1            | 2uF 50v Electrolytic Capacitor                         | Input voltage smoothing for the regulator                      |
| 2            | 47nF Ceramic Capacitor                                 | Smoothing Capacitors for current sensor  (not on PCB)          |
| 1            | 4.7nF Ceramic Capacitor                                | Smoothing Capacitors for current sensor (not on PCB)           |
| 1            | 0.25A Radial Resettable Fuse                           | Over current protection (Short Circuit)                        |
| 1            | 8 Way DIP Socket                                       | Socket for Op-Amp                                              |
| 1            | Microchip MCP6002 Dual Op Amp                          | Used in differential amplifier for current input               |
| 2            | 15 way SIL 2.54mm Female PCB Socket                    | Socket for Arduino                                             |
| 1            | 6 way SIL 2.54mm Female PCB Socket                     | Socket for Bluetooth Module                                    |
| 1            | 5v 1A Voltage Regulator (Tracopower TSR 1-2450)        | Take 24v from the car and provide a robust 5v to the Arduino   |
| 1            | Rectifier Diode, 50V 1A                                | Reverse Polarity Protection                                    |
| 2            | NTC Thermistor 10kΩ@25°                                | Temp Sensor (not on PCB)                                       |
| 2            | Hall Effect Sensor (A1101EUA-T)                        | Sensor for wheel/motor rpm (not on PCB)                        |
| 1            | Current Sensor (LEM HAIS 50p)                          | Senses current in the 24v cable from the battery. (not on PCB) |
| 3            | 4 pin Pluggable Terminal 5.08mm                        | Connectors                                                     |
| 2            | 3 pin Pluggable Terminal 5.08mm                        | Connectors                                                     |
| 1            | 2 pin Pluggable Terminal 5.08mm                        | Connectors                                                     |
| 1            | 3 pin Pluggable Terminal 3.81mm                        | Connectors                                                     |
| 1            | Arduino Nano                                           | The Brain of the eChook                                        |
| 1            | USB Cable for Arduino                                  | Connect Arduino to PC                                          |
| 1            | HC-05 Bluetooth module                                 | Send data to phone over bluetooth                              |
| 1            | 6 way Male-Female PCB Jumper Cable (Dupont Connectors) | Allows connecting the bluetooth module remotely                |
| 8            | Neodymium Puck Magnets                                 | Place on hub and motor shaft to trigger hall effect sensors    |
| 1            | eChook PCB                                             |                                                                |

![Kit Contents](.gitbook/assets/img\_20180129\_190858.jpg)

## Tools and Consumables Required

Some tools and consumables will be required to build the kit and integrate the sensors to the car:

* Soldering Iron and Solder
* Solder Sucker or solder wick (handy correcting any build errors)
* Wire Snips
* Small flathead screwdriver&#x20;
* Multimeter
* Wire for connecting sensors remote to the board



## Board Version differences

v1.3 is the first production version as sold by Greenpower, earlier versions are prototypes. This guide is aimed at V1.3 but should apply to all boards unless stated below.

### V1.0

Any V1.0 board will already be assembled and partially tested so the ‘build stage’ is not required - you can skip this bit!

The connection outputs and component references changed after V1.0, so the pin out's aren't all compatible!

NOTE: for V1.0 it is important that before power is applied to the board the DCDC converter is set to the right voltage with the Arduino, Bluetooth module and op-amp unplugged. Later boards do not have adjustable power supplies so this instruction no longer applies.

### V1.1, V1.2

These revisions had the following changes:

* Changed to a fixed 5V DC-DC regulator.
* Increased solder pad sizing.
* Moved all components to the same side of the PCB.
* Altered Board layout.
* Added labelled multimeter test points to the bottom of the board.
* Moved the BT module off-board
* Improved Silkscreen.
* Increased tolerances to avoid manufacturing errors.
* Added logo and component values to silkscreen.
* Changed to a white board (solder mask) with black silkscreen.

The initial batch of V1.2 boards had some manufacturing errors, resulting in it being easy to bridge a pad to the ground plane when soldering the board. This drove the change in tolerances, increasing the overlap of the solder mask over the ground plane around component pads. The issue is detailed [here](http://wechook.com/?p=778).

V1.2 was the first board sold in kit form - the V1.3 build instructions apply to V1.2 as well.

### V1.3

The first version of the board sold in kit form through Greenpower for the 2018 season.

Changelog:

* Added current sensor multimeter test point.
* Changed silkscreen to reflect new echook.uk website.

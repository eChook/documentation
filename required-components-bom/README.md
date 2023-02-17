# The eChook Nano Kit

Greenpower sell an eChook Nano kit that contains all the hardware and sensors needed to get eChook telemetry running on a greenpower car. The android app and live data website are free to use, no kit purchase necessary.

This is a DIY kit containing of the eChook PCB, all components required to populate the PCB as well as sensors for Current, Temperature (x2) and Rotation (Wheel and motor shaft).

![](<../.gitbook/assets/image (5).png>) ![](<../.gitbook/assets/image (12) (1).png>)

### Buying or DIYing the eChook nano

The kit is sold exclusively by Greenpower through their Green power store [here](https://www.greenpower.co.uk/product/340).

If you want to source the components yourself, the bare eChook nano GPT board is available from the eChook shop [here](https://shop.echook.uk).

If you want to go totally DIY, or tweak the PCB to your own requirements, the schematics and PCB layouts are Open Sourced and available on [GitHub](https://github.com/eChook/eChook-Nano-PCB).



### Kit Contents:

| **Quantity** | **Component**                                          | **Use**                                                      |
| ------------ | ------------------------------------------------------ | ------------------------------------------------------------ |
| 1            | eChook nano PCB                                        |                                                              |
| 1            | 470r Resistor                                          | Voltage drop for LED                                         |
| 12           | 1k Resistor                                            | Protection for Arduino pins                                  |
| 2            | 4k7 Resistor                                           | Input Resistors for current differential amplifier           |
| 4            | 10k Resistor                                           | Feedback on Differential amp and pull ups for Thermistors    |
| 2            | 16k Resistor                                           | 24v and 12v Potential Dividers                               |
| 1            | 47k Resistor                                           | Post amp current filter                                      |
| 2            | 82k Resistor                                           | 24v and 12v Potential Dividers                               |
| 1            | Green LED, 5mm                                         | Indicator LED on PCB                                         |
| 1            | BC547 NPN Transistor                                   | Amplification stage of PWM output on PCB                     |
| 3            | Ceramic Capacitor 1uF                                  | Low Pass filtering on some sensors                           |
| 1            | 22uF 50v Electrolytic Capacitor                        | Input voltage smoothing for the regulator                    |
| 2            | 47nF Ceramic Capacitor                                 | Smoothing Capacitors for current sensor  (not on PCB)        |
| 1            | 4.7nF Ceramic Capacitor                                | Smoothing Capacitors for current sensor (not on PCB)         |
| 1            | 0.25A Radial Resettable Fuse                           | Over current protection (Short Circuit)                      |
| 1            | 8 Way DIP Socket                                       | Socket for Op-Amp                                            |
| 1            | Microchip MCP6002 Dual Op Amp                          | Used in differential amplifier for current input             |
| 2            | 15 way SIL 2.54mm Female PCB Socket                    | Socket for Arduino                                           |
| 1            | 6 way SIL 2.54mm Female PCB Socket                     | Socket for Bluetooth Module                                  |
| 1            | 5v 1A Voltage Regulator (Tracopower TSR 1-2450)        | Take 24v from the car and provide a robust 5v to the Arduino |
| 1            | Rectifier Diode, 50V 1A                                | Reverse Polarity Protection                                  |
| 2            | NTC Thermistor 10kΩ@25°                                | Temp Sensor (not on PCB)                                     |
| 2            | Hall Effect Sensor (A1101EUA-T)                        | Sensor for wheel/motor rpm (not on PCB)                      |
| 1            | Current Sensor (LEM HAIS 50p)                          | Senses current in the 24v cable from the battery.            |
| 3            | 4 pin Pluggable Terminal 5.08mm                        | Connectors                                                   |
| 2            | 3 pin Pluggable Terminal 5.08mm                        | Connectors                                                   |
| 1            | 2 pin Pluggable Terminal 5.08mm                        | Connectors                                                   |
| 1            | 3 pin Pluggable Terminal 3.81mm                        | Connectors                                                   |
| 1            | Arduino Nano                                           | The Brain of the eChook                                      |
| 1            | USB Cable for Arduino                                  | Connect Arduino to PC                                        |
| 1            | HC-05 Bluetooth module                                 | Send data to phone over bluetooth                            |
| 1            | 6 way Male-Female PCB Jumper Cable (Dupont Connectors) | Allows connecting the bluetooth module remotely              |
| 8            | Neodymium Puck Magnets                                 | Place on hub and motor shaft to trigger hall effect sensors  |

![Kit Contents](../.gitbook/assets/img\_20180129\_190858.jpg)

## Tools and Consumables Required

Some tools and consumables will be required to build the kit and integrate the sensors to the car:

* Soldering Iron and Solder
* Solder Sucker or solder wick (handy correcting any build errors)
* Wire Snips
* Small flathead screwdriver&#x20;
* Multimeter
* Wire for connecting sensors remote to the board



##

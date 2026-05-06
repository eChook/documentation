# First Power On

This page is for initial board safety checks and first power-up **before** fitting the Arduino, Bluetooth module, and op-amp.

## Pre Power On Tests

The Arduino, Bluetooth Module and Op-Amp have not been connected yet as these are the components most susceptible to being damaged by an error with the board. Before plugging in these final components or powering up the board it is sensible to carry out some simple checks.

#### Visual Inspection

Visually inspect the soldering, looking for any areas where the solder has bridged connections, creating short circuits, especially on the closer op-amp, Arduino and Bluetooth pins. If any shorts are found, fix them. A small magnifying glass can be useful for identifying issues here.

#### Test Points / Multimeter Inspection

On the back of the PCB there are multiple 3mm silver circles, each with a label ending in 'TP'. These are test points, designed to give easy multimeter access for testing the board.

Use the following test points as your continuity-check references:

<table><thead><tr><th width="202">Label</th><th>Signal</th></tr></thead><tbody><tr><td>GND</td><td>Ground</td></tr><tr><td>PWR5VTP</td><td>+5v Power</td></tr><tr><td>BattTotalVTP</td><td>24V battery signal after potential divider circuit (0-5v)</td></tr><tr><td>Batt1VTP</td><td>12V battery signal after potential divider circuit (0-5V)</td></tr><tr><td>ThrottleTP</td><td>Input voltage from the throttle (0-5v)</td></tr><tr><td>CurrentTP</td><td>Output from current differential amplifier circuit / Current signal into to Arduino</td></tr><tr><td>Temp1TP</td><td>Temperature 1 input to the Arduino</td></tr><tr><td>Temp2TP</td><td>Temperature 2 input to the Arduino</td></tr><tr><td>BrakeTP</td><td>Signal in from Brake switch</td></tr></tbody></table>

To see exactly where these test points are in the circuit, take a look at the [Circuit Schematics](../circuit-schematics/).

The multimeter tests check that there are no short circuits on the board. Place the multimeter into continuity mode (aka beep mode) and check that there is no continuity between any of the pads. The most important checks are that no other test point has continuity to the ground test point, and that no other test point has continuity to the 5V test point. There should also be no continuity between any of the other test points.



## First Power On

Follow this order for first power-up:

1. If a bench power supply is available, use this as the safest power source.
2. Set the supply voltage to 24V and current limit to around 0.3A.
3. Attach power to the 24v and ground pins on the power connector.
4. If a bench supply is not available, a pair of Greenpower batteries can be used, but there **must** be a fuse inline between the battery and board, close to the battery. Preferably 1A, but 5A is sufficient.

The pinout for the power socket can be found here: [Connecting the eChook to the Car](../connecting-the-echook-to-the-car/#connector-pin-out).

Once connected, assuming the current limiter hasn’t been hit, use the multimeter to check that the 5V rail on the board is reading 5V. If it is not, check the soldering of the power module and ensure that 24V is reaching it.

## Plug in the Final Components

Once you have completed the above checks, plug in the Arduino, Bluetooth module and op-amp.

* The Arduino plugs in with the USB connection to the outside edge of the PCB.&#x20;
* The op-amp has a dot on one corner, this goes with the notched end of the 8-pin socket.
* The Bluetooth module can connect directly to the 6-pin header on the PCB, or through the included 6 way jumper cable. Ensure that it is plugged in the right way round using the silkscreen labels on the PCB and bluetooth module.

Power up and you should get some flashing LEDs on the Arduino and the BT module. This is now a complete, but unprogrammed eChook Nano board.

At this point, the board is assembled, powered, and ready for Arduino programming.

If you want to proceed with fitting the sensors to the car and wiring it all up before programming the Arduino, jump ahead to '[Connecting the eChook to the Car](../connecting-the-echook-to-the-car/)'.

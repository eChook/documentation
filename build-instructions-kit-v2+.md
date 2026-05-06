# Build Instructions (Kit V2+)

The V2 board comes preassembled, however there is still a little assembly needed to attach the Bluetooth module and some soldering on the sensor boards.

## Before You Start

This page is for **Kit V2+** boards. The main PCB is preassembled, but the Bluetooth module and sensor boards still require assembly.

## Bluetooth Module

On V2, this gets attached to the board rather than on a length of wire. In the bag with the module there should be a 3D printed plastic 'y' shaped support and a small Philips head screw.

Assemble in this order:

1. Bend the header pins on the HC-05 Bluetooth module to be vertical. Do this carefully, one pin at a time to avoid putting too much force through the PCB.
2. Slide the 'Y' support over the module, with the bottom of the Y pointing in the same direction as the pins.
3. Insert this into the 6 pin BT header on the main eChook board, pressing the bottom of the support into the hole in the board.
4. Secure the support from the bottom of the board with the included screw.

## Magnet Sensing Boards

The Magnet Sensor boards come preassembled, other than the magnet sensor (Allegro A1101 hall effect sensor) itself, which is a small 3 pin component, requires soldering to the board.

1. Bend the pins. Place the top of the sensor, chamfered edges up, inline with the PCB through hole mounting point with it's legs over the end of the board, and bend the legs down 90 degrees. This ensures the legs are bent at the right point.
2. Bend the legs apart slightly so that they fit into the three mounting holes, with the sensor body over the white 'eC' marked square on the board. The flat side of the sensor goes against the board, the chamfered side faces away from the board.
3. Solder the three legs in place.
4. A spot of hot glue, or a wrap of electrical tape should be used to secure the sensor to the board to avoid damage from vibration in the car.

## Current Sensor Board

{% embed url="https://youtu.be/21s8vgiA-Jw" %}

In the bag with the LEM HAIS-50-P current sensor is a small PCB, three capacitors, and a connector and wire.

Solder the components from smallest to largest - start with the three capacitors. The two 47nF capacitors are marked 473, and the 4.7nF capacitor is marked 472. They are not polarity sensitive, so it does not matter which way around they go.

Next, mount the connector header, with the 'gap' side towards the edge of the board. Solder only one pin initially and check that it is fitted flush and square with the board. If it is not, reheat that one joint and adjust its position. Once correct, solder the remaining three pins.

Finally, fit the current sensor. It only fits in one orientation. As with the connector, solder one of the larger mounting pins first, check and correct its position if necessary, then solder the remaining mounting pin and 4 smaller connections.

## Arduino

Finally, plug in the Arduino to the two 15-pin sockets with the USB plug at the board edge and you're all done!

At this point, the V2+ assembly is complete and the board is ready for Arduino programming.

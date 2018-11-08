# First Power On

## Pre Power On Tests

The Arduino, Bluetooth Module and Op-Amp have not been connected yet as these are the components most susceptible to being damaged by an error with the board. Before plugging in these final components or powering up the board it is sensible to carry out some simple checks.

First, visually inspect the soldering, looking for any areas where the solder has bridged connections, creating short circuits, especially on the closer op-amp, Arduino and Bluetooth pins. If any shorts are found, fix them. A small magnifying glass can be useful for identifying issues here.

Use a Multimeter to check for a short circuit between ground and power. There is a labelled test point on the bottom of the PCB for ground and 5v, for 24v use the labelled pin on the voltage regulator. Test that there is no connection between 24v, 12v, 5v and GND using the continuity test function \(beeper\) on the multimeter. If any of these tests show a short circuit this _must_ found and fixed before going any further.

## First Power On

If a bench power supply is available, this is the safest power source to use. Set the voltage to 24V and the current limit to around 0.3A and attach to the power connectors 24v and ground pins. If a bench power supply isn’t available a pair of Greenpower batteries can be used, but there **must** be a fuse inline between the battery and the board. Preferably 1A, but 5A is sufficient.

The pin out for the power socket can be found here: [Connecting the eChook to the Car](../connecting-the-echook-to-the-car/#connector-pin-out).

Once connected, assuming the current limiter hasn’t been hit, use the multimeter to check that the 5V rail on the board is reading 5V. If it isn’t check the soldering of the power module and ensure that the 24V is getting to it.

## Plug in the Final Components

Once you have completed the above checks, plug in the Arduino, Bluetooth module and op-amp.

* The arduino plugs in with the USB connection to the outside edge of the PCB. 
* The op-amp has a dot on one corner, this goes with the notched end of the 8-pin socket.
* The Bluetooth module can connect directly to the 6-pin header on the PCB, or through the included 6 way jumper cable. Ensure that it is plugged in the right way round using the silkscreen labels on the PCB and bluetooth module.

Power up and you should get some flashing LEDs on the Arduino and the BT module. This is now a complete, but unprogrammed eChook nano board.

If you want to proceed with fitting the sensors to the car and wiring it all up before programming the Arduino, jump ahead to '[Connecting the eChook to the Car](../connecting-the-echook-to-the-car/)'.


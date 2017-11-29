## Pre Power On Tests

The Arduino, Bluetooth Module and Op-Amp have not been connected yet as these are the components most susceptible to being damaged by an error with the board. Before plugging in these final components or powering up the board it is sensible to carry out some simple checks.

First, visually inspect the soldering, looking for any areas where the solder has bridged connections, creating short circuits, especially on the closer op-amp, Arduino and Bluetooth pins. If any shorts are found, fix them. A small magnifying glass can be useful for identifying issues here.

Use a Multimeter to check for a short circuit between ground and power. There are labelled test points for these signals on the bottom of the PCB. Test that there is no connection between 24v, 12v, 5v and GND using the continuity test function \(beeper\) on the multimeter. If any of these tests show a short circuit this _must_ found and fixed before going any further.




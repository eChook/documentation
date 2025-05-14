# Power

## 24V

## Power not getting to the Tracopower DCDC Module

24V is being supplied at the input but isn't seen at the pins of the DCDC power module. The most likely cause for this is that the rectifier diode is the wrong way around. This triggers the short circuit protection when the voltage supply is correct - the diode creates a short circuit between 24V and ground and causes the polyfuse to activate, stopping any voltage going to the rest of the board. To fix, reverse the diode on the PCB

## 5V

If there is 24V at the input pin to the DCDC Power Module, but no voltage on the 5V rail, the most likely cause is a short to ground on the 5V rail, which causes the short circuit protection on the DCDC Power module to activate.&#x20;

Use a multimeter in continuity mode to check between the 5V rail and Ground. If it beeps, you have a short circuit. If it doesn't beep, check that you have 24V going into the DCDC power module. If not, look at the 24v section above, if you do, the power module needs replacing.

First unplug all connectors where 5V goes out to the wiring harness and see if the 5V rail recovers on the eChook board. (V2.0+ boards, the red error LED will illuminate next to the relevant connector if there is a short in the harness, it won't affect the eChook board)

If the 5V rail doesn't recover, move on to removing the Bluetooth module, Arduino then op-amp (U3 chip, PCB V1.x only) from the board.

If there is still an issue, there is a short directly on the PCB. This could be an assembly issue, or physical damage to the PCB.

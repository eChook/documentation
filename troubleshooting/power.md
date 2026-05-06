# Power

## Fault LEDs

If the 24V fault LED is lit, the board is trying to draw more than 300mA from the 24V supply. This usually indicates a short circuit on the PCB. Also check for any conductive items under the PCB. A failed (hot) arduino can also cause this to light.

If any of the 5V fault LEDs are lit, there is likely a harness fault causing a short circuit in the harness attached to the connector nearest the lit fault LED. This can also indicate a failed sensor if it has failed short-circuit.

## 24V

## Power not getting to the Tracopower DCDC Module

If 24V is present at the input but is not seen at the pins of the DCDC power module, the most likely cause is that the rectifier diode is installed in the wrong orientation. This triggers short-circuit protection when the voltage supply is correct: the diode creates a short circuit between 24V and ground, causing the polyfuse to activate and stop voltage reaching the rest of the board.

To fix this (V1 boards only), reverse the diode on the PCB and verify its orientation against the board marking before powering up again.

## 5V

If there is 24V at the input pin to the DCDC power module but no voltage on the 5V rail, the most likely cause is a short to ground on the 5V rail. This causes the short-circuit protection on the DCDC power module to activate.&#x20;

Use a multimeter in continuity mode to check between the 5V rail and ground:
- If it beeps, you have a short circuit.
- If it does not beep, check that you have 24V going into the DCDC power module.
  - If not, refer to the 24V section above.
  - If you do, the power module needs replacing.

First, unplug all connectors where 5V goes out to the wiring harness and check whether the 5V rail recovers on the eChook board. (On V2.0+ boards, the red error LED will illuminate next to the relevant connector if there is a short in the harness, and it will not affect the eChook board.)

If the 5V rail doesn't recover, move on to removing the Bluetooth module, Arduino then op-amp (U3 chip, PCB V1.x only) from the board.

If there is still an issue, there is a short directly on the PCB. This could be an assembly issue, or physical damage to the PCB.

If you need further help, contact us on the forum or webchat.

# Current Sensor

## Current Sensor Troubleshooting

If you are not receiving a current reading from the eChook, or are getting an obviously wrong reading (for example, multiple amps when no current is flowing), first isolate where the problem is in the system:

1. Test the current sensor. \
   With no current flowing (ideally no cable passing through the sensor) and the eChook powered from 24 V, measure the voltages on the eChook board connector to the current sensor, relative to ground. You should see 5 V on the 5 V supply connection, and very close to 2.5 V on both the Reference and Sense wires. \
   If the Ref and/or Sense wires are not reading 2.5 V, disconnect the affected wire from the eChook board (just that single wire, while keeping power to the current sensor) and measure the voltage again.
   1. If the voltage returns to 2.5 V when disconnected, there is a hardware issue on the telemetry board.
   2. If the voltage is unchanged when disconnecting the wire, the current sensor has failed and requires replacing. Continue testing to check that there is not also a cascade failure on the board.
   3. If both wires read 2.5 V as expected, the current sensor is most likely working. If you can pass a known current through it and check the voltage readings, you should see the Sense voltage rising above the Reference voltage.
2. Test the op-amp circuit.\
   The op-amp circuit (component U3 on the telemetry board) compares Reference and Sense voltages from the current sensor and outputs the voltage difference multiplied by 2. This output can be checked by measuring the voltage between GND and the Current Test Point on the bottom of the board.\
   With the current sensor plugged in and no current flowing, after verifying that the Ref and Sense connections show \~2.5 V, measure the voltage at the Current Test Point. If this is not very close to 0 V (there will normally be a few mV present), the op-amp has failed and needs replacing. The required component is a [Microchip 6002 PDIP](https://octopart.com/mcp6002-i%2Fp-microchip-96737).

If you have experienced a current sensor failure, we would be very interested to know the circumstances (when the kit was purchased, how long it has been in use, what was happening when the failure was noted, etc.). We are aware of a few failures and are trying to gather as much data around them as possible. Please email us at info@echook.uk, or contact us on the forum or webchat.

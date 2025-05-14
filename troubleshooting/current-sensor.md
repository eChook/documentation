# Current Sensor

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

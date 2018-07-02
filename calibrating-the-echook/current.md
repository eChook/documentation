# Current

The current sensor is calibrated during manufacture. Any inaccuracies in the measurement are introduced by tolerances in the differential amplifier. Resistors with a 1% tolerance have been used here. As such the default calibration should be very close and re-calibrating the current sensor should not make a huge difference to the readings.

To calibrate the current a bench power supply **with a current limit** function is required. With the power supply off, feed a length of wire through the current sensor, then connect it across the +ve and -ve terminals of the power supply as a Short Circuit - doing this might feel very wrong!

If the power supply does not have a current readout, connect a multimeter set to measure current in series with the wire. Note the maximum current on the multimeter \(normally 10A\) and be sure not to exceed this later!

Turn the current limit down to 0 and switch on the power supply. Slowly increase the current limit to control the current flowing through the sensor. Due to the very low voltages involved the wire will not get too hot, even when passing considerable current, however make sure to keep an eye on the wire temperature.

Calibrating at around the expected current draw of 20 to 30 Amps during a race is sensible, but few power supplies will be able to provide this amount of current. Coil the wire through the sensor multiple times - the detected current is multiplied by the number of times the wire passes through the sensor. If the power supply is outputting 2A, a wire coiled through the sensor 5 times would give the eChook a reading of 10 Amps.

Note the current being output by the power supply - multiplied as required if the wire passes through the current sensor multiple times. Now use a multimeter to measure the voltage on pin A2 of the Arduino. There is a linear relationship between current and voltage so this is enough to calculate the ratio between them.

$$
(I_{supply} * Num.PassesThroughSensor)/V_{A2} = Multiplier
$$

Open the Calibration.h file and update the CAL\_CURRENT variable with the results of your calculation.

```c
const float CAL_CURRENT = 37.55;
```


# Voltage

## Calibrating 24v

Due to tolerances on the resistors used to drop the voltage from 24v to a level readable by the arduino \(0-5v\), each board will require a slightly different calibration. The step down is linear, so only one measurement needs to be taken.

To calibrate this reading, connect the +24v pin to a power source and use a multimeter to measure the voltage. For this example, lets call it 23.5v. Now measure the voltage on the other side of the potential divider, which is Pin A0 on the Arduino. For this example lets call it 3.6v. Now you need to calculate the ratio between them:

`Supply Voltage / Arduino Voltage=23.5 / 3.6=6.53`

Now enter this figure into the Calibration.h file as variable `CAL_VOLTAGE_TOTAL` . Reflash the Arduino for the calibration to take effect.

## Calibrating 12v

Calibration is by the same method as 24V above. Measure the voltage at the 12V input and the voltage to pinA7of the Arduino and divide the former by the latter to obtain a multiplier to use in the code.

Open the Calibration.h file and update the `CAL_BATTERY_LOWER` variable with the results of your calculation.


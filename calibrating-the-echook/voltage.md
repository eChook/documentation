# Voltage

## Calibrating 24v

Due to tolerances on the resistors used to drop the voltage from 24v to a level readable by the arduino (0-5v), each board will require a slightly different calibration. The step down is linear, so only one measurement needs to be taken.

To calibrate this reading, connect the +24v pin to a power source and use a multimeter to measure the voltage. For this example, lets call it 23.5v. Now measure the voltage on the other side of the potential divider, which is the 24v test point on the PCB, and Pin A0 on the Arduino. For this example let's call it 3.6v. Now you need to calculate the ratio between them:

$$
{V_{Supply} / V_{Arduino}} = 23.5/3.6 = 6.53
$$

Now enter this figure into the Calibration.h file as variable `CAL_BATTERY_TOTAL` . Reflash the Arduino for the calibration to take effect.

```c
const float CAL_BATTERY_TOTAL       = 6.53;
```

## Calibrating 12v

Calibration is by the same method as 24V above. Measure the voltage at the 12V input and the voltage to pin A7 of the Arduino and divide the former by the latter to obtain a multiplier to use in the code.

$$
V_{input}/V_{pin_A7} = calibration Value
$$

Open the Calibration.h file and update the `CAL_BATTERY_LOWER` variable with the results of your calculation.

```c
const float CAL_BATTERY_LOWER       = 3.071;
```

## Reference Voltage

```c
const float CAL_REFERENCE_VOLTAGE   = 5;
```

This calibration option is a throwback to when eChook boards had adjustable DC-DC regulators and having exactly 5V powering the Arduino wasn't guaranteed. With the fixed 5V Tracopower DC-DC regulators, the output should be exactly 5V, and as such, this setting should be left at 5V.

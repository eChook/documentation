# Voltage

- **V2 Arduino code (code version 2.0 or later):** enter these calibration values in the calibration web app at [configure.echook.uk](https://configure.echook.uk).
- **Legacy Arduino code (below version 2.0):** update these values in `calibration.h` and re-upload the code.

## Calibrating 24V

Due to resistor tolerances in the divider from 24V to an Arduino-readable level (0-5V), each board needs a slightly different calibration. The step-down is linear, so one measurement pair is enough.

Follow this order:

1. Connect the +24V pin to a power source and use a multimeter to measure supply voltage. For this example, use 23.5V.
2. Measure the voltage on the other side of the potential divider (the 24V test point on the PCB and pin A0 on the Arduino). For this example, use 3.6V.
3. Calculate the ratio between them:

$$
{V_{Supply} / V_{Arduino}} = 23.5/3.6 = 6.53
$$

4. For legacy code versions, enter this figure into `calibration.h` as `CAL_BATTERY_TOTAL`. Reflash the Arduino for the calibration to take effect.
5. For V2 code versions, enter the same value in the web app.

```c
const float CAL_BATTERY_TOTAL       = 6.53;
```

## Calibrating 12V

Calibration is by the same method as 24V above:

1. Measure the voltage at the 12V input.
2. Measure the voltage to pin A7 of the Arduino.
3. Divide the former by the latter to obtain a multiplier to use in the code.

$$
V_{input}/V_{pin_A7} = calibration Value
$$

4. For legacy code versions, open `calibration.h` and update `CAL_BATTERY_LOWER` with the result.
5. For V2 code versions, enter the same value in the web app.

```c
const float CAL_BATTERY_LOWER       = 3.071;
```

## Reference Voltage

```c
const float CAL_REFERENCE_VOLTAGE   = 5;
```

This calibration option is a throwback to when eChook boards had adjustable DC-DC regulators and having exactly 5V powering the Arduino wasn't guaranteed. With the fixed 5V Tracopower DC-DC regulators, the output should be exactly 5V, and as such, this setting should be left at 5V.

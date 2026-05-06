# Wheel Speed and Motor RPM

There are two factors that affect the wheel speed reading taken by the eChook: the number of magnets on the wheel, and the circumference of the wheel.

- **V2 Arduino code (code version 2.0 or later):** enter these values in the calibration web app at [configure.echook.uk](https://configure.echook.uk).
- **Legacy Arduino code (below version 2.0):** both values are set in `calibration.h`.

Set the values in this order:

1. Count the number of magnets on the wheel.
2. Measure wheel circumference as the distance travelled in one full wheel rotation (the outermost circumference of the tyre, not simply 2πr for a 16” wheel).
   - You can measure this with a flexible tape measure, or by marking the tyre contact point on the floor, rolling one full rotation, and measuring between the two marks.
   - Use meters for the units.
3. Count the number of magnets on the motor shaft for motor RPM.
4. Enter the values:
   - For V2 code versions, enter them in the web app.
   - For legacy code versions, enter them in `calibration.h` and re-upload the code to the Arduino.

For legacy code versions, enter the new figures into the `calibration.h` file and re-upload the code to the Arduino.

```text
const int       CAL_WHEEL_MAGNETS        = 6; //Number of magnets on wheel
const int       CAL_MOTOR_MAGNETS        = 3; // Number of magnets on motor shaft for hall effect sensor
const float     CAL_WHEEL_CIRCUMFERENCE  = 1.178; //Outer circumference of tyre, in Meters. i.e. the distance travelled in one revolution
```


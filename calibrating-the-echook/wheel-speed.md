# Wheel Speed and Motor RPM

There are two factors that affect the wheel speed reading taken by the eChook. The number of magnets on the wheel, and the circumference of the wheel. Both of these are variables in the calibration.h file.

The number of magnets is simple. The wheel circumference is the distance travelled in one rotation of the wheel, so the outermost circumference of the tyre, not simply 2πr for a 16” wheel. This can either be measured with a flexible tape measure, or placing the wheel on the floor with the valve at the bottom and marking the contact point, rolling it for one rotation, placing a second mark at this point, then measuring between marks. Use meters for the units.

The motor RPM is simply dependant on the number of magnets on the motor shaft. Enter this in the calibration.h file accordingly.

Enter the new figures into the calibration.h file and re-upload the code to the Arduino.

```text
const int       CAL_WHEEL_MAGNETS        = 6; //Number of magnets on wheel
const int       CAL_MOTOR_MAGNETS        = 3; // Number of magnets on motor shaft for hall effect sensor
const float     CAL_WHEEL_CIRCUMFERENCE  = 1.178; //Outer circumference of tyre, in Meters. i.e. the distance travelled in one revolution
```


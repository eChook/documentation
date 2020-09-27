# Wheel and Motor RPM

Knowing the Wheel and Motor RPM, especially for cars with multiple gears, is very useful for determining gear ratios used around the track and ensuring the motor is run in it’s most efficient RPM range.

Two non-latching hall effect sensors are included in the eChook kit. For the pin out, google the name printed on them to find the data sheet. They will require 5V, GND and have one output. This output goes to the Motor RMP or Wheel RPM input on the eChook. No specific pin out is given here as different sensors have been used through the various eChook hardware iterations.

Positioning the sensor on the car is the more difficult part. The hall effect sensor is triggered by magnets that need to be attached to the motor shaft/wheel. The eChook kit contains 10 5mm puck magnets for this.

The tapered side of the hall effect sensor is the ‘sensing’ side. This will only pick up one pole of the magnet, **so check magnet polarity!** If you use the app you can watch the RMP as you wave a magnet over the sensor to determine the correct polarity - it will give a speed or RPM reading only when the polarity is correct.

{% hint style="info" %}
If the magnets aren't all in the same polarity, the speed or motor RPM will read too high!
{% endhint %}

Magnets need to be securely mounted and evenly spaced on the motor shaft and wheel, the suggested number is three on the motor shaft and 6 on the wheel. Increasing the number will give a higher resolution reading. The number of magnets used needs to be specified in the calibration.h file. Whilst not pretty, we have found electrical tape effective in securing magnets to the motor shaft, and have used 3D Printed mounts to secure magnets to the wheel.

The hall effect sensor needs to be mounted very close to the magnets, with the tapered facing them. The distance between magnets and sensor needs to be 1-3mm for the small 1x3mm disc magnets. We have used both folded sheet aluminium and 3D printed brackets to hold the hall effect sensors. Larger magnets may allow for a larger sensing gap.


# Calibrating Wheel Speed

There are two factors that affect the wheel speed reading taken by the eChook. The number of magnets on the wheel, and the circumference of the wheel. Both of these are variables in the calibration.h file.

The number of magnets is simple. The wheel circumference is the distance travelled in one rotation of the wheel, so the outermost circumference of the tyre, not simply $$π*16$$ for a 16” wheel. This can either be measured with a flexible tape measure, or placing the wheel on the floor with the valve at the bottom and marking the contact point, rolling it for one rotation, placing a second mark at this point, then measuring between marks.

Enter the new figures into the calibration.h file and re-upload the code to the Arduino.

  



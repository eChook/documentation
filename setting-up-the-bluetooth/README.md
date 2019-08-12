# Setting up the Bluetooth

This is a step that should only need doing once to each bluetooth module. It comes programmed from the factory called ‘HC05’ and set to a baud rate of 9600. Before use, we need to set the baud rate to 115200, and change the name - potentially to that of the car it will be fitted to.

When the eChook Arduino code is open in the Arduino IDE there will be two tabs, the second of which will be called ‘Calibration.h’. The first parameters in this file are the bluetooth settings.

```text
//Bluetooth Settings
const String CAL_BT_NAME     = "your-car-name-here";
```

Save and upload the new code to the Arduino.

Now the Arduino needs to send these settings to the bluetooth module. To transfer these settings from the Arduino to the HC-05 bluetooth module follow these steps:

1. Insert the Arduino into the eChook board and unplug the HC-05 Bluetooth module.
2. Power the eChook board from a source _other than the USB_ on the Arduino. Ensure that the USB is unplugged for this procedure. A 12v or 24v battery connected to the main power input is ideal.
3. Press the small button next to the ‘EN’ pin on the bluetooth module and hold this down while plugging it into the eChook nano board. Release once plugged in.
4. The bluetooth module LED should now be blinking slowly. Two seconds on, two seconds off. If this is not the case repeat step 3.
5. Press the reset button on the Arduino. The ‘L’ LED on the arduino should blink quickly 3 times and the LED on the Bluetooth module should resume to flashing quickly, signifying it is waiting for a connection. The module will now appear on a phone under the name specified.
6. If the bluetooth module LED will keeps blinking slowly the configuration has failed. Go back to step 3 and repeat the process.

The board is now ready to be paired with a phone!

{% hint style="info" %}
Note: Apple devices will not be able to discover the eChook board as Apple does not implement the serial over bluetooth protocol that it uses. Android/Windows/Linux etc will be able to discover it.
{% endhint %}


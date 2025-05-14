# Setting up the Bluetooth

This is a process that should only need doing once to each bluetooth module. It comes programmed from the factory called ‘HC05’ and set to a baud rate of 9600. Before use, we need to set the baud rate to 115200, and change the name - potentially to that of the car it will be fitted to.

There are two steps to the process. The first is entering the bluetooth name you want and saving that to the Arduino. The second is using the Arduino to send the configuration to the bluetooth module itself.

### Setting the Bluetooth name

As of eChook Arduino code version 2.0, you can set the name by going to configure.echook.uk in either Chrome or Edge browsers and connecting your eChook. For more information see the [Calibrating the eChook](../calibrating-the-echook/) section.

Alternatively, the old method still works. When the eChook Arduino code is open in the Arduino IDE there will be a tab called ‘Calibration.h’. The first parameters in this file are the bluetooth settings.

```
//Bluetooth Settings
const String CAL_BT_NAME     = "your-car-name-here";
```

Save and upload the new code to the Arduino.

### Configuring the HC-05 Bluetooth module

These steps differ between versions of the board. If you have a V2.0+ board and have cut the JP3 jumper on the back of the board, this disables the automatic configuration, and you need to follow the V1.x procedure.

{% tabs %}
{% tab title="PCB V2.0+ (Black)" %}
{% hint style="danger" %}
We are aware of a few of the eChook Nano V2.0 kits from early 2025 being sent out with incompatible Bluetooth modules. If you have a V2.0 kit, and are having issues getting data in the app, please see the [Bluetooth Troubleshooting Section](../troubleshooting/bluetooth.md).
{% endhint %}

V2.0+ of the board automatically configures the bluetooth module each time it is first powered on. Once you have set the bluetooth name, disconnect the USB, wait a couple of seconds and reconnect it. The red LED on the bluetooth module should come on for \~1s, turn off, then start flashing. This indicates a successful configuration.\
\
To see more information on the process, open the Arduino IDE, and start the serial monitor, connected to the Arduino Nano Every COM port. Now perform the power cycle described above, and the eChook will print debug information to the serial monitor.
{% endtab %}

{% tab title="PCBV1.x (White)" %}


1. Insert the Arduino into the eChook board and unplug the HC-05 Bluetooth module.
2. Power the eChook board. If using an Arduino Nano Clone, use a power source _other than the USB_ on the Arduino and ensure that the USB is unplugged for this procedure. The Arduino Nano Every works with USB power.
3. Press the small button next to the ‘EN’ pin on the bluetooth module and hold this down while plugging it into the eChook nano board. Release once plugged in.
4. The bluetooth module LED should now be blinking slowly. Two seconds on, two seconds off. If this is not the case repeat step 3.
5. Press the reset button on the Arduino. The ‘L’ LED on the arduino should blink quickly 3 times and the LED on the Bluetooth module should resume to flashing quickly, signifying it is waiting for a connection. The module will now appear on a phone under the name specified.
6. If the bluetooth module LED will keeps blinking slowly the configuration has failed. Go back to step 3 and repeat the process.
{% endtab %}
{% endtabs %}

The board is now ready to be paired with a phone!

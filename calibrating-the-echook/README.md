# Calibrating the eChook

From the default calibration values, a correctly assembled eChook board will give reasonably accurate data. This section takes you through calibrating each input in turn. Each calibration routine involves taking some readings with external equipment - generally a multimeter - some simple calculations, and updating a calibration variable on your eChook nano.

On earlier versions of the board (with Arduino code below version 2.0, released in Jan 2024) updating the calibration requires updating the calibration.h file, then reflashing the Arduino with the new values. Boards running V2.0 can be connected to a computer, and the calibrations read and updated via a web interface.

The signals that will benefit most from calibration are speed, motor RPM and temperature, followed by voltages, and then current.

### Calibration Web Interface

The calibration web interface is available at [configure.echook.uk](https://configure.echook.uk). Please note it requires either Chrome or Edge desktop browsers. There is no mobile browser support.

Unplug the bluetooth module, and connect your eChook to your computer. Navigate to the [configuration webapp](https://configure.echook.uk) and click connect. A browser menu will open - select the eChook's COM port from the list and press connect. After a few seconds the screen below should open.

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

To update a calibration, enter the new number in the corresponding box. Any changes are higlighted, and the bottom right button will reflect how many changes you have entered from the configuration saved on the eChook. To save the changes to the eChook, press the bottom right button. These will be reflected immediately in the values being read out on screen.

Once you have a configuration you are happy with, it is recommended to take a backup using the 'Backup Config' button. Keep this somewhere safe.

The next few pages were  written for the old system of updating the calibration.h file. For V2.0+ Simply enter the numbers into the web app instead.

### Issues?

As this has only just been rolled out to a wider audience, I anticipate some teething issues. Please feed back any issues on the forum, or via email to info@echook.uk.

The biggest issue I anticipate - **Unplug the Bluetooth Module!** :)


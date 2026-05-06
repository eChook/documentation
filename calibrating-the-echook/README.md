# Calibrating the eChook

From the default calibration values, a correctly assembled eChook board will give reasonably accurate data. This section takes you through calibrating each input in turn. Each calibration routine involves taking some readings with external equipment - generally a multimeter - some simple calculations, and updating a calibration variable on your eChook nano.

On earlier versions of the board (with Arduino code below version 2.0, released in Jan 2024), updating the calibration requires editing the calibration.h file, then reflashing the Arduino with the new values. Boards running V2 (Arduino code version 2.0 or later) can be connected to a computer, and the calibrations can be read and updated via a web interface.

The signals that will benefit most from calibration are speed, motor RPM and temperature, followed by voltages, and then current.

## Choose your calibration path

- **V2 (Arduino code version 2.0 or later):** use the web interface at `configure.echook.uk`.
- **Legacy (Arduino code below version 2.0):** update values in `calibration.h`, then reflash the Arduino.

### Calibration Web Interface

The calibration web interface is available at [configure.echook.uk](https://configure.echook.uk). Please note it requires either Chrome or Edge desktop browsers. There is no mobile browser support.

Use the web interface in this order:

1. Unplug the Bluetooth module (unless you have an Arduino Nano Every) and connect your eChook to your computer.
2. Navigate to the [configuration webapp](https://configure.echook.uk) and click connect.
3. In the browser menu, select the eChook's COM port from the list and press connect.
4. After a few seconds, the screen below should open.

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

5. Enter the new number in the corresponding box. Any changes are highlighted, and the bottom-right button will reflect how many changes you have entered from the configuration saved on the eChook.
6. To save the changes to the eChook, press the bottom-right button. These will be reflected immediately in the values being read out on screen.
7. Once you have a configuration you are happy with, it is recommended to take a backup using the 'Backup Config' button. Keep this somewhere safe.

The next few pages describe the legacy `calibration.h` workflow. For V2 (Arduino code version 2.0 or later), enter the numbers into the web app instead.

### Issues?

If you hit any issues, please feed back on the forum, or via email to info@echook.uk.

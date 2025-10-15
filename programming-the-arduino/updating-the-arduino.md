# Updating the Arduino

If you are just setting up your eChook for the first time, skip this page.

Over time, there will be updates to the eChook Arduino code, and new releases will be show on the eChook github page here:&#x20;

{% embed url="https://github.com/eChook/eChook-Arduino-Nano/releases/" %}

To update your eChook to a new release, download the zip file from the link above, extract it, open it in the Arduino IDE and follow the steps on the last page to upload it to the Arduino.

### Updates and Calibrations

Between code version 1.x and 2+ there has been a change in how calibrations are stored on the Arduino. In v1.x, the calibration was hard coded into the calibration.h file, and values from this file need to be manually copied across to the newly downloaded release before uploading it.

From v2.0 onwards, the calibrations are stored in a separate memory location (EEPROM) on the Arduino, and are changed via the web interface at [configure.echook.uk](https://configure.echook.uk). This means that the calibrations are maintained on the Arduino and aren't affected by reprogramming.

**Updating from V1.x > V2+**

This is the most involved update. The recommended route is to keep a copy of your old calibration.h file, upload the new V2 release to the Arduino without changing any values in code, then proceed to the [configuration website](https://configure.echook.uk) and enter your previous calibrations through the new interface.

**Updating from V2+ to V2++**

Just download the new release and flash it - your calibrations will remain on the Arduino.&#x20;


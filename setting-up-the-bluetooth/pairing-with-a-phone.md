# Pairing with a phone

#### Install the App

Install the ‘[eChook Companion](https://play.google.com/store/apps/details?id=com.ben.drivenbluetooth)’ app from the Google Play Store. 

The app requires two permissions and won't work properly unless they're allowed at first start up. Access to device media storage is required to save a log file to the phone, and access to Location is required for lap counting, logging GPS speed, and with the in-house telemetry, displaying car location on track.

#### Power up the eChook

Power up the eChook with the bluetooth module plugged in. The LED on the bluetooth module should be flashing rapidly, indicating it is disconnected from a phone.

#### Connect the two

On the phone, go to bluetooth settings and scan for devices. It may take a while to resolve the name, but the name set in the Calibration.h file should appear. Pair with it using the “1234” passcode.

Open the eChook app and go to settings. Touch 'Select Bluetooth Device' and select your newly paired device from the list.

Back in the main app screen, press the blue bluetooth connect button in the bottom left corner. It should start displaying information from the board. At this point, the only data will be the supply voltage.

{% hint style="warning" %}
If the app can’t connect it will try to reconnect regularly. This will happen if the BT module has lost power, but it **will also happen if the data being sent from the eChook stops**, therefore if the Arduino isn’t programmed properly and isn't regularly sending out data, the bluetooth will appear to fail to connect.
{% endhint %}

Further instructions on using the app are in the 'Using the eChook Companion App' section.

{% page-ref page="../using-the-app/" %}


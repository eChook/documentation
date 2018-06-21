# Pairing with a phone

Any phone running Android 5 or above should work with the app.

Power up the eChook board with the bluetooth module plugged in. The LED on the bluetooth module should be flashing rapidly, indicating it is disconnected from a phone.

On the phone, go to bluetooth settings and scan for devices. It may take a while to resolve the name, but the name set in the Configuration.h file should appear. Pair with it using the “1234” passcode.

Now install the ‘[eChook Companion](https://play.google.com/store/apps/details?id=com.ben.drivenbluetooth)’ app from the google play store.

Open the app and go to settings. Find bluetooth device name and enter the name of the BT module.Back in the main app screen, press the blue bluetooth connect button. It should start displaying information from the board. At this point, the only data will be the supply voltage.

If the app can’t connect it will try to reconnect regularly. This will happen if the BT module has lost power, but it will also happen if the data being sent from the eChook stops, therefore if the Arduino isn’t programmed properly, the bluetooth will appear to fail to connect.

Further instructions on using the app are in the 'Using the eChook Companion App' section.


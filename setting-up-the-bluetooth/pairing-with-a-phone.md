# Pairing with a phone

#### Install the App

Install the [Omni Telemetry](https://play.google.com/store/apps/details?id=net.keduro.omni\&hl=en_GB) app from the Google Play Store.

The app requires two permissions and won't work properly unless they're allowed at first start up. Access to device media storage is required to save a log file to the phone, and access to Location is required for lap counting, logging GPS speed, and with the in-house telemetry, displaying car location on track.

#### Power up the eChook

Power up the eChook with the Bluetooth module plugged in. The LED on the bluetooth module should be flashing rapidly, indicating it is disconnected from a phone.

#### Connect the two

On the phone, go to Bluetooth settings and scan for devices. It may take a while to resolve the name, but the configured eChook name should appear. If needed, set or check this name using the [Calibrating the eChook](../calibrating-the-echook/) section. It is recommended to change from the default name, as there may be multiple 'eChook' Bluetooth devices at a race day! Pair with it using the "1234" passcode.

Open Omni Telemetry, then open the three-dot menu in the top-right corner and select Settings. Choose your newly paired eChook device from the Bluetooth device list.

On exiting settings, the app will attempt to connect to the eChook board and the Bluetooth icon in the top right should turn green. At this point, the only data will be the supply voltage.

{% hint style="warning" %}
If the app can’t connect, the Bluetooth icon will be red, and  it will try to reconnect regularly. This will happen if the BT module has lost power, but it **will also happen if the data being sent from the eChook stops**. If the Arduino isn’t programmed properly and is not regularly sending out data, the Bluetooth link can appear to fail to connect.
{% endhint %}

Further instructions on using the app are in the "Using the App" section.

{% page-ref page="../using-the-app/" %}


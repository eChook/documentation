# Bluetooth

{% hint style="danger" %}
**We are aware that a number of V2.0 kits were supplied with an incompatible Bluetooth module! See the steps in the 'No Data being sent to app' section below to determine if your kit is affected, and for next steps if it is.**
{% endhint %}

## Pairing

If the Bluetooth module is not appearing as the name you have configured when you attempt to pair it to your phone, and it is showing up as 'HC-05' or similar instead, the configuration of the HC-05 Bluetooth module has failed.

See [setting-up-the-bluetooth](../setting-up-the-bluetooth/ "mention") for more information on configuring the module.

## No Data being sent to app

This section assumes the module is paired and connected to your phone, you select the Bluetooth device in the Omni app, and no data appears.

**Does the Omni App crash?** If so, this is the first indicator of an incompatible Bluetooth module.

#### Check if data is being transmitted

To do this, install a Bluetooth Serial Terminal app, such as [Bluetooth Serial Terminal by Kai Morich](https://play.google.com/store/apps/details?id=de.kai_morich.serial_bluetooth_terminal\&hl=en-US).

Open the app. In settings, change the display mode to HEX, then in the devices menu, select the Bluetooth module. There are two tabs in the devices menu, one for 'Bluetooth Classic' devices and one for 'Bluetooth LE'. Your eChook board should appear in the Bluetooth Classic tab.

&#x20;_If it appears in the Bluetooth LE tab you have an incompatible Bluetooth module. go to the Incompatible Module section below._

If your module appeared in the Bluetooth Classic tab, tap it to connect to it. If data is being transmitted you will see something like this:

<figure><img src="../.gitbook/assets/Screenshot_20250514-085552~2.png" alt="" width="188"><figcaption><p>HEX Data being received </p></figcaption></figure>

**If you see data as above:**&#x20;

If you are running unmodified eChook Arduino code, the eChook board is working as it should, the issue is app related. Double check the correct Bluetooth device is selected in the Omni app. If that doesn't change it, try reinstalling the app. \
If you have modified the eChook Arduino code, re-flash the latest release from github.

If neither of these fixes your issue, contact us for further help.

**If you don't see data as above:**

The Arduino is not sending data out. Re-flash the latest Arduino code release from github and try again. If the issue persists, contact us for further help.

## Incompatible HC-05 Bluetooth Modules

As of late 2024, a new 'HC-05' compatible module has started being sold. It's being advertised as a standard HC-05 module, but is actually a Bluetooth Low Energy device. This uses a completely different wireless communication protocol than HC-05 modules and as such, is incompatible. Suppliers selling this module appear generally (and genuinely) unaware, and are still marketing it as a Bluetooth 2.0 device. These new Bluetooth Low Energy devices look very similar to the compatible HC-05 modules so easily slip under the radar.

Unfortunately the batch of HC-05 modules I bought for the V2.0 kits appears to have been a mix of good modules and Low Energy modules. The random ones I sampled before kitting were all good, and at the time I was not aware of the incompatible versions existing, but two teams (so far - 05/2025) have reported receiving incorrect modules.

If you have purchased an eChook Nano V2.0 kit from Greenpower and have verified that your module is a Bluetooth Low Energy device in the Bluetooth Serial app, as described above, email us at info@echook.uk with a screenshot showing the eChook appearing in the Bluetooth LE tab of the Bluetooth Serial App, a picture of the Bluetooth module, and an invoice of your original kit purchase.

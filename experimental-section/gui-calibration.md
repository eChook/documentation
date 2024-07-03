# GUI Calibration

There is a new code release for the Arduino: V2.0-alpha1.&#x20;

This is the first major code change for the eChook Nano GPT in years. The code has been completley restructured, breaking it down into individual files by function, but the major change is that the calibration variables are now stored in EEPROM (on board non-volatile memory) rather than being hard coded in the calibration.h file.

This also comes hand in hand with a new web page that connects to your eChook either over USB or Bluetooth (No mobile support, desktop/laptop only).

This is an alpha pre-release. It may be a bit buggy, but the more people who try it, the quicker those bugs will be found and fixed! If you do find a bug please report it here: [https://github.com/eChook/eChook-Arduino-Nano/issues](https://github.com/eChook/eChook-Arduino-Nano/issues)

#### Flashing the new firmware:

Download the latest release from here:  (at the time of writing, v2.0-alpha1)

{% embed url="https://github.com/eChook/eChook-Arduino-Nano/releases" %}

Open this in the Arduino IDE and flash/upload it as per normal. Don't worry about copying your old calibrations over at this point - they will come in later.

#### Loading your calibration:

Head over to the shiny new calibration page here:

{% embed url="https://calibration.echook.uk" %}

{% hint style="info" %}
This web page uses the WebSerial API which has limited browser support. You can use either **Chrome, Edge or Opera**. No mobile browsers support WebSerial.
{% endhint %}

Now either connect your eChook via USB (bluetooth module needs to be **disconnected** for USB Serial communication to work), or pair your computer to the bluetooth module. Press the big connect button and a browser menu will appear for you to select the correct serial port.

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

The page should now display every measurement being taken by the eChook, updating live, along with the relevent calibration values. If you already have a calibration, enter the values from your old calibration.h file into the relevent text boxes - the interface will highlight any changes you've made - and click the 'Send x Changes' button in the bottom right. The readings will update to reflect the new calibrations within \~1 second.\
If this is the first time you're calibrating your eChook, refer to the '[Calibrating the eChook](../calibrating-the-echook/)' section of this document, but enter the calculated values on the web page.

I strongly recommend using the backup button once you've finished your initial setup, and keeping the downloaded file somewhere safe.

That's all there is to it! Please let us know how you get on, either with the web chat on this page, the forum or an email to info@echook.uk.



### Known Bugs

**Issue**: Sometimes when you press connect on the website, it loads but displays 'Not Calibratable' on each line.\
**Fix**: Refresh the page and connect again.\
**Cause**: Undetermined.

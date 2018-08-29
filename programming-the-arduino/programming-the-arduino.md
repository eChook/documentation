# Programming the Arduino

Locate and open the ‘eChookCode.ino’ file that was downloaded in the last step. This will open in the Arduino IDE with 'calibration.h' in another tab.

Before the code can be compiled, the IDE needs to know what Arduino the code is for. Go to Tools&gt;Board and select the Arduino Nano, then go to Tools&gt;Processor and select ATmega328. The bottom right of the Arduino IDE should now read “Arduino Nano, ATmega328”.

{% hint style="info" %}
As of Arduino IDE v1.8.2 the processor to select is "**ATmega328 \(Old Bootloader\)**". Not selecting this will result in AVRDude out of sync errors on uploading.
{% endhint %}

Now check that the code compiles. Click the ‘tick’ button on the top left of the Arduino IDE window. A progress bar will appear at the bottom of the window - this step will likely take a couple of minutes the first time. When done the message bar will read ‘Done Compiling’. If there was an error, the console below the message bar will show it. The most likely causes will be not having the bounce2 library added properly, or the wrong target Arduino being selected. If you have a problem at this point please get in touch or comment on the documentation here and we will resolve it.

Assuming the code compiled successfully, it can now be uploaded \(flashed\) to the Arduino. Before plugging the Arduino in, go to ‘Tools &gt; Port’ and take note of which COM ports are listed. Now connect the Arduino via the mini USB cable. The computer will assign it a COM port. Go back to ‘Tools &gt; Port’ and select the new COM port, which will be the Arduino.

{% hint style="info" %}
It is important to **disconnect** the bluetooth module from the eChook board before attempting to flash code. 
{% endhint %}

Press the ‘Upload’ button to compile and flash the code to the board. The TX and RX lights on the Arduino will flash rapidly while the upload is ongoing. When finished the Arduino IDE will show “Upload Complete” if it has all worked.

### Compilation Errors

It might not all work. If this happens the Arduino IDE will show compilation failed and some errors, generally red, in the log at the bottom of the window. Some errors are more helpful than others, but to make them as useful as possible, go into preferences and enable verbose logging:

![](../.gitbook/assets/image%20%287%29.png)

Now try the upload again - it will still fail, but should give more information on why. If you can't make sense of them yourself head over to the [support forum](http://echook.boards.net) and start a new thread with a copy of the errors - we'll give you a hand decrypting it.


# Programming the Arduino

Locate and open the ‘eChookCode.ino’ file that was downloaded in the last step. This will open in the Arduino IDE with 'calibration.h' in another tab.

Before the code can be compiled, the IDE needs to know what Arduino the code is for. Go to Tools>Board and select the Arduino Nano, then go to Tools>Processor and select ATmega328\*. The bottom right of the Arduino IDE should now read “Arduino Nano, ATmega328”.

Now check that the code compiles. Click the ‘tick’ button on the top left of the Arduino IDE window. A progress bar will appear at the bottom of the window - this step will likely take a couple of minutes the first time. When done the message bar will read ‘Done Compiling’. If you have a problem at this point take a look at the suggestions at the bottom of this page

Assuming the code compiled successfully, it can now be uploaded (flashed) to the Arduino. Before plugging the Arduino in, go to ‘Tools > Port’ and take note of which COM ports are listed. Now connect the Arduino via the mini USB cable. The computer will assign it a COM port. Go back to ‘Tools > Port’ and select the new COM port, which will be the Arduino.

{% hint style="info" %}
It is important to **disconnect** the Bluetooth module from the eChook board before attempting to flash code.&#x20;
{% endhint %}

Press the ‘Upload’ button to compile and flash the code to the board. The TX and RX lights on the Arduino will flash rapidly while the upload is ongoing. When finished the Arduino IDE will show “Upload Complete” if it has all worked.

## Upload Errors

It might not work first time. Don't panic!

### Common Errors

#### _Out Of Sync_

If an error occurs it will show up in the black console window at the bottom of the IDE. The most common error seen is an out of sync error, which will show something like the following:

```
avrdude: stk500_getsync(): not in sync: resp=0x00
avrdude: stk500_disable(): protocol error, expect=0x14, resp=0x51
```

There are two common causes for this:

1. The bluetooth module is plugged in at the same time as you are trying to program the Arduino. Unplug it and try again.
2. You have the wrong Arduino or wrong processor selected in the IDE.&#x20;
   1. Go to **Tools>Board>Arduino AVR Boards** and make sure the **Arduino Nano** is selected.&#x20;
   2. Go to **Tools>Processor** and make sure **ATmega328P** is selected. If the error still appears, try selecting the **ATmega328P (Old Bootloader)** instead.

#### _Access is denied_

A more recent error is 'Can't open Device' and will show something like the following:

```
avrdude: ser_open(): can't open device "\\.\COM3": Access is denied
```

This happens when the COM port is already open in another process. With Arduino IDE 2.x it seems that this other process is often the IDE itself. If you are seeing this error there doesn't seem to be one fix that works for everyone, but here are a few things to try:

1. Open Serial Monitor (Square button top right of the IDE), then close it again. This makes the IDE close the serial port if it has it open. Now try to upload the code again.
2. Unplug the Arduino, close the IDE, re-open the IDE, plug in the Arduino and hit upload the moment windows recognises it.
3. A little drastic, but try another computer! This generally works.

#### Any other Issues

If you are seeing other issues, or compilation errors rather than upload errors you'll have the errors listed in the console window. Some errors are more helpful than others, but to make them as useful as possible, go into preferences and enable verbose logging:

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Now try the upload again - it will still fail, but should give more information on why. Feel free to give google a try, but if you can't make sense of the log, use the chat feature on this page or head over to the [support forum](http://echook.boards.net) and start a new thread with a copy of the errors - we'll give you a hand deciphering it.


# Programming the Arduino

Locate and open the ‘eChookCode.ino’ file that was downloaded in the last step. This will open all files in the Arduino IDE.

Before the code can be compiled, the IDE needs to know what Arduino the code is for. Go to Tools>Board.

If you have an Arduino Nano (as provided in the kit), select Arduino AVR Boards > Arduino Nano, then go to Tools>Processor and select ATmega328\*. The bottom right of the Arduino IDE should now read “Arduino Nano, ATmega328”.

If you have an Arduino Nano Every, you need to go to 'Boards Manager' and search 'megaAVR', then install the megaAVR boards package. Now go to Tools>Boards>megaAVR Boards> Arduino Nano Every

Now check that the code compiles. Click the ‘tick’ button on the top left of the Arduino IDE window. A progress bar will appear at the bottom of the window - this step will likely take a couple of minutes the first time. When done the message bar will read ‘Done Compiling’. If you have a problem at this point take a look at the suggestions at the bottom of this page

Assuming the code compiled successfully, it can now be uploaded (flashed) to the Arduino. Before plugging the Arduino in, go to ‘Tools > Port’ and take note of which COM ports are listed. Now connect the Arduino via the mini USB cable. The computer will assign it a COM port. Go back to ‘Tools > Port’ and select the new COM port, which will be the Arduino.

{% hint style="info" %}
If you are using the older Arduino Nano Clone, it is important to **disconnect** the Bluetooth module from the eChook board before attempting to flash code. This isn't required for the Arduino Nano Every, it can be programmed with everything connected.
{% endhint %}

Press the ‘Upload’ button to compile and flash the code to the board. The TX and RX lights on the Arduino will flash rapidly while the upload is ongoing. When finished the Arduino IDE will show “Upload Complete” if it has all worked.

## Upload Errors

It might not work first time. Don't panic!

### Common Errors

#### _Out Of Sync_

If an error occurs it will show up in the Output window at the bottom of the IDE. The most common error seen is an out of sync error, which will show something like the following:

```
avrdude: stk500_getsync(): not in sync: resp=0x00
avrdude: stk500_disable(): protocol error, expect=0x14, resp=0x51
```

There are some common causes for this:

1. The bluetooth module is plugged in at the same time as you are trying to program the Arduino . Unplug it and try again. (Arduino Nano Clone **only**)
2. The wrong COM port is selected - does the port disappear from the Tools>Port menu when you unplug the Arduino?
3. You have the wrong Arduino or wrong processor selected in the IDE.&#x20;
   1. Ensure the correct Arduino is selected.&#x20;
   2. If using a Arduino Nano Clone go to **Tools>Processor** and make sure **ATmega328P** is selected. If the error still appears, try selecting the **ATmega328P (Old Bootloader)** instead.
4. You have the wrong version of the CH340 driver installed. Check the driver date and version in device manager matches below. If not, go back to the [driver install page](arduino-ch340-drivers.md) for the correct link.

<figure><img src="../.gitbook/assets/image (1).png" alt="" width="375"><figcaption></figcaption></figure>

#### _Access is denied_

A more recent common error is 'Can't open Device' and will show something like the following:

```
avrdude: ser_open(): can't open device "\\.\COM3": Access is denied
```

This happens when the COM port is already open in another process. With Arduino IDE 2.x it seems that this other process is often the IDE itself. If you are seeing this error there doesn't seem to be one fix that works for everyone, but here are a few things to try:

1. Open Serial Monitor (Square button top right of the IDE), then close it again. This makes the IDE close the serial port if it has it open. Now try to upload the code again.
2. Unplug the Arduino, close the IDE, re-open the IDE, plug in the Arduino and hit upload the moment windows recognises it.
3. Check the driver version - as in point 4 of the out of sync error section above.
4. A little drastic, but try another computer! This generally works.

**Oct 2024 Update:** Windows 11 now appears to re-write the CH340G drivers for the Nano Clone boards on start-up, requiring an uninstall and reinstall of the correct drivers each boot. All new kits come with an Arduino Nano Every and will not encounter this issue, but it is certainly annoying for teams with the older Arduino. Any eChook Nano board will work with the newer Arduino Nano Every.

#### Any other Issues

If you are seeing other issues, or compilation errors rather than upload errors you'll have the errors listed in the console window. Some errors are more helpful than others, but to make them as useful as possible, go into preferences and enable verbose logging:

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Now try the upload again - it will still fail, but should give more information on why. Feel free to give google a try, but if you can't make sense of the log, use the chat feature on this page or head over to the [support forum](http://echook.boards.net) and start a new thread with a copy of the errors - we'll give you a hand deciphering it.


# Programming the Arduino

Locate and open the ‘eChookCode.ino’ file. This will open in the Arduino IDE.

Before the code can be compiled, the IDE needs to know what Arduino the code is for. Go to Tools&gt;Board and select the Arduino Nano, then go to Tools&gt;Processor and select ATmega328. The bottom right of the Arduino IDE should now read “Arduino Nano, ATmega328”.

Now check that the code compiles. Click the ‘tick’ button on the top left of the Arduino IDE window. A progress bar will appear at the bottom of the window - this step will likely take a couple of minutes the first time. When done the message bar will read ‘Done Compiling’. If there was an error, the console below the message bar will show it. The most likely causes will be not having the bounce2 library added properly, or the wrong target Arduino being selected. If you have a problem at this point please get in touch or comment on the documentation here and we will resolve it.

Assuming the code compiled successfully, it can now be uploaded \(flashed\) to the Arduino. Before plugging the Arduino in, go to ‘Tools &gt; Port’ and take note of which COM ports are listed. Now connect the Arduino via the mini USB cable. The computer will assign it a COM port. Go back to ‘Tools &gt; Port’ and select the new COM port, which will be the Arduino.

It is important to disconnect the bluetooth module from the eChook board before attempting to flash code. Press the ‘Upload’ button to compile and flash the code to the board. The TX and RX lights on the Arduino will flash rapidly while the upload is ongoing. When finished the Arduino IDE will show “Upload Complete”.


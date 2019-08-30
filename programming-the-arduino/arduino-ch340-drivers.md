# Arduino CH340 Drivers

The Arduino IDE software installs the drivers for genuine Arduinos. A genuine Arduino Nano will cost in the region of £15, the clone Arduino Nano's included with the eChook kit can be had for around £1.50, so it was an easy choice!

The disadvantage is that they require different drivers. These are for the CH340 Serial to USB interface chip they use instead of the more expensive FTDI chip on genuine arduinos. This page links to drivers for different operating systems. It is required to install the relevant driver before continuing. Once installed the clone Arduino will behave exactly as a genuine one.

## Windows

Windows drivers can be installed from [here](http://www.wch.cn/download/CH341SER_EXE.html) or [here](https://drive.google.com/open?id=0B8NB2ERSryMSdlQxNFpPM1BGenc). Go through the beautifully chenglish install process.

## Mac

Drivers for mac are slightly more difficult. You can either disable KEXT security \(which is not advisable\) and get a free driver or you can get a signed driver from [here](https://www.mac-usb-serial.com/) - they do however cost money.

## Linux

CH340 drivers are baked in, just plug and play.


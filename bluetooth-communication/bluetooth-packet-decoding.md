## Decoding the Bluetooth Packets

If the output to the bluetooth module is viewed on the computer it is not human readable - the packets need to be decoded. Instead you will see similar to below:![](https://lh6.googleusercontent.com/I2sMeDueTuUThXxbOMM2WJRbVZcitf5ixVKBwcTFVNBEBjfYEplq_lqGAyZ6SL6bjpJsDJ8julGr-rbbjAfqIpjnOa5CQIJCQ1Q4daYPHTr_Vc2RGQJsHeiYkN0WfttuthohwvaY)



If you want to view the output on a computer there is a python script to do that at [https://github.com/eChook/Python-Serial-Interpreter](https://github.com/eChook/Python-Serial-Interpreter). This requires Python 3.x with pySerial and tkinter modules installed.

The interpretation code used in the Android app is available [here](https://github.com/eChook/eChook-Android/blob/master/app/src/main/java/com/ben/drivenbluetooth/threads/BTStreamReader.java).


### **Continuous Disconnecting and Reconnecting**

If the eChook Companion app connects the the module but gets no data through, it will continuously disconnect and reconnect in an effort to correct the problem. If this is occurring there is an issue with the data rather than with the bluetooth itself.

* Check that the Tx light on the arduino is flashing periodically \(should be a flash every 0.25 seconds\). This indicates that the Arduino is sending data out.

* Check that the baud rate of the Arduino and the HC-05 bluetooth module match. If the HC-05 has been auto configured by the Arduino, they will be the same. For the auto configuration procedure, see [here](https://docs.echook.uk/configuring-the-bluetooth-module/configuring-the-bluetooth-module.html).




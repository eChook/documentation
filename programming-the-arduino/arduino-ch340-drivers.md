# Arduino CH340 Drivers

The Arduino Compatible Nano included in the kit\* requires a driver to be installed that isn't installed by the Arduino IDE.



Sparkfun have written an excellent installation guide here:

{% embed url="https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all" %}

Once drivers are installed continue to the next page.



{% hint style="info" %}
Note that as of Q2 2023 some teams have been experiencing an error "`avrdude: ser_open(): can't set com-state for "\.\COMx`" when trying to program the Arduino on Windows 10+ computers. This roughly corresponds with a new version of the drivers being released - if you experience this please try installing an older version of the drivers from the link below.

We're still trying to determine a definitive fix for the issue, so if you are having issues or find a solution let us know with the message button on the bottom right of the page :)
{% endhint %}

{% embed url="https://drive.google.com/file/d/1ioG8mri-eTHbXVdG_pV-I54ftH8aERBr/view?usp=sharing" %}

\* During the chip shortage in 2022 some kits were supplied with Genuine Arduino Nano Every boards - if you have one of these kits you can skip this step, the drivers were installed with the Arduino IDE.


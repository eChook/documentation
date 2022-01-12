# Build Steps Photos

Here is a sequence of photos showing the building up of a v1.3 eChook board.&#x20;

As a general rule it is easier to solder components that protrude least from the board first and work your way up. This is because when you place the component in the board and turn it upside down to solder it, the board rests against the tallest component, holding it in place.

### Soldering

If you are new to soldering it may be worth looking for some guides online before starting. Here is a good (possibly slightly over the top detailed) soldering tutorial from EEVBlog that could be worth a watch:&#x20;

{% embed url="https://www.youtube.com/watch?v=fYz5nIHH0iY" %}

### Interactive Build Viewer

{% embed url="https://echook.github.io/eChook-Nano-PCB/v1.3.1/ibom.html" %}
Click to open&#x20;
{% endembed %}

The Interactive BOM linked above is a very useful aid for building the board linking components to their location on the board. Use it in conjunction with the steps below which show a recommended build order and point out any components that need to be placed with a specific orientation.

### Build Steps

![PCB and all components laid out](<../.gitbook/assets/image (4).png>)

Start with the resistors - these are the smallest components.

{% hint style="info" %}
If the resistors aren't labelled, use the[ resistor colour codes](http://www.instructables.com/id/How-to-read-color-codes-from-resistors-1/) or a multimeter to determine their values
{% endhint %}



![All resistors soldered in place](<../.gitbook/assets/image (3).png>)

* Ceramic Capacitors and the Diode next

{% hint style="info" %}
Ceramic Capacitors (1μF) - these have 105 printed on them. The first two digits indicate the value, the third digit is the number of zeros following that value, to give the capacitance in pico Farads.

105 translates to $$10 \times10^5$$ pF or 1,000,000pF, 1000 nF or finally, 1μF
{% endhint %}

{% hint style="danger" %}
**Diode** - The grey end of the diode goes to the end pointed to by the ‘arrow’ diode symbol on the silkscreen.
{% endhint %}

![Diode and 1µF capacitors in place ](<../.gitbook/assets/image (8).png>)

* Transistor: This looks similar to the hall effect sensors but is larger and has 'BC547' printed on it.  There will be a few mm of leg between the transistor and the PCB. &#x20;
* LED: The LED is labelled as PWM on the board as this is the signal it shows by default.

{% hint style="danger" %}
Both the **LED** and **transistor** need to be placed in the correct orientation - the 'D' shape of the component matches the outline on the board.
{% endhint %}

![Transistor and LED added](<../.gitbook/assets/image (9).png>)

* Tracopower Voltage Regulator

{% hint style="danger" %}
**Voltage Regulator** is orientation specific.  The dot on the printed face lines up with the square solder point, with the printed face to the outside edge of the PCB
{% endhint %}

* Electrolytic Capacitor (22μF)

{% hint style="danger" %}
**Electrolytic Capacitors** are orientation specific. The -ve leg is marked with a grey stripe on the capacitors body and hollow '-' symbols. The PCB indicates which side the +ve leg is with a '+' sign.
{% endhint %}

* Header Socket for the Arduino and Bluetooth Module
* 8 pin DIP Socket for the Op-Amp

{% hint style="danger" %}
The **DIP Socket** is orientation specific.  There is an indentation on the silk screen image, this lines up with the indentation on the socket.
{% endhint %}

{% hint style="info" %}
For larger components with 3+ pins it can be helpful to solder one pin in first then make sure that the component is flat with the PCB. To adjust it, simply melt the solder on the single pin and move the component until you are happy. Now solder the remaining pins.
{% endhint %}

![DCDC regulator, 22uF Capacitor, Header and DIP Socket added.](<../.gitbook/assets/image (2).png>)

* Polyfuse
* Connectors

![Polyfuse and Connectors added.](<../.gitbook/assets/image (5).png>)

\
All soldering on the PCB is now done.&#x20;

{% hint style="warning" %}
**Complete the power on tests** described on the next page **before** plugging in the Arduino, Bluetooth Module and Op-Amp as shown below.
{% endhint %}

{% hint style="danger" %}
When connecting the Bluetooth module, ensure that it is plugged in the right way round using the silkscreen labels on the PCB and bluetooth module.
{% endhint %}

![](<../.gitbook/assets/image (6).png>)

The remaining components are fitted to the car itself, as described in the 'Connecting the eChook to the Car' section.

{% content-ref url="../connecting-the-echook-to-the-car/" %}
[connecting-the-echook-to-the-car](../connecting-the-echook-to-the-car/)
{% endcontent-ref %}


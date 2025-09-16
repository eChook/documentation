# Current Sensor

Current is probably the most useful data to have on a Greenpower car as it gives the best indication of how quickly the batteries are being discharged.

{% tabs %}
{% tab title="Kit V1.4 +" %}


From Kit version 1.4 a PCB breakout board for the current sensor is included to carry the LEM sensor, three capacitors, and a connection to the vehicle harness.

![](<../.gitbook/assets/image (8).png>)

From V2.0 onwards, a JST connector and wiring pigtails have been included as connections to the current sensor PCB.
{% endtab %}

{% tab title="Kit < V1.4" %}
The current sensor needs two 47nF capacitors and one 4.7nf capacitor soldered to it, as close to the pins as possible as shown in the[ datasheet](http://docs-europe.electrocomponents.com/webdocs/142e/0900766b8142e844.pdf) diagram below:

![](../.gitbook/assets/screenshot-from-2017-11-29-22-09-22.png)

Solder the wires and the capacitors directly to the current sensor pins. It is advisable to add some form of stress relief so that if the wires are pulled, the solder joints don't take the force. This can be achieved with some hot glue around the connections, cable ties (as shown below) or tape etc.
{% endtab %}
{% endtabs %}

### Connecting the sensor to the eChook board

The four outputs from the current sensor PCB, labelled 5V, GND, Ref and Sense (Out on early boards), match the labels of the four pins on the eChook board current sensor - although the pin order is different.

| Current Sensor | eChook board current connector |
| -------------- | ------------------------------ |
| +5v            | 5V                             |
| Ref            | Ref                            |
| Sense/Out      | Sens                           |
| GND            | GND                            |

If possible, avoid a long harness between the eChook board and the sensor to limit interference on the current signal.

### Positioning the sensor in the car

This sensor needs to be placed around the main 24V cable from the battery. A convenient location is often next to the circuit breaker. The orientation of this sensor is important; if it is the wrong way around it will not read a current. The correct orientation is shown below - note the lip around the right hand side of the sensor aperture, and if you have a PCB mounted sensor, the mounting direction is printed on the bottom of the board.

![](../.gitbook/assets/screenshot-from-2017-11-29-22-10-26.png)




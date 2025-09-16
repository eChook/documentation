# Throttle Input

Throttle input is useful to log to see how the car is being driven, however due to the number of different ways throttles are implemented on cars there are a few methods of interfacing it to the eChook.

A throttle input is also needed for the apps lap counter feature, as this uses the throttle to determine race start.

Finally, the eChook will take a variable throttle and output a PWM signal that can be used as an input to a higher power motor driver circuit. The green LED on the eChook board is connected to this output.

## Throttle Configuration

There are two main ways that teams tend to use the throttle input with the eChook, depending on whether a separate motor control system is being used (be that simple relays or a more sophisticated controller such as a 4QD)

* Logger only - the motor control is handled by a different system and the eChook is just used to log the the throttle input
* Motor control (Fully Connected) - the PWM output of the eChook is used to control the motor, according to the throttle input and any processing on the eChook.

#### Logger only:

The eChook needs to share the same ground reference, normally battery negative, as the motor control system, and just the throttle signal should be fed into the eChook board

| Throttle                            | eChook Throttle Connenctor |
| ----------------------------------- | -------------------------- |
| Not Connected                       | 5V                         |
| Throttle Signal to Motor Controller | In                         |
| Not Connected - shared GND          | GND                        |

{% hint style="danger" %}
#### **If using a 4QD controller DO NOT connect the 4QD Ground to the eChook Ground.**&#x20;

The 4QD controllers have built in reverse polarity protection (unless you have an extreme version of a controller that specifically states it has no reverse polarity protection). The circuit they've used to achieve this creates a small voltage offset between the 4QD ground and the chassis/eChook ground. If the two are connected and the motor is run, significant current will attempt to flow through the connecting wire, potentially melting it, and likely causing damage to the eChook board.
{% endhint %}



#### Fully Connected

The eChook provides 5V power and the ground reference as well as reading the throttle output

| Throttle               | eChook Throttle Connector |
| ---------------------- | ------------------------- |
| 5V Power (If required) | 5V                        |
| Output Signal          | In                        |
| GND                    | GND                       |

These tables apply to each different type of throttle described below

### Throttle Types

As well as different ways of connecting the throttle, there are multiple common types of throttle used in Greenpower racing, and the connections are different for each:

{% tabs %}
{% tab title="5V Variable Throttle" %}
This is the input that the eChook board is designed for and is the commonly used eBike or eScooter hall effect throttle, or any potentiometer based throttle and if a variable throttle input is used, it is likely that it already works in this voltage range, however confirm this with a multimeter before attaching anything.&#x20;

This type of throttle can be connected directly to the eChook as per the tables above, depending on whether the eChook is acting as a logger only, or for motor control.
{% endtab %}

{% tab title="Push Button Throttle" %}
There are a few configurations of pushbutton throttle. For a car running a relay for motor control the throttle button will likely be switching 24v, or in some cases 12v. In this case, the throttle voltage is above the 5V expected by the eChook.

*   V1.x Boards need a potential divider circuit to reduce the voltage from the button to a safe 5V for the eChook using a potential divider circuit between the button and the throttle connection:&#x20;

    ![](https://lh5.googleusercontent.com/KW_L3b9ZulcJHl2DW7X59uPfOaAb0Wx-hhOOY05LV8JsQ-45gsAX87I-p3_iwrGjc9t9DdA0AJs7RcMXF0zFeOA8yvB3myBPQoFCtgvISXY-wqJguEm9DNX9WkTusLDgDmWt9u7F)

    \
    For a button switching a 24v signal, set R1=82k and R2 = 16k. This drops 30V to 5V and is intended to protect against the batteries having higher voltages than 12V each.\
    Resistor values for other voltages can be calculated by the formula below, where V\_out is the feed to the eChook board, and V\_in is the output from the throttle button.

$$
V_{out } = V_{in} *( R_2/{R_1+R_2})
$$

* V2.x Boards have overvoltage protection circuitry built into the board, so a voltage of up to 30v can be connected to the board through a single inline resistor to limit the current. The recommended resistor value is above 1kOhm, and below 10kOhm inclusive.

#### eChook Configuration

To tell the eChook that it is connected to a pushbutton throttle, connect it to the calibration web interface, as described in the calibration section of this document, and select Throttle Tyle: On/Off.
{% endtab %}

{% tab title=">5V Variable Throttle" %}
If the car has a variable throttle with an output that goes over 5V, a potential divider is needed to reduce the maximum output voltage to 5v. See the Push Button Throttle tab for the potential divider design, then connect the Throttle and ground connections as per tables above.
{% endtab %}
{% endtabs %}




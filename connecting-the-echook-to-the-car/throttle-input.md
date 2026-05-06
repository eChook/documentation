# Throttle Input

Throttle input is useful to log because it shows how the car is being driven. Since throttle systems vary between cars, there are several safe ways to interface throttle signals to the eChook.

Throttle input is also needed for the app lap counter feature, because this uses throttle signal to detect race start.

The eChook can also take a variable throttle input and generate a PWM output for a higher-power motor driver circuit. The green LED on the eChook board is connected to this output.


## Throttle Configuration

There are two common ways to use throttle input with the eChook, depending on whether a separate motor control system is used (from simple relays to a controller such as a 4QD).

* Logger only - motor control is handled by another system and the eChook only logs the throttle input.
* Motor control - eChook PWM output is used to control the motor based on throttle input and any eChook processing.

#### Logger only

The eChook must share the same ground reference, normally battery negative, as the motor control system. Only the throttle signal is fed into the eChook board.

| Throttle                            | eChook Throttle Connector |
| ----------------------------------- | -------------------------- |
| Not Connected                       | 5V                         |
| Throttle Signal to Motor Controller | In                         |
| Not Connected - shared GND          | GND                        |

{% hint style="danger" %}
#### **If using a 4QD controller DO NOT connect the 4QD Ground to the eChook Ground.**&#x20;

4QD controllers have built-in reverse polarity protection (unless you have a variant that explicitly states it does not). This can create a small voltage offset between 4QD ground and chassis/eChook ground. If these grounds are connected and the motor runs, significant current may flow through the ground wire, potentially melting wiring and damaging the eChook board.
{% endhint %}



#### Fully connected

The eChook provides 5V power and ground reference while reading throttle output.

| Throttle               | eChook Throttle Connector |
| ---------------------- | ------------------------- |
| 5V Power (If required) | 5V                        |
| Output Signal          | In                        |
| GND                    | GND                       |

These tables apply to each throttle type described below.

### Throttle Types

As well as different connection methods, there are multiple throttle types used in Greenpower racing, and each has different wiring requirements:

{% tabs %}
{% tab title="5V Variable Throttle" %}
This is the input type the eChook is designed for. It is common on eBike/eScooter hall-effect throttles and potentiometer-based throttles. Most variable throttles are already in this voltage range, but confirm with a multimeter before connecting anything.

This type of throttle can be connected directly to the eChook as per the tables above, depending on whether the eChook is acting as a logger only, or for motor control.
{% endtab %}

{% tab title="Push Button Throttle" %}
There are a few push-button throttle configurations. On cars using relay-based motor control, the button often switches 24V, and sometimes 12V. This is above the 5V range expected by the eChook input.

*   `V1.x` boards need a potential divider to reduce button voltage to a safe 5V at the eChook input:

    ![](https://lh5.googleusercontent.com/KW_L3b9ZulcJHl2DW7X59uPfOaAb0Wx-hhOOY05LV8JsQ-45gsAX87I-p3_iwrGjc9t9DdA0AJs7RcMXF0zFeOA8yvB3myBPQoFCtgvISXY-wqJguEm9DNX9WkTusLDgDmWt9u7F)

    \
    For a button switching a 24V signal, set `R1 = 82k` and `R2 = 16k`. This drops 30V to 5V and provides margin for battery voltages above 12V per battery.\
    Resistor values for other voltages can be calculated by the formula below, where V\_out is the feed to the eChook board, and V\_in is the output from the throttle button.

$$
V_{out } = V_{in} *( R_2/{R_1+R_2})
$$

* `V2+` boards include overvoltage input protection, so up to 30V can be connected through a single inline resistor to limit current. Recommended resistor value is `1kOhm` to `10kOhm` inclusive.

#### eChook Configuration

To configure eChook for a push-button throttle, connect to the calibration web interface and select `Throttle Type: On/Off`.
{% endtab %}

{% tab title=">5V Variable Throttle" %}
If the car has a variable throttle that can exceed 5V, use a potential divider to reduce the maximum output to 5V. See the Push Button Throttle tab for divider design, then wire throttle and ground as shown in the tables above.
{% endtab %}
{% endtabs %}




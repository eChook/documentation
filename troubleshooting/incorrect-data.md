# Incorrect Data

## Slightly wrong values being shown&#x20;

If the values move as expected, but are a little off, they likely need some calibration.

{% content-ref url="../calibrating-the-echook/" %}
[calibrating-the-echook](../calibrating-the-echook/)
{% endcontent-ref %}

## Very wrong values being shown

If there are obviously wrong values being reported by the phone, i.e. voltages when the batteries aren't plugged in, or high current when the motor is off the most likely cause is a wrong resistor in the circuit for that sensor. Use a multimeter and compare the values to those on the schematics [here](../circuit-schematics/).

If the value is far higher than anything you'd expect, it's best to power off the board quickly as an incorrect circuit could be sending more voltage to the Arduino than it is designed for with potential to cause damage.


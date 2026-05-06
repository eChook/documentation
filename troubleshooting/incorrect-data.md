# Incorrect Data

## Slightly wrong values being shown&#x20;

If values move as expected but are slightly off, they likely need calibration.

{% content-ref url="../calibrating-the-echook/" %}
[calibrating-the-echook](../calibrating-the-echook/)
{% endcontent-ref %}

## Very wrong values being shown

If obviously wrong values are being reported in the app (for example, voltage when the batteries are not plugged in, or high current when the motor is off), the most likely cause is an incorrect resistor value in the circuit for that sensor. Use a multimeter and compare the resistor values to the schematics [here](../circuit-schematics/).

If a value is far higher than expected, power off the board quickly. An incorrect circuit could be sending more voltage to the Arduino than it is designed for, with potential to cause damage.

These issues are unlikely on the V2 pre-assembled boards.

If you need help identifying the fault, contact us on the forum or webchat.


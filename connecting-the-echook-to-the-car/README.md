# Connecting the eChook to the Car

Now that the board is sending data to the phone, it needs to have some useful data to send. All of the external connections to the board go through pluggable terminal connectors. This makes it easy to wire into the vehicle’s harness with the screw terminals, and makes the board easy to remove from the car if necessary.

{% hint style="info" %}
There is a post with some guidance to building a Greenpower car wiring harness on the eChook forum [here](http://echook.boards.net/thread/26).
{% endhint %}

The image below shows the external interfaces to the board numbered, with details on each connection in the table.&#x20;

![eChook nano v1.3.1 Board Bottom View with connector pinouts](<../.gitbook/assets/image (10).png>)

{% hint style="info" %}
&#x20;Label the connectors on the harness side to make it easier to identify them in future.
{% endhint %}

## Connector Pin Out

<table data-header-hidden><thead><tr><th>Connector</th><th data-type="number">Pin</th><th>Signal</th><th>Use</th></tr></thead><tbody><tr><td>Connector</td><td>null</td><td>Signal</td><td>Use</td></tr><tr><td>Power In</td><td>1</td><td>24v</td><td>Power and 24V monitoring</td></tr><tr><td></td><td>2</td><td>12v</td><td>Monitoring the lower battery voltage. </td></tr><tr><td></td><td>3</td><td>Ground</td><td>Main grounding point for the board.</td></tr><tr><td>Motor PWM</td><td>1</td><td>5V PWM Output</td><td>A PWM output. Could control the drive motor, or a fan etc.</td></tr><tr><td></td><td>2</td><td>Ground reference</td><td>Ground for PWM line</td></tr><tr><td>Therm</td><td>1</td><td>5v Supply</td><td>5V supply for the Hall Effect Sensors</td></tr><tr><td></td><td>2</td><td>Motor RPM </td><td>Pulsed 5v signal from motor hall effect sensor</td></tr><tr><td></td><td>3</td><td>Wheel RPM</td><td>Pulsed 5v signal from wheel hall effect sensor</td></tr><tr><td></td><td>4</td><td>Ground reference</td><td>Ground for Hall Effect Sensors</td></tr><tr><td>Therm</td><td>1</td><td>Temp 1 - Line to thermistor</td><td>Connection to thermistor 1. Thermistor connects between here and ground</td></tr><tr><td></td><td>2</td><td>Temp 2 - Line to thermistor</td><td>Connection to thermistor 2. Thermistor connects between here and ground</td></tr><tr><td></td><td>3</td><td>Ground reference</td><td>Ground connection for thermistors</td></tr><tr><td>Throttle</td><td>1</td><td>5v Supply</td><td>5v supply for the throttle</td></tr><tr><td></td><td>2</td><td>0-5v throttle input</td><td>Analogue input for a variable throttle, or digital for a push button.</td></tr><tr><td></td><td>3</td><td>Ground reference</td><td>Ground reference for throttle</td></tr><tr><td>Ext Buttons</td><td>1</td><td>Ground reference</td><td>Ground reference for buttons</td></tr><tr><td></td><td>2</td><td>Brake Switch</td><td>Brake input for logging brake use</td></tr><tr><td></td><td>3</td><td>Button 1 Active LOW digital Input</td><td>Input for 'Race Start' button needed for lap counting</td></tr><tr><td></td><td>4</td><td>Button 2 Active LOW digital Input</td><td>Input for 'Switch Screen' button.</td></tr><tr><td>Current</td><td>1</td><td>5v Supply</td><td>5V to current sensor</td></tr><tr><td></td><td>2</td><td>Current Reference Analogue input</td><td>Input from current sensor reference pin</td></tr><tr><td></td><td>3</td><td>Current Sensing Analogue input</td><td>Input from Current Sense pin</td></tr><tr><td></td><td>4</td><td>Ground reference</td><td>Ground reference for current sensor</td></tr></tbody></table>

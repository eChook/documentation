# Bluetooth Communication

#### Bluetooth Hardware

The HC-05 bluetooth module takes a serial \(USART\) input and transmits any incoming data to a paired phone. This is compatible with any microcontroller with a hardware \(or emulated\) serial port. On Arduinos, this is accessed by using 'Serial' in your code.

The HC-05 modules are cheap to buy - generally under £5.

#### Communication Schema

Sending data over bluetooth takes time and power. To minimise these on the eChook a very compact packeting system was used. Each sensor update is sent in a packet of data 5 bytes long. Each byte looks like this:

`[{][id][data_1][data_2][}]`

The \[ \] indicate each byte.

**{} - **These braces indicate the start and finish of a packet - this allows for basic error detection as the receiver knows to expect a '}' 4 bytes after the '{'. When that is detected, anything within is likely to be data.

**id - **This is the data identifier. It is a single character that can be looked up in a table to identify what sensor the data in the packet is from.

**data 1 and 2 - **These two bytes contain the value from the sensor.

#### Encoding the data

Encoding the data into 2 bytes required limiting the data that is sent. To achieve this any value below 127 is sent to an accuracy of 2 decimal points, and any value above 127 is sent as an integer.

If the value being sent is below 127 the **data1 **byte contains the integer portion of the value and the **data2 **value contains two decimal points. If the value is over 127 the **data1 **byte contains the hundreds and thousands portion and the **data2 **value contains the tens and units.




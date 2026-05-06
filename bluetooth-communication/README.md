# Bluetooth Communication

## Bluetooth Hardware

The HC-05 Bluetooth module takes a serial \(USART\) input and transmits any incoming data to a paired phone. This is compatible with any microcontroller with a hardware \(or emulated\) serial port. On Arduinos, this is accessed using `Serial` in your code.

The HC-05 modules are cheap to buy - generally under £5.

## Communication Schema

Sending data over Bluetooth takes time and power. To minimize both on the eChook, a very compact packet system is used. Each sensor update is sent in a packet that is 5 bytes long:

`[{][id][data_1][data_2][}]`

The \[ \] indicate each byte.

**{} -** These braces indicate the start and end of a packet. This allows for basic error detection, because the receiver expects a `}` 4 bytes after `{`.

**id -** This is the data identifier. It is a single character that can be looked up in a table to identify what sensor the data in the packet is from.

**data 1 and 2 -** These two bytes contain the value from the sensor.

## Encoding the data

Encoding data into 2 bytes requires limiting how values are represented. Any value at 127 and below is sent to an accuracy of 2 decimal places, and any value above 127 is sent as an integer.

If the value being sent is 127 or below, the **data1** byte contains the integer portion of the value and **data2** contains the decimal portion to two decimal places. If the value is above 127, **data1** contains the hundreds and thousands portion and **data2** contains the tens and units.


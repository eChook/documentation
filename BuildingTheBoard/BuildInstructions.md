## Build Instructions

In it’s simplest form, building the board consists of soldering all components in their correct places, as shown below.

To make the process of soldering the board as easy as possible, it’s best to start with the smallest components first. All components sit on the top of the board, none on the bottom.

First solder all the resistors in place, being the smallest components. Follow this with the remaining small components on the board. A few of these are orientation specific:

* Diode - The grey end of the diode goes to the end pointed to by the ‘arrow’ diode symbol on the silkscreen.
* Electrolytic Capacitor \(22uF\) - This has a -ve and +ve leg. The marked -ve leg goes opposite the ‘+’ mark on the silkscreen. The other diodes can be soldered in any orientation.
* Transistor - the ‘D’ shape of the transistor lines up with the ‘D’ shape on the silkscreen.
* LED - The flat edge on the LED lines up with the flat edge on the silkscreen.
* Power Module - The dot on the pink face lines up with the square solder point.
* Op-Amp and socket - there is an indentation on the silk screen image, this lines up with the indentation on both the socket and chip.

The two 15 Pin strips of header are for the Arduino, and the 6 pin is for the Bluetooth Module. To solder these to the PCB, first solder one middle pin. This holds the strip in and you can ensure it is mounted straight by melting the solder on that one pin and adjusting if needed before soldering the rest of the pins in place. Repeat this procedure for the connectors around the outside of the board to allow easy positioning.

Don’t plug in the op-amp, arduino or bluetooth module quite yet.

High resolution photos of a finished board can be found [here](https://goo.gl/photos/QLNfrek9v2v522xa9).

### ** PCB Component Reference Table**

| **Ref Name** | **Description** | **Value / Type** |
| :--- | :--- | :--- |
| BT | 6 way Pin Header |   |
| C1 | Electrolytic Capacitor | 22uF |
| C3 | Ceramic Capacitor | 1u |
| C4 | Ceramic Capacitor | 1u |
| C5 | Ceramic Capacitor | 1u |
| Current | Pluggable Terminal 5.08mm 4pin | - |
| D1 | Diode Schottky 1A 40V DO41 | 1N5819RL |
| Expansion | - | - |
| Ext | Pluggable Terminal 5.08mm 4pin | - |
| FS1 | Polyfuse, 250mA | 250mA |
| MotorPWM | Pluggable Terminal 5.08mm 2pin | - |
| PowerIn | Pluggable Terminal 5.08mm 3pin | - |
| PWM | LED 5mm | - |
| Q1 | Transistor | BC547 |
| R1 | Resistor | 82K |
| R2 | Resistor | 16K |
| R3 | Resistor | 82K - originally 33K was used for early boards |
| R4 | Resistor | 16K |
| R5 | Resistor | 10K |
| R6 | Resistor | 1K |
| R7 | Resistor | 10K |
| R8 | Resistor | 1K |
| R9 | Resistor | 1K |
| R10 | Resistor | 1K |
| R11 | Resistor | 1K |
| R12 | Resistor | 1K |
| R13 | Resistor | 1K |
| R14 | Resistor | 1K |
| R15 | Resistor | 470R |
| R16 | Resistor | 1K |
| R17 | Resistor | 1K |
| R18 | Resistor | 1K |
| R19 | Resistor | 1K |
| R20 | Resistor | 4K7 |
| R21 | Resistor | 4K7 |
| R22 | Resistor | 10K |
| R23 | Resistor | 10K |
| R24 | Resistor | 47K |
| RPM | Pluggable Terminal 5.08mm 4pin | - |
| Therm | Pluggable Terminal 5.08mm 3pin | - |
| Throttle | Pluggable Terminal 5.08mm 3pin | - |
| U1 | Arduino Headers | - |
| U2 | Regulator,6.5-32Vin,5Vout 1A | TSR\_1-2450 |
| U3 | Dual BIFET Op Amp | MCP6002 |




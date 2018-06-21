# Build Instructions

In its simplest form, building the board consists of soldering all components in their correct places, as shown in the table below.

To make the process of soldering the board as easy as possible, it’s best to start with the smallest components first. All components sit on the top of the board, none on the bottom.

This is a suggested order for soldering the components. Lines in **bold** mark components that are orientation specific, pay particular attention to these.

1. Resistors - these are the smallest components.
2. **Diode** - The grey end of the diode goes to the end pointed to by the ‘arrow’ diode symbol on the silkscreen.
3. Ceramic Capacitors \(1uF\) - these have 105 printed on them.
4. **BC547 Transistor** - Caution, looks similar to the hall effect sensors but is larger. Will have 'BC547' printed on it. The ‘D’ shape of the transistor lines up with the ‘D’ shape on the silkscreen. There will be a few mm of leg between the transistor and the PCB
5. **Green LED** - The flat edge on the LED lines up with the flat edge on the silkscreen. It is labelled as PWM on the board as this is the signal it shows by default.
6. Polyfuse - this looks like a ceramic capacitor but the legs have inward bends at the top.
7. **Voltage Regulator** - The dot on the pink face lines up with the square solder point with the pink face to the outside edge of the PCB
8. **Electrolytic Capacitor \(22uF\)** - The -ve leg is marked by a grey stripe with a hollow '-' sign on it. The +ve leg goes in the hole next to the ‘+’ mark on the silkscreen.
9. PCB Socket \(header\) for Arduino and BT Module x 3 - Solder one pin first and check that it is flat to the PCB before soldering the rest.
10. **8-Pin DIP Socket** - There is an indentation on the silk screen image, this lines up with the indentation on the socket.
11. Connectors - Solder one pin first and check that it is flat to the PCB before soldering the rest.

The board is done! Remaining components in the kit go elsewhere in your car - see "[Connecting the eChook to the Car](https://docs.echook.uk/Connecting-the-eChook-to-the-Car/connecting-the-echook-to-the-car.html)"

Don’t plug in the op-amp, arduino or bluetooth module quite yet, carry out tests on the next page first.

High resolution photos of a finished board can be found [here](https://goo.gl/photos/QLNfrek9v2v522xa9).

### Video Instructions

Ian has recorded a video of building a board: [View on Youtube](https://www.youtube.com/watch?v=PspD6s5LoBA).

##  **PCB Component Reference Table**

| **Ref Name** | **Description** | **Value / Type** |
| :--- | :--- | :--- |
| BT | 6 way Pin Header |  |
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

Pin outs for the connectors on the eChook can be found in the 'Connecting the eChook to the car' section of the documentation [here](https://docs.echook.uk/Connecting-the-eChook-to-the-Car/connecting-the-echook-to-the-car.html).


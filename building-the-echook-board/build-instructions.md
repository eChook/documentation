# Build Instructions

In its simplest form, building the board consists of soldering all components in their correct places, as shown in the table below.

To make the process of soldering the board as easy as possible, it’s best to start with the smallest components first. All components sit on the top of the board, none on the bottom. The bottom of the board has the eChook logo and board version number printed on it, the top has hte component outline and values.

{% hint style="info" %}
See the next page for a step-by-step build guide.
{% endhint %}

High resolution photos of a finished board can be found [here](https://goo.gl/photos/QLNfrek9v2v522xa9). Note that this is a slightly earlier board where the bluetooth wires are soldered directly to the board instead of connected via a header. Also the components appearance may differ slightly to those supplied in the kits, as the suppliers may change between manufacturing runs.

### Video Instructions

Ian has recorded a video of building a board: [View on Youtube](https://www.youtube.com/watch?v=PspD6s5LoBA).

##  **PCB Component Reference Table**

{% hint style="info" %}
Use this table to identify which component goes to which label on the PCB
{% endhint %}

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

Once the board is fully populated there will be a few components remaining. These are the sensors that fit to the car. Your kit may also have a few spare components.

Pin-outs for the connectors on the eChook can be found in the 'Connecting the eChook to the car' section of the documentation.

{% page-ref page="../connecting-the-echook-to-the-car/" %}


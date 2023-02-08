---
description: This section covers assembling the eChook PCB
---

# Build Instructions

In its simplest form, building the board consists of soldering all components in their correct places, as shown in the table below.

To make the process of soldering the board as easy as possible, it’s best to start with the smallest components first. All components sit on the top of the board, none on the bottom. The bottom of the board has the eChook logo and board version number printed on it, the top has the component outline and values.

High resolution photos of a finished board can be found [here](https://goo.gl/photos/QLNfrek9v2v522xa9). Note that this is a slightly earlier board where the Bluetooth wires are soldered directly to the board instead of connected via a header. Also the components appearance may differ slightly to those supplied in the kits, as the suppliers may change between manufacturing runs.

### Glossary of Terms

If you are new to this, here is a little introduction to some of the terms used ahead:

* PCB - Printed Circuit Board, the white board in the kit that components are soldered to.
  * Soldermask - this is the white layer on the PCB. It stops solder sticking to areas it's not wanted (and makes the board look pretty)
  * Silkscreen - this is the black text/logos on top of the soldermask giving component references, values, text and logos.
* Solder Sucker - a tool that sucks up melted solder, good for removing components if they've been soldered in the wrong place.
* Solder Wick - a braided copper wick that can be used to soak up solder as an alternative to a Solder Sucker. Nicer to use but more expensive to buy.

### Video Instructions

Ian recorded the process of building up an earlier v1.2 board - with useful tips along the way:

{% embed url="https://www.youtube.com/watch?v=PspD6s5LoBA" %}

## &#x20;**PCB Component Reference Table**

Each component position on the PCB has a component reference next to it. The table below identifies the component for each reference.&#x20;

The Graphical BOM and images on the next page direct you through the build process.

| **Ref Name** | **Description**                             | **Value / Type** |
| ------------ | ------------------------------------------- | ---------------- |
| BT           | 6 way Pin Header                            |                  |
| C1           | Electrolytic Capacitor                      | 22uF             |
| C3           | Ceramic Capacitor                           | 1u               |
| C4           | Ceramic Capacitor                           | 1u               |
| C5           | Ceramic Capacitor                           | 1u               |
| Current      | Pluggable Terminal 5.08mm 4pin              | -                |
| D1           | Diode Schottky 1A 40V DO41                  | 1N5819RL         |
| Expansion    | -                                           | -                |
| Ext          | 4 Pin Connector, Pluggable Terminal, 5.08mm | -                |
| FS1          | Polyfuse, 250mA                             | 250mA            |
| MotorPWM     | 2 Pin Connector, Pluggable Terminal, 5.08mm | -                |
| PowerIn      | 3 Pin Connector, Pluggable Terminal, 5.08mm | -                |
| PWM          | LED 5mm                                     | -                |
| Q1           | Transistor                                  | BC547            |
| R1           | Resistor                                    | 82K              |
| R2           | Resistor                                    | 16K              |
| R3           | Resistor                                    | 82K              |
| R4           | Resistor                                    | 16K              |
| R5           | Resistor                                    | 10K              |
| R6           | Resistor                                    | 1K               |
| R7           | Resistor                                    | 10K              |
| R8           | Resistor                                    | 1K               |
| R9           | Resistor                                    | 1K               |
| R10          | Resistor                                    | 1K               |
| R11          | Resistor                                    | 1K               |
| R12          | Resistor                                    | 1K               |
| R13          | Resistor                                    | 1K               |
| R14          | Resistor                                    | 1K               |
| R15          | Resistor                                    | 470R             |
| R16          | Resistor                                    | 1K               |
| R17          | Resistor                                    | 1K               |
| R18          | Resistor                                    | 1K               |
| R19          | Resistor                                    | 1K               |
| R20          | Resistor                                    | 4K7              |
| R21          | Resistor                                    | 4K7              |
| R22          | Resistor                                    | 10K              |
| R23          | Resistor                                    | 10K              |
| R24          | Resistor                                    | 47K              |
| RPM          | Pluggable Terminal 5.08mm 4pin              | -                |
| Therm        | Pluggable Terminal 5.08mm 3pin              | -                |
| Throttle     | Pluggable Terminal 5.08mm 3pin              | -                |
| U1           | Arduino Headers                             | -                |
| U2           | Voltage Regulator, 5v 1A.                   | TSR\_1-2450      |
| U3           | Dual Op Amp                                 | MCP6002          |

Once the board is fully populated there will be a few components remaining. These are the sensors that fit to the car. Your kit will also have a few spare components - mostly spare resistors.

### Current Sensor Breakout Board (Kit v1.4+)

From kit v1.4 a PCB breakout board for the LEM current sensor is included. This carries the two 47nF capacitors, the 4.7nF capacitor and the current sensor as shown below:

![](<../.gitbook/assets/image (8).png>) ![](<../.gitbook/assets/image (14).png>)

{% hint style="info" %}
Pin-outs for the connectors on the eChook can be found in the [connecting-the-echook-to-the-car](../connecting-the-echook-to-the-car/ "mention") section of the documentation.
{% endhint %}


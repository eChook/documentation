# Power Regulator

This schematic shows the resettable polyfuse, reverse polarity protection and the 5V regulator.

![NOTE: The regulator is a TSR-1-2450. The reference to TSR-1-24120 below it is the PCB footprint used, which is the same.](<../.gitbook/assets/image (13).png>)

## Resettable Polyfuse

FS1 is a 250mA polyfuse. If the eChook board draws more than 250mA at 24v, the resistance of this fuse will increase from milli Ohms to a few Mega Ohms, effectively cutting power to the eChook. If there is a short circuit, this will cut off the power supply, limiting any damage. It also plays a role in reverse polarity protection, described below.

Once power is removed from the fuse it resets within a few seconds.

## Reverse Polarity Protection

This protects the board against the +24V and Ground being connected the wrong way around. Diode D1 is placed in reverse bias - under normal operation no current will flow through it, however if the input polarity is reversed it becomes a conductor, creating a low resistance current path from the ground rail to the 24v rail. This current all passes through the polyfuse and is considerably above its 250mA cutoff current which will cause it to break the circuit immediately.

## 5V Switching Regulator

Component U2 is the TRACOPOWER Switching Regulator. It takes any input voltage between 6.5V and 36V and provides a stable 5V output of up to 1A. C1 is a 22uF smoothing capacitor for the input voltage to the regulator, as specified in the datasheet.

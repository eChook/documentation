# Power Regulator

This schematic shows the resettable polyfuse, reverse polarity protection and the 5V regulator.

![NOTE: The regulator is a TSR-1-2450. The reference to TSR-1-24120 below it is the PCB footprint used, which is the same.](<../.gitbook/assets/image (13).png>)

## Resettable Polyfuse

FS1 is a 250mA polyfuse. If the eChook board draws more than 250mA at 24V, the resistance of this fuse increases from milliohms to a few megaohms, effectively cutting power to the eChook. If there is a short circuit, this cuts off the power supply and limits potential damage. It also plays a role in reverse polarity protection, described below.

Once power is removed from the fuse, it resets within a few seconds.

## Reverse Polarity Protection

This protects the board against the +24V and ground being connected the wrong way around. Diode D1 is placed in reverse bias - under normal operation no current flows through it. However, if the input polarity is reversed, it becomes a conductor, creating a low-resistance current path from the ground rail to the 24V rail. This current passes through the polyfuse and is considerably above its 250mA cut-off current, which causes it to break the circuit immediately.

## 5V Switching Regulator

Component U2 is the TRACOPOWER switching regulator. It takes any input voltage between 6.5V and 36V and provides a stable 5V output of up to 1A. C1 is a 22uF smoothing capacitor for the input voltage to the regulator, as specified in the datasheet.

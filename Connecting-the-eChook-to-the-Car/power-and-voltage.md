## Power to the Board {#docs-internal-guid-c4233111-09ca-8d5a-7c1c-1dfc2e9d0636}

To power the board in the car, connect the 0v pin on the ‘Power In’ socket to ground, and the +24v pin to the 24v battery supply on the car. To comply with greenpower regulations it is suggested to take power from after the isolator switch and the board must have it’s own fuse, nominally 5A, although 1A may be preferable.

## 24v Monitoring

This is the total battery voltage reading. It is taken directly from the boards power source, so no extra connections are needed.

## 12v Monitoring

This monitors the voltage of the ‘lower’ battery, allowing the system to monitor and log the voltages of both 12v batteries. This will show if one of the batteries is in a worse condition than the other.

The 12v monitoring requires a wire from the positive terminal of the lower battery, as shown by thewire\_12Vlabel in the diagram below:

![](/assets/Screenshot from 2017-11-29 22-00-19.png)

As this is a wire from the battery it requires a fuse of it’s own, a low value \(&lt;1A\) is recommended but 5A is sufficient. As this is simply a reference wire, no current will be drawn through it, so a thin wire can be used, however if a 5A fuse is used, ensure that the wire is rated to carry over 5A.


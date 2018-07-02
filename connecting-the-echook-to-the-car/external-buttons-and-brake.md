# External Buttons and Brake

There are three button inputs on the eChook board. Two of these are to interface with the app as using the touchscreen is generally inconvenient when driving and wearing gloves. One button cycles through the map and data screens on the app, while the other activates ‘launch’ mode to trigger lap counting. The final button input is to detect if the brakes are applied.

A push to make button \(not included in kit\) is required for each input, and is simply wired between the relevant button connection and a ground reference. This can be the reference on the ‘EXT’ connector, or ground elsewhere on the vehicle.

## Braking signal from brake light

As it is not always practical to attach another switch to the brake lever for logging purposes, it is also possible to connect the eChook to the brake light on the car instead. This requires a potential divider to step down the voltage driving the brake light voltage to 5v. To design the potential divider, follow the same guide as for connecting the throttle, and simply connect the output to the brake input. Depending on the car the brake light could be switched on the +ve side \(i.e. 24v side\) or the ground side. Ensure that the connection to the eChook is made on the switched side of the light, as shown below for a 24V brake light system.

![](https://lh4.googleusercontent.com/V9i01vwxJSmsg6HIEdEN-fDVn4EpTTwEAoKph0fRIcXXVdiyJ8_yV-685Dqug5seFBuX_EMQA9VhIa_k5-lMQ6drWDLhKY50Kt7-IPJhLIe6O4urHIDyd4UJt6qDwfbRr9VQf6p_)

eChook logs for the circuit on the left will show high \(100\) when the brake is pressed and low \(0\) when it is not pressed. The circuit on the right will give the inverse of this. It will still be apparent when the brake is on and off, however could be neatened in the eChook Arduino code.


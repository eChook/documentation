# Throttle Input

Throttle input is useful to log to see how the car is being driven, however due to the number of different ways throttles are implemented on cars there are a few methods of interfacing it to the eChook.

A throttle input is also needed for the apps lap counter feature, as this uses the throttle to determine race start.

Finally, the eChook will take a variable throttle and output a PWM signal that can be used as an input to a higher power motor driver circuit. The green LED on the eChook board is connected to this output.

## Variable throttle 0v-5v

This is the input that the eChook board is designed for. If a variable throttle input is used, it is likely that it already works in this voltage range, however confirm this with a multimeter before attaching anything. If it does, simply run a second wire from the output to the ‘Throttle In’ pin on the eChook nano board. The board can also provide power and ground to the throttle.

## Variable throttle with output above 5v:

The output from the throttle will need to be reduced such that the highest output voltage is stepped down to 5v in order to interface with the eChook Board. To do this a potential divider will be needed. For potential divider design, see [this SparkFun tutorial](https://learn.sparkfun.com/tutorials/voltage-dividers). \(Tip: to reduce current use, choose the resistors such that the sum of R1 and R2 is around 10kΩ\)

For example: If the maximum output of the throttle is 10v, a potentiometer is needed that reduces this to 5v. As this is halving the voltage, R1 and R2 will be equal. 5kΩfor each is a sensible figure to use.

Connect the potential divider as shown:

![](https://lh5.googleusercontent.com/KW_L3b9ZulcJHl2DW7X59uPfOaAb0Wx-hhOOY05LV8JsQ-45gsAX87I-p3_iwrGjc9t9DdA0AJs7RcMXF0zFeOA8yvB3myBPQoFCtgvISXY-wqJguEm9DNX9WkTusLDgDmWt9u7F)

Warning: Use a multimeter to verify that the output from the throttle to the board \(eChook\_Board\_Throttle\_Inabove\) does not exceed 5V before connecting it to the board. Higher voltages are likely to damage the arduino.

## Push Button Throttle

If the vehicle runs a push button throttle, the same potential divider as above will be needed. For a button switching a 24v signal, set R1=82k and R2 = 16k. This drops 30V to 5V and is intended to protect against the batteries having higher voltages than 12V each.

The second tweak needed for a push button throttle is in code. Within the code there are two ‘readThrottle’ functions, one for a variable throttle input, one for a push button. By default the push button function is commented out:

![](https://lh6.googleusercontent.com/CAEAoiHKOEKyukwirS0e39eVdBUcFY0UA1xSfdo8wJKsOlWa445s51SyLxOuQwxCtJMV_cZVKudRkI758Xg3MbpXjaRO3Wg8_Y1CxmcRzcYLdZvecekJte78wcOjE3PVGOOJbQX_)In order to use a push button throttle, comment out or delete the first function and un-comment the lower one.


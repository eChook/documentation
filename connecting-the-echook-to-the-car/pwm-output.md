# PWM Output

This output will most likely not be used. It provides a 500Hz, 5V PWM output with the duty cycle mirroring the throttle input percentage. 

This can be used as an input to a custom motor driver circuit such as the one used on the Driven and weChook cars, or as an input into some 4QD motor drivers. 

An example schematic for a custom motor controller is below. Built well it should be reliable, and we can give advice, but attempt this at your own risk, and a backup relay \(as shown below\) is recommended!! The most important thing to note is that the copper on a PCB can not handle the current required for the motor - we used large aluminium bus bars bolted on top of the PCB.

![](https://lh5.googleusercontent.com/3pW04xyPngyTtoq86KlSpStIkefsHWNe5GYhydUF1aXQbb3hvtONRAx4F8aLCk-sMGE9HXBWJxQmkSKZ48EOJFgjw-_s3rADhfrZxiAv-pmPF7jSbnq84uhIN7_AKJrLfaOeZKhX)

